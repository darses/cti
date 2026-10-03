# CTI

> Free CTI, so it can't be bad.

## Interact.sh domains (interactsh-domains.txt)

Last update: 2026-10-03

List of Out-of-Band / OAST interact.sh domains, intended for inclusing in detection rules or searches. Contains all servers found in SMTP services via Shodan query using `product:"Interactsh SMTP Server" port:25` and extracted with `jq -r '.data' | grep 220 | cut -d ' ' -f 2`. A `.`-prefix format is used to clarify this requires a wildcard subdomain match. The list only contains active servers according to the Nuclei template `dns-interactsh-detect.yaml`.

## Burp Collaborator Server domains (burpsuite-domains.txt)

List of Out-of-Band / OAST Burp Collaborator Server domains. Shodan queries: `"X-Collaborator-Version"`, `port:25 "Burp Collaborator Server ready"`. A `.`-prefix format is used to clarify this requires a wildcard subdomain match.
