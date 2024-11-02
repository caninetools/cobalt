<script lang="ts">
    import env from "$lib/env";
    import { t } from "$lib/i18n/translations";

    import OuterLink from "$components/misc/OuterLink.svelte";
    import SettingsToggle from "$components/buttons/SettingsToggle.svelte";
    import SettingsCategory from "$components/settings/SettingsCategory.svelte";
</script>

<SettingsCategory sectionId="tunnel" title={$t("settings.privacy.tunnel")}>
    <SettingsToggle
        settingContext="privacy"
        settingId="alwaysProxy"
        title={$t("settings.privacy.tunnel.title")}
        description={$t("settings.privacy.tunnel.description")}
    />
</SettingsCategory>

{#if env.PLAUSIBLE_ENABLED}
    <SettingsCategory sectionId="plausible" title={$t("settings.privacy.plausible")}>
        <SettingsToggle
            settingContext="privacy"
            settingId="disableAnalytics"
            title={$t("settings.privacy.plausible.title")}
            description={$t("settings.privacy.plausible.description")}
        />
        <div class="subtext learn-more-plausible">
            <OuterLink href="https://plausible.io/privacy-focused-web-analytics">
                {$t("settings.privacy.plausible.learnmore")}
            </OuterLink>
        </div>
    </SettingsCategory>
{/if}

{#if env.UMAMI_ENABLED}
    <SettingsCategory sectionId="umami" title={$t("settings.privacy.umami")}>
        <SettingsToggle
            settingContext="privacy"
            settingId="disableAnalytics"
            title={$t("settings.privacy.umami.title")}
            description={$t("settings.privacy.umami.description")}
        />
        <div class="subtext learn-more-plausible">
            <OuterLink href="https://umami.is/features">
                {$t("settings.privacy.umami.learnmore")}
            </OuterLink>
        </div>
    </SettingsCategory>
{/if}

<style>
    .learn-more-plausible {
        padding-top: 6px;
    }
</style>
