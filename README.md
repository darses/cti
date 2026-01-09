# CTI

> Free CTI, so it can't be bad.

## Interact.sh domains (interactsh-domains.txt)

Last update: 2026-01-07

List of Out-of-Band / OAST interact.sh domains, intended for inclusing in detection rules or searches. Contains all servers found in SMTP services via Shodan query using `product:"Interactsh SMTP Server" port:25` and extracted with `jq -r '.data' | grep 220 | cut -d ' ' -f 2`. Addtionally Interact.sh domains without SMTP were found and addedd with the query `http.html:"<h1> Interactsh Server </h1>"` and extracted with `jq -r .data | grep Server | cut -d ' ' -f 2`. A `.`-prefix format is used to clarify this requires a wildcard subdomain match. The list may contain inactive servers which were historically seen.

The file `interactsh-domains-checked.txt` contains the Nuclei output for the templates `dns-interactsh-detect.yaml`, `ldap-interactsh-detect.yaml`, `smtp-interactsh-detect.yaml`, and `interact-server.yaml`. The resulting hosts were scanned with `ssl-dns-names.yaml`, `ssl-issuer.yaml` and `dnsx -a -aaaa -asn -cdn -list`.

## Burp Collaborator Server domains (burpsuite-domains.txt)

List of Out-of-Band / OAST Burp Collaborator Server domains, found in SMTP services via Shodan query using `port:25 "Burp Collaborator Server ready"`.
