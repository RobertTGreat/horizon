# Launcher UI direction review — PR #1614

🤖 Agent: Prepared by Robert’s OpenAI Codex agent for the [requested direction review](https://github.com/ludovic111/horizon/pull/1614#issuecomment-6390428558).

**Before:** owner’s registry/profile baseline [#1640](https://github.com/ludovic111/horizon/pull/1640), `dbdc0389fe9ce9d46911f7f0b8bff12b83eb7607`.

**After:** complete draft UI series [#1628](https://github.com/ludovic111/horizon/pull/1628), `465bed263326c4b2dacb857fadaedbae5852b462`, including that registry baseline. The after images show the combined direction across #1612–#1628, not only the changes in #1614.

## Player problems addressed

- **Home:** Choose the instance to launch beside Play while keeping the existing landscape, version picker and Home layout.
- **Content:** Find and manage content with Installed/Browse, compact source/sort/filter controls and page-size selection, leaving more room for useful results.
- **Versions:** Tell installed builds from available downloads immediately without repeating the page title above them.
- **Settings:** Reach the relevant controls through icon sections instead of scrolling through every setting, including the existing AI opt-out and connect-agent configuration.
- **Instance:** Manage an individual profile from one workspace with its launch/setup action, content controls, worlds, files, logs and settings; pagination and visible-row rendering bound large lists.

## Dark appearance

| Screen | Before | After |
| --- | --- | --- |
| Home | [![Before dark Home](images/before-dark-home.jpg)](images/before-dark-home.jpg) | [![After dark Home](images/after-dark-home.jpg)](images/after-dark-home.jpg) |
| Content | [![Before dark Content](images/before-dark-content.jpg)](images/before-dark-content.jpg) | [![After dark Content](images/after-dark-content.jpg)](images/after-dark-content.jpg) |
| Versions | [![Before dark Versions](images/before-dark-versions.jpg)](images/before-dark-versions.jpg) | [![After dark Versions](images/after-dark-versions.jpg)](images/after-dark-versions.jpg) |
| Settings / Launcher | [![Before dark Settings / Launcher](images/before-dark-settings.jpg)](images/before-dark-settings.jpg) | [![After dark Settings / Launcher](images/after-dark-settings.jpg)](images/after-dark-settings.jpg) |
| Imported instance workspace | [![Before dark Imported instance workspace](images/before-dark-instance.jpg)](images/before-dark-instance.jpg) | [![After dark Imported instance workspace](images/after-dark-instance.jpg)](images/after-dark-instance.jpg) |

## Light appearance

| Screen | Before | After |
| --- | --- | --- |
| Home | [![Before light Home](images/before-light-home.jpg)](images/before-light-home.jpg) | [![After light Home](images/after-light-home.jpg)](images/after-light-home.jpg) |
| Content | [![Before light Content](images/before-light-content.jpg)](images/before-light-content.jpg) | [![After light Content](images/after-light-content.jpg)](images/after-light-content.jpg) |
| Versions | [![Before light Versions](images/before-light-versions.jpg)](images/before-light-versions.jpg) | [![After light Versions](images/after-light-versions.jpg)](images/after-light-versions.jpg) |
| Settings / Launcher | [![Before light Settings / Launcher](images/before-light-settings.jpg)](images/before-light-settings.jpg) | [![After light Settings / Launcher](images/after-light-settings.jpg)](images/after-light-settings.jpg) |
| Imported instance workspace | [![Before light Imported instance workspace](images/before-light-instance.jpg)](images/before-light-instance.jpg) | [![After light Imported instance workspace](images/after-light-instance.jpg)](images/after-light-instance.jpg) |

## Horizon registry

The draft retains Horizon as a native browser source, exposes signature/capability information beside Install, and makes registry packs available as their own profiles. Java-specific sort/filter controls are hidden for the Horizon source. **Visible interaction change for direction review:** the draft puts Modrinth/Horizon in a source dropdown rather than keeping the baseline’s permanent source tabs.

| Screen | Before | After |
| --- | --- | --- |
| Horizon registry | [![Before dark Horizon registry](images/before-dark-registry.jpg)](images/before-dark-registry.jpg) | [![After dark Horizon registry](images/after-dark-registry.jpg)](images/after-dark-registry.jpg) |

| Screen | Before | After |
| --- | --- | --- |
| Horizon registry | [![Before light Horizon registry](images/before-light-registry.jpg)](images/before-light-registry.jpg) | [![After light Horizon registry](images/after-light-registry.jpg)](images/after-light-registry.jpg) |

## Design-system fit

The launcher-specific **Blocks** section of `docs/design-system.md` governs these screens: the existing dark/light token palettes, Horizon mark and wordmark, purple primary actions, Pixelify headings/actions, Geist/Geist Mono reading text, square outlined/bevelled panels, pixel icons, stone background and generated landscape are retained. The changes concentrate on hierarchy, navigation and density; imported source art stays inside icon slots. Settings keep icon-and-title section controls; the AI section retains the opt-out and connection setup.

## Additional states

- [Home instance picker — dark](images/after-dark-home-instance-picker.jpg)
- [Browser source picker — dark](images/after-dark-source-picker.jpg)
- [Browser source picker — light](images/after-light-source-picker.jpg)
- [AI settings and connect-agent setup — dark](images/after-dark-ai-settings.jpg)
- [AI settings and connect-agent setup — light](images/after-light-ai-settings.jpg)
- [Native Horizon pack workspace — dark](images/after-dark-registry-instance.jpg)
- [Native Horizon pack workspace — light](images/after-light-registry-instance.jpg)

## Capture notes and limits

These are unedited captures of the actual native Windows GPUI launcher, at the same 1182 × 762 window size, in both appearances. No game was launched. Each run used isolated temporary game, launcher, data and configuration folders, with self-update disabled and an offline preview identity.

Modrinth cards use live catalog metadata and source artwork; metadata can change between captures. Both browser views show the broad catalog. The Horizon browser uses the owner's checked-in registry fixture, including Coordinates HUD. Its unavailable remote icon falls back to a letter slot.

The imported “UI sample pack” has 24 synthetic report entries; “Cozy” is a prepared native-profile fixture with the checked-in signed Coordinates HUD sample and 24 empty sample resource-pack ZIPs. Counts and port/compatibility labels on the sample instance are fixture data, not compatibility test results. “Set up files” / disabled Play is expected because these homes contain no prepared game or game executable. The screenshots do not demonstrate a completed install or launch flow.

The baseline's imported-instance management is embedded in Mods → Modpacks; it has no equivalent standalone Content Workspace. That embedded view is the “before” instance screenshot.

These files are review media only, stored separately from the code PRs. Screenshots show layout and direction; they are not a substitute for interaction, accessibility or performance testing. The independent fixes #1612 and #1613 can be reviewed separately while the larger UI direction is discussed.

🤖 Generated with OpenAI Codex in T3 Code.
