<script lang="ts">
    import env from "$lib/env";
    import { t } from "$lib/i18n/translations";

    import SectionHeading from "$components/misc/SectionHeading.svelte";
</script>

<section id="instance">
<SectionHeading
    title={$t("about.heading.instance")}
    sectionId="instance"
/>

this instance of cobalt is hosted by [canine.tools](https://canine.tools). you can read more about the canine.tools project [here](https://canine.tools/about).

this subdomain is proxied through cloudflare to prevent abuse from bots & scrapers against the api.
</section>

<section id="apikeys">
<SectionHeading
    title={$t("about.heading.apikeys")}
    sectionId="apikeys"
/>

api keys can be used to bypass the restrictions against the api. however, api keys are given by request and only under certain conditions:

<ul>
<li>no commercial use of any kind. this means you cannot use this api for your own "downloader" with ads</li>
<li>no use for ai training</li>
<li>no spam requests</li>
</ul>
keys can be revoked at any point under the discretion of this instance owner.
</section>

<section id="credits">
<SectionHeading
    title={$t("about.heading.credits")}
    sectionId="credits"
/>

this version of cobalt web is running a fork, licensed under the same license as cobalt. you can find the changes of the fork [here](https://github.com/caninetools/cobalt).

the api itself is running unmodified cobalt using the docker provided image.
</section>