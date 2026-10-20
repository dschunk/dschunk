# Portfolio website and GitHub review — October 19, 2026

This is a source-control and public-endpoint maintenance record, not an assertion that every authenticated workflow or third-party service has been manually tested. Times below are Eastern Daylight Time on October 19 unless otherwise indicated.

## Completed changes

- **Everyday IT Tips**: published three evidence-first field guides (Entra Connect Sync, Exchange Online shared mailbox permissions/forwarding, and Windows DNS dynamic registration). Updated homepage, guide archive, relevant Windows/infrastructure/operations topic pages, search index, RSS, sitemap and validation coverage. [Source commit](https://github.com/dschunk/everydayITtips/commit/40adf376d72470f2562c4ba7430f5e0bfa13c297). [Validation run](https://github.com/dschunk/everydayITtips/actions/runs/39364058231).
- **DavidSchunk.com**: surfaced all three articles on the portfolio homepage and writing/reference library; refreshed corresponding sitemap modification dates. [Source commit](https://github.com/dschunk/davidschunk.com/commit/9a092de225a4fab00c51a8c60e2c7a8d3974852b). [Validation](https://github.com/dschunk/davidschunk.com/actions/runs/39364218742).
- **GitHub profile**: featured the new field guides in the workbench section.
- **SchunkOps tools**: linked companion field guides from the Windows toolkit and Microsoft 365 README files, without touching script execution logic.
- **Website health workflow**: added three production article URL probes and Voice of Adoptees homepage/Worker-health probes. [Monitoring workflow run](https://github.com/dschunk/dschunk/actions/runs/39364396568).

## Verified

- The three new article URLs returned **HTTP 200** from the GitHub Actions production monitoring runner on October 19, 2026. This confirms reachable paths at that time, not search-index inclusion or every embedded asset's behavior.
- Everyday IT Tips static-site validation passed.
- DavidSchunk.com source build/validation passed after the changes.
- The pre-existing site health suite reported success for its 12 targets before expansion; a passing probe can also mean HTTP 403 was explicitly classified as unverified rather than a confirmed healthy response. Read per-job summaries before claiming universal uptime.

## Open issue: Voice of Adoptees production cutover

The built source site is not conclusively what the domain currently serves. [Deployment run 38120145539](https://github.com/dschunk/voiceofadoptees.com/actions/runs/38120145539) validated successfully, but the workflow skipped Wrangler deployment because the expected Cloudflare credentials were unavailable, and its `/api/health` probe returned HTTP 404 on multiple attempts. The newer centralized website health workflow also returned HTTP 404 from that health endpoint. The publicly indexed root page still showed older-season copy. Existing [deployment issue #4](https://github.com/dschunk/voiceofadoptees.com/issues/4) and [cutover issue #1](https://github.com/dschunk/voiceofadoptees.com/issues/1) track related work.

**Remediation checklist:**

1. In Cloudflare, confirm the zone is active, the apex/www DNS records and redirects are intentional, and the requested domain is attached to the intended Worker/route.
2. Supply the least-privileged Cloudflare token and account ID to the correct GitHub Actions repository/environment secrets. Do not store their values in Git.
3. Verify deployment actually ran rather than reporting a validation-only success. Check Cloudflare Worker name `voiceofadoptees-com`, its static assets, the `EMAIL` binding, and private contact destination configuration before enabling the form.
4. Require `GET https://voiceofadoptees.com/api/health` to return JSON with `ok: true`, then verify the current homepage/episodes/guest pages and a real non-production contact-form test.
5. Keep old route redirects in place to preserve indexed links after cutover.

## Watch items

- The Russian Adoptees Organization homepage contains a dated advisory for **October 22, 2026**. Confirm the event's actual outcome and update the headline/banner promptly after October 22, citing the official source. Do not publish unconfirmed venue or service details.
- The **Department of Cash** project should not be rebranded to a new business name until branding/domain and legal clearance and deployment targets are resolved; preserve existing links in the meantime.
- Several other static or authenticated sites have repository-level validators but require periodic browser-based smoke tests, authenticated workflow checks, and hosting logs to validate more than public HTTP responses.

## Ongoing routine

- Review [website health runs](https://github.com/dschunk/dschunk/actions/workflows/site-health.yml) and treat HTTP 403 as *unverified*, never as proof that a site is functioning.
- Review deploy logs separately from build and test logs. Production correctness is a different question from compiling.
- On publishing new Everyday IT Tips content, update archive, topic hubs, search index, RSS, sitemap and structured metadata together; publish via a single atomic commit and require the validation workflow to pass.
- Keep secrets, private case data, contact destinations, and employer systems out of public repositories.
