<script lang="ts">
    import env from "$lib/env";
    import { t } from "$lib/i18n/translations";

    import SectionHeading from "$components/misc/SectionHeading.svelte";
</script>

<section id="general">
<SectionHeading
    title={$t("about.heading.general")}
    sectionId="general"
/>

a política de privacidade do cobalt é simples: não coletamos nem armazenamos nada sobre você.
o que você faz é exclusivamente seu negócio, não nosso nem de mais ninguém.

estes termos aplicam-se apenas ao uso da instância oficial do cobalt.
em outros casos, você pode precisar contatar o responsável pela instância para informações precisas.
</section>

<section id="local">
<SectionHeading
    title={$t("about.heading.local")}
    sectionId="local"
/>

ferramentas que usam processamento no dispositivo funcionam offline, localmente,
e nunca enviam dados processados para lugar algum.
elas são explicitamente identificadas assim sempre que aplicável.
</section>

<section id="saving">
<SectionHeading
    title={$t("about.heading.saving")}
    sectionId="saving"
/>

ao usar a funcionalidade de salvar, o cobalt pode precisar proxyar ou remuxar/transcodificar arquivos.
se for o caso, um túnel temporário é criado para esse propósito
e informações mínimas necessárias sobre a mídia são armazenadas por 90 segundos.

em uma instância do cobalt oficial e sem modificações,
**todos os dados do túnel são criptografados com uma chave que somente o usuário final possui**.

os dados criptografados do túnel podem incluir:
- nome do serviço de origem.
- URLs originais dos arquivos de mídia.
- argumentos internos necessários para diferenciar tipos de processamento.
- metadados mínimos do arquivo (nome gerado, título, autor, ano de criação, informações de copyright).
- informações mínimas sobre a requisição original que podem ser usadas em caso de falha na URL durante o processo de tunelamento.

esses dados são removidos irremediavelmente da RAM do servidor após 90 segundos.
ninguém tem acesso aos dados em cache do túnel, nem mesmo os donos da instância,
desde que o código fonte do cobalt não seja modificado.

os dados de mídia dos túneis nunca são armazenados ou cacheados em nenhum lugar.
tudo é processado ao vivo, mesmo durante remuxing e transcodificação.
os túneis do cobalt funcionam como um proxy anônimo.

se seu dispositivo suporta processamento local,
as informações criptografadas do túnel contêm muito menos dados, pois são retornadas ao cliente.

veja o [código fonte relacionado no github](https://github.com/imputnet/cobalt/tree/main/api/src/stream)
para saber mais sobre como isso funciona.
</section>

<section id="encryption">
<SectionHeading
    title={$t("about.heading.encryption")}
    sectionId="encryption"
/>

os dados temporariamente armazenados do túnel são criptografados usando o padrão AES-256.
as chaves de decriptação estão incluídas somente no link de acesso e nunca são registradas, cacheadas ou armazenadas em qualquer lugar.
apenas o usuário final tem acesso ao link e às chaves de criptografia.
as chaves são geradas de forma única para cada túnel solicitado.
</section>

{#if env.PLAUSIBLE_ENABLED}
<section id="plausible">
<SectionHeading
    title={$t("about.heading.plausible")}
    sectionId="plausible"
/>

usamos o [plausible](https://plausible.io/) para obter um número aproximado
de usuários ativos do cobalt, de forma totalmente anônima. nenhuma informação identificável sobre
você ou suas requisições é armazenada. todos os dados são anonimizados e agregados.
auto-hospedamos e gerenciamos a [instância plausible](https://{env.PLAUSIBLE_HOST}/) usada pelo cobalt.

o plausible não usa cookies e é totalmente compatível com GDPR, CCPA e PECR.

se desejar sair da análise anônima, você pode fazer isso nas [configurações de privacidade](/settings/privacy#analytics).
se sair, o script do plausible não será carregado.

[saiba mais sobre o compromisso do plausible com a privacidade](https://plausible.io/privacy-focused-web-analytics).
</section>
{/if}

<section id="cloudflare">
<SectionHeading
    title={$t("about.heading.cloudflare")}
    sectionId="cloudflare"
/>

usamos os serviços do cloudflare para:
- proteção contra ddos e abusos.
- proteção contra bots (cloudflare turnstile).
- hospedagem e deploy do app web estático (cloudflare workers).

todos esses são necessários para proporcionar a melhor experiência para todos.
o cloudflare é o provedor mais privado e confiável que conhecemos para todas essas soluções.

o cloudflare é totalmente compatível com GDPR e HIPAA.

[saiba mais sobre o compromisso do cloudflare com a privacidade](https://www.cloudflare.com/trust-hub/privacy-and-data-protection/).
</section>
