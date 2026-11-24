# Website and deployment readiness

Review snapshot: 2026-11-24. Public GitHub repository trees and the local portfolio were inspected. No source repository was cloned or changed, and nothing was deployed.

## Project evidence and status

| Project                      | Public evidence                                         | Portfolio description                                                                                                                                                                    |
| ---------------------------- | ------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SEREN                        | Python and PowerShell files, including a text-chat CLI. | Early-stage AI assistant prototype. Voice and wake features remain experimental. Shared configuration and offline tests are not claimed because they are not in the current public tree. |
| CS50x                        | README and one Scratch project file.                    | A learning archive; the public files do not establish course completion.                                                                                                                 |
| MallConnect                  | No matching public repository was found.                | Clearly marked private and under development, with no source or implementation details linked.                                                                                           |
| Book launch site             | No matching public repository or demo was verified.     | Clearly marked as a local prototype; no working purchase flow is claimed.                                                                                                                |
| Other inspected repositories | README-only, license-only, or data-only public trees.   | Not presented as completed websites or live demos.                                                                                                                                       |

No project screenshots or live demos were verified. The portfolio's project artwork is typographic illustration, not a product screenshot.

## Browser checks

- Served the static site locally and checked it in headless Chrome at 1440×1000, 390×844, and 320×740.
- All sections rendered at each size. The four navigation links reached their sections, and no horizontal overflow was detected.
- No browser console errors or failed network requests occurred. The site uses a local SVG favicon and no project-image assets.
- LinkedIn rejected automated requests from this environment, so its destination could not be independently confirmed here. The GitHub profile and both linked repositories returned HTTP 200.
- Keyboard testing confirmed the first Tab focuses the visible skip link. Screen-reader and assistive-technology testing has not been performed.

## GitHub Pages workflow

The manual workflow at `.github/workflows/pages.yml` packages the static `site` directory and deploys it when manually dispatched. It uses the maintained `actions/checkout@v7`, `actions/upload-pages-artifact@v5`, and `actions/deploy-pages@v5.0.1` actions. It grants read-only repository contents access and grants Pages and OIDC permissions only to the deployment job. It contains no secrets.

The workflow has not been dispatched, and Pages is not enabled. Before deployment, create the public GitHub repository and set **Settings → Pages → Build and deployment → Source** to **GitHub Actions**. Then manually run the `Manual portfolio Pages deployment` workflow.

## Remaining publication steps

1. Review the public-facing content and the staged file list.
2. Create `AnugrahM/Anugrah-Portfolio` on GitHub without adding starter files.
3. Push the local `main` branch to that repository.
4. Set the Pages source to GitHub Actions and manually dispatch the workflow.

This checklist records the publication preparation steps; update the deployment status after the first Pages release.
