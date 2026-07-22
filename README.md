# revyoos-updates

Update files for the **Revyoos Widget Loader** WordPress plugin.

This repository does not contain the plugin's source code — it only hosts:

- The JSON manifest describing the latest available version
  (`revyoos-widget-loader.json`)
- The `.zip` file for each release (`revyoos-widget-loader-X.Y.Z.zip`)

The plugin installed on each WordPress site checks this JSON periodically
and, if it finds a newer version, shows the usual "update available"
notice in `wp-admin`.

## Publishing a new version

1. Upload the new `.zip` as an asset of a [Release](../../releases) (or as
   a raw file in this repo, depending on how you've set it up).
2. Update `revyoos-widget-loader.json`:
   - `version` → new version number (must exactly match the `Version:`
     header and the `REVYOOS_WL_VERSION` constant in the plugin)
   - `download_url` → URL of the new `.zip`
   - `sections.changelog` → release notes for the new version
   - `last_updated` → release date
3. Done. Sites will detect it automatically on their next check (or when
   clicking "Check Again" in Updates, if there's no recent cache).

No other action is needed on client sites.
