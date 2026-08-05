# B5 Secure MTA-STS

Production static site for the `b5secure.com` MTA-STS policy endpoint.

## Required endpoint

`https://mta-sts.b5secure.com/.well-known/mta-sts.txt`

The policy starts in `testing` mode. After TLS-RPT monitoring and validation, change `mode: testing` to `mode: enforce`, deploy the update, verify the production endpoint, and then update the `_mta-sts.b5secure.com` TXT record with a new policy ID.

## Deployment

- Azure Static Web Apps
- App location: `/`
- API location: blank
- Output location: blank
- Custom domain: `mta-sts.b5secure.com`

The root landing page contains no analytics, cookies, forms, third-party JavaScript, remote fonts, or external assets.
