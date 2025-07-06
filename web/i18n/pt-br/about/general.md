<script lang="ts">
    import { t } from "$lib/i18n/translations";
    import { contacts, docs } from "$lib/env";

    import SectionHeading from "$components/misc/SectionHeading.svelte";
</script>

<section id="summary">
<SectionHeading
    title={$t("about.heading.summary")}
    sectionId="summary"
/>

cobalt ajuda você a salvar qualquer coisa dos seus sites favoritos: vídeo, áudio, fotos ou gifs. basta colar o link e você já está pronto para usar!

sem anúncios, rastreadores, paywalls ou outras bobagens. apenas um aplicativo web prático que funciona em qualquer lugar, quando você precisar.
</section>

<section id="motivation">
<SectionHeading
    title={$t("about.heading.motivation")}
    sectionId="motivation"
/>

cobalt foi criado para o benefício público, para proteger as pessoas de anúncios e malwares empurrados por downloaders alternativos.
acreditamos que o melhor software é seguro, aberto e acessível. todos os projetos imput seguem esses princípios básicos.
</section>

<section id="privacy-efficiency">
<SectionHeading
    title={$t("about.heading.privacy_efficiency")}
    sectionId="privacy-efficiency"
/>

todas as requisições para o backend são anônimas e todas as informações sobre possíveis túneis de arquivos são criptografadas.
temos uma política rígida de zero registros e não armazenamos nem rastreamos *nada* sobre pessoas individuais.

se uma requisição requer processamento adicional, como remuxing ou transcodificação, o cobalt processa a mídia
diretamente no seu dispositivo. isso garante melhor eficiência e privacidade.

se seu dispositivo não suporta processamento local, então o processamento ao vivo baseado no servidor é usado.
nesse caso, a mídia processada é transmitida diretamente para o cliente, sem nunca ser armazenada no disco do servidor.

você pode [ativar o túnel forçado](/settings/privacy#tunnel) para aumentar ainda mais a privacidade.
quando ativado, o cobalt irá tunelar todos os arquivos baixados, não apenas aqueles que precisem.
ninguém saberá de onde você está baixando algo, nem mesmo seu provedor de rede.
tudo o que verão é que você está usando uma instância do cobalt.
</section>

<section id="community">
<SectionHeading
    title={$t("about.heading.community")}
    sectionId="community"
/>

cobalt é usado por inúmeros artistas, educadores e criadores de conteúdo para fazer o que amam.
estamos sempre em contato com nossa comunidade e trabalhamos juntos para tornar o cobalt ainda mais útil.
fique à vontade para [participar da conversa](/about/community)!

acreditamos que o futuro da internet é aberto, por isso o cobalt é
[source first](https://sourcefirst.com/) e [fácil de hospedar]({docs.instanceHosting}).

se seu amigo hospeda uma instância de processamento, basta pedir o domínio e [adicioná-lo nas configurações da instância](/settings/instances#community).

você pode conferir o código-fonte e contribuir [no github]({contacts.github}) a qualquer momento.
recebemos todas as contribuições e sugestões com prazer!
</section>