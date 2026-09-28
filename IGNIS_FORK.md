# Ignis Yopass fork

`ignis` is the deployed branch. It starts at upstream release `14.10.0` and
keeps a small frontend-only patch: Ignis name and icon defaults. The upstream
license checks and secret-sharing behavior are unchanged. Deployment policy
settings such as `DISABLE_FEATURES` and `NO_LANGUAGE_SWITCHER` belong in the
Coolify Compose definition, not in this fork.

`master` follows the GitHub fork of `jhaals/yopass`. The `upstream` Git remote
points to `https://github.com/jhaals/yopass.git`. To take a later upstream
release, fetch it, create a branch from `ignis`, merge the release tag into
that branch, test it, and open a PR back to `ignis`. The image workflow publishes
an immutable commit tag to GHCR when `ignis` advances. Promote the digest to
Coolify only after verifying the image and an end-to-end one-time secret.

Keep upstream `LICENSE` and notices intact. The icon comes from the Ignis
workspace brand assets.
