<script lang="ts">
    import { contacts, docs, partners } from "$lib/env";
    import { t } from "$lib/i18n/translations";

    import SectionHeading from "$components/misc/SectionHeading.svelte";
    import BetaTesters from "$components/misc/BetaTesters.svelte";
</script>

<section id="imput">
<SectionHeading
    title="imput"
    sectionId="imput"
/>

cobalt é feito com amor e carinho por [imput](https://imput.net/) ❤️

somos uma pequena equipe de duas pessoas, mas trabalhamos duro para criar softwares de qualidade que beneficiem todos.
se você gosta do nosso trabalho, considere apoiá-lo na [página de doações](/donate)!
</section>

<section id="testers">
<SectionHeading
    title={$t("about.heading.testers")}
    sectionId="testers"
/>

um enorme agradecimento aos nossos testadores por testarem as atualizações antecipadamente e garantirem sua estabilidade.
eles também nos ajudaram a lançar o cobalt 10!
<BetaTesters />

todos os links são externos e levam para seus sites pessoais ou redes sociais.
</section>

<section id="partners">
<SectionHeading
    title={$t("about.heading.partners")}
    sectionId="partners"
/>

parte da infraestrutura de processamento do cobalt
é fornecida por nosso parceiro de longa data, [royalehosting.net]({partners.royalehosting})!
</section>

<section id="meowbalt">
<SectionHeading
    title={$t("general.meowbalt")}
    sectionId="meowbalt"
/>

meowbalt é o mascote veloz do cobalt, um gato muito expressivo que ama internet rápida.

toda a arte incrível do meowbalt que você vê no cobalt
foi feita por [GlitchyPSI](https://glitchypsi.xyz/).
ele também é o criador original do personagem.

a imput detém os direitos legais sobre o design do personagem meowbalt,
mas não sobre artes específicas criadas por GlitchyPSI.

nós amamos o meowbalt, então precisamos estabelecer algumas regras para protegê-lo:
- você não pode usar o design do meowbalt de nenhuma forma que não seja fan art.
- você não pode usar o design ou artes do meowbalt comercialmente.
- você não pode usar o design ou artes do meowbalt em seus próprios projetos.
- você não pode usar ou modificar as artes do meowbalt feitas por GlitchyPSI de nenhuma forma.

se você criar fan art do meowbalt, compartilhe com a gente no
[nosso servidor do Discord](/about/community), adoraríamos ver!
</section>

<section id="licenses">
<SectionHeading
    title={$t("about.heading.licenses")}
    sectionId="licenses"
/>

o código da API do cobalt (servidor de processamento) é open source e licenciado sob a [AGPL-3.0]({docs.apiLicense}).

o código do frontend do cobalt é [source first](https://sourcefirst.com/) e está licenciado sob a [CC-BY-NC-SA 4.0]({docs.webLicense}).

precisamos tornar o frontend source first para impedir golpistas de lucrarem com nosso trabalho
e para evitar clones maliciosos que enganam as pessoas e prejudicam nossa imagem pública.
tirando o uso comercial, ele segue os mesmos princípios de muitas licenças open source.

nós utilizamos muitas bibliotecas de código aberto, mas também criamos e distribuímos as nossas.
você pode ver a lista completa de dependências no [github]({contacts.github})!
</section>
