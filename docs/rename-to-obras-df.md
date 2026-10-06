# Rename to Obras DF

Prepared on 2026-10-06. The GitHub rename and publication are pending merge approval. The intended repository is `noah-art3mis/obras-df`; the intended report address is `https://simulacro.cv/obras-df/`.

The currently published revision, `2e6a21d52ca7a5d7cee4faf3778bed21460ad1ba`, is preserved on `archive/published-takehome-2026-10-06`. Keep that branch as the original publication record.

## References found

| Location                                   | Reference                                             | Treatment                                                 |
| ------------------------------------------ | ----------------------------------------------------- | --------------------------------------------------------- |
| This repository                            | README, report HTML and notebook links                 | Updated in the rename branch                              |
| Python project metadata                    | Project name in `pyproject.toml` and `uv.lock`         | Updated to `obras-df`; dependency versions unchanged        |
| `noah-art3mis.github.io/projects.markdown`   | Project name and old GitHub Pages URL                  | Prepared as a redirect PR, then a canonical-link PR        |
| Main website                               | Old report directory and `index.html` addresses       | Companion branch redirects to the new report path          |
| `design/portfolio-redesign` website branch  | Older copy of the project listing                     | Integrate the companion change before publishing redesign |
| `feat/local-marimo` analysis branch         | README, notebook, package metadata and planning links | Integrate the rename after the active text review          |
| `~/projects/simulacro-blog/`                | Source URLs in README, post plan and research workbook | Update current source links after the public rename        |
| Saved notebook and HTML diagnostic outputs | Old absolute filesystem paths in historical warnings | Preserve as execution provenance                          |

Local checkout paths remain unchanged while the marimo editor is active. Internal notebook filenames containing `lablivre` remain valid and do not contain `takehome`. Moving the primary checkout later requires repairing Git worktree metadata and updating the blog's local path references; it is not required for the public rename.

## Citation audit

Searched local projects and worktrees, including HTML/JSON/notebook exports, the CV repository, both remote CV feature branches, the CV/portfolio worktree, the personal website and its redesign, the Simulacro Tech sources, local blog material, application notes, and text documents in Downloads. No matching citations were found in the CV sources. Twelve PDF files were checked for both extracted text and embedded hyperlinks, including the website CV, local CV exports/archives and two CVs in Windows Downloads; none contained a LabLivre reference. Some files are duplicate copies.

The remote `portfolio-lis` README contained no citation. Account-wide GitHub code search and public web search found no additional relevant citations, but search indexes are incomplete. Private Ghost drafts, sent applications and other people's copies were not inspected. Preserving the old report address covers the known entry URLs in copies we cannot update.

## Publication sequence

1. Obtain merge approval for the coordinated PRs. First merge the main website preparation PR (`chore/obras-df-links`), which adds the old-path redirect and the Obras DF label while retaining the currently working report URL.
2. Wait for the main website's successful GitHub Pages deployment and confirm its deployed commit includes that preparation change. A merged PR is not evidence of deployment. Keep the current project repository name until this check succeeds.
3. Rename the existing GitHub repository to `obras-df`. Do not create a replacement repository under the old name: that would disable GitHub's repository redirects. Confirm Pages still publishes `main` from `/`, request a rebuild if needed, and wait for the new report address to serve successfully. The source content still has its old links at this point; the deployed redirect keeps them working.
4. Verify the new report and the old-address redirects, then merge the project rename PR and retarget/merge the stacked website canonical-link PR (`chore/obras-df-canonical-link`) to `main`. Update the repository homepage to `https://simulacro.cv/obras-df/` and its description to describe planned investment rather than expenditure. Wait for both resulting deployments.
5. Update the local `origin` URL to `https://github.com/noah-art3mis/obras-df.git`. This also updates linked worktrees that share the remote configuration.
6. Check the new report, assets and interactive figures. Check both old hostnames (`simulacro.cv` and `noah-art3mis.github.io`) at `/takehome-lablivre-analysis/` and `/takehome-lablivre-analysis/index.html`, including a real section anchor and query string. The companion redirect preserves both when JavaScript is enabled and provides a normal link otherwise. Other old project-file paths are outside this redirect's scope. If GitHub Pages has not yet routed both sites correctly, stop the remaining cutover steps and investigate rather than claiming completion.
7. Update the local blog's current repository/report URLs and integrate the rename into the marimo and website-redesign branches without overwriting active edits. Keep historical source revisions and the archive branch intact.
8. Verify the normal deployments and clean up only the merged rename worktrees and branches. Keep the preparation branch until the stacked PR is retargeted. Keep the active marimo worktree and archival branch.

GitHub automatically redirects repository URLs after a rename, but does not automatically redirect GitHub Pages project URLs. The old report route therefore lives in the main website repository. See [GitHub's rename documentation](https://docs.github.com/en/repositories/creating-and-managing-repositories/renaming-a-repository).

## Validation before publication

The companion redirect has one browser regression test covering both old entry URLs, with a query string and executive-summary section anchor. It failed with HTTP 404 before the redirect existed and passed after implementation. It serves the real redirect file with a destination fixture; live GitHub Pages routing remains a post-deployment check.

The project lockfile validates offline. The notebook and report edits are limited to their public links and the HTML document title; existing cells, outputs and heading IDs remain intact. A full local Jekyll build is not established by the redirect test.
