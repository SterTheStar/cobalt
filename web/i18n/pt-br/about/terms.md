<script lang="ts">
    import { t } from "$lib/i18n/translations";
    import SectionHeading from "$components/misc/SectionHeading.svelte";
</script>

<section id="general">
<SectionHeading
    title={$t("about.heading.general")}
    sectionId="general"
/>

estes termos aplicam-se apenas ao uso da instância oficial do cobalt.
em outros casos, você pode precisar contatar o responsável pela instância para obter informações precisas.
</section>

<section id="saving">
<SectionHeading
    title={$t("about.heading.saving")}
    sectionId="saving"
/>

a funcionalidade de salvar simplifica o download de conteúdo da internet
e não assumimos nenhuma responsabilidade sobre o uso do conteúdo salvo.

os servidores de processamento funcionam como proxies avançados e nunca gravam o conteúdo solicitado no disco.
tudo é tratado na RAM e removido permanentemente assim que o túnel é concluído.
não mantemos logs de downloads e não podemos identificar ninguém.

você pode saber mais sobre como os túneis funcionam na [política de privacidade](/about/privacy).
</section>

<section id="responsibility">
<SectionHeading
    title={$t("about.heading.responsibility")}
    sectionId="responsibility"
/>

você (usuário final) é responsável pelo que faz com nossas ferramentas, como usa e distribui o conteúdo gerado.
por favor, seja cuidadoso ao usar conteúdo de terceiros e sempre credite os criadores originais.
certifique-se de não violar nenhum termo ou licença.

quando usado para fins educacionais, cite sempre as fontes e credite os criadores originais.

uso justo e créditos beneficiam todos.
</section>

<section id="abuse">
<SectionHeading
    title={$t("about.heading.abuse")}
    sectionId="abuse"
/>

não temos como detectar automaticamente comportamentos abusivos porque o cobalt é totalmente anônimo.
porém, você pode reportar essas atividades para nós por e-mail e faremos o possível para agir manualmente: abuse[at]imput.net

**este e-mail não é destinado ao suporte ao usuário, você não receberá resposta caso sua dúvida não seja relacionada a abuso.**

se estiver enfrentando problemas, pode buscar suporte por qualquer método disponível na [página da comunidade](/about/community).
</section>
