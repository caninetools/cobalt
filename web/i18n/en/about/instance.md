<script lang="ts">
    import { t } from "$lib/i18n/translations";
    import SectionHeading from "$components/misc/SectionHeading.svelte";
</script>

<section id="about">
<SectionHeading
    title={$t("about.heading.instance_about")}
    sectionId="about"
/>

this cobalt instances is hosted by the [canine.tools project](https://canine.tools/).
</section>

<section id="services">
<SectionHeading
    title={$t("about.heading.instance_services")}
    sectionId="services"
/>

we use a vpn for all outbound requests.

youtube is known to not work 100% of the time. we use a session server for youtube, so keep trying until it works.

other services should work fine.
</section>

<section id="apikeys">
<SectionHeading
    title={$t("about.heading.instance_apikeys")}
    sectionId="apikeys"
/>

we offer api keys for developers to use. keys are given by request once we approved your usage. they can be revoked at anytime without warning.

if you want an api key, please email [hyper@canine.tools](mailto:hyper@canine.tools) ([PGP key](https://canine.tools/assets/hyper%40canine.tools.asc)). please email for a key, do not contact the maintainer via other methods or they will be ignored.

when you request an api key, please include the following:

* the purpose of using our cobalt instance
* ips and user agents your program uses
* how often your program will use the api roughly

furthermore, here are some general rules. all rules from [canine.tools terms](https://canine.tools/terms/) also apply here.

* mass downloading of media is okay
* no commercial use. this includes requiring to pay to use your program, access to downloading media must be free. this also means no ads.
* no downloading media for ai training

we don't generally monitor requests, but we may contact you if we see anything suspicious.

</section>

<section id="fork">
<SectionHeading
    title={$t("about.heading.instance_fork")}
    sectionId="fork"
/>

our instance (web and api) is running a fork of the main cobalt codebase. it's licensed under the same license. you can find all changes on [our repository](https://github.com/caninetools/cobalt).

* [api license](https://github.com/caninetools/cobalt/blob/main/api/README.md#license)
* [web license](https://github.com/caninetools/cobalt/blob/main/web/README.md#license)

</section>