# dify-image-mirror

One-time helper repo. DGX (`spark-5581`) can't reach `registry-1.docker.io` directly
(upstream router/ISP appears to block/filter it), but it can reach `github.com`/`ghcr.io`
fine. This repo's GitHub Actions workflow pulls the handful of images the Dify project
needs from Docker Hub (from GitHub's own network, unaffected) and re-pushes them to
`ghcr.io`, so DGX can pull from there instead.

Trigger manually: Actions tab -> "Mirror Dify images to ghcr.io" -> Run workflow.
