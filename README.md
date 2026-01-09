# CTI

> Free CTI, so it can't be bad.

## Interact.sh domains (interactsh-domains.txt)

Last update: 2026-01-07

List of Out-of-Band / OAST interact.sh domains, found in SMTP services via Shodan query using `product:"Interactsh SMTP Server" port:25` and extracted with `jq -r '.data' | grep 220 | cut -d ' ' -f 2`. Addtionally Interact.sh domains without SMTP were found and addedd with the query `http.html:"<h1> Interactsh Server </h1>"` and extracted with `jq -r .data | grep Server | cut -d ' ' -f 2`.

The file `interactsh-domains-checked.txt` contains the Nuclei output for the templates `dns-interactsh-detect.yaml`, `ldap-interactsh-detect.yaml`, `smtp-interactsh-detect.yaml`, `interact-server.yaml`, `ssl-dns-names.yaml`, `ssl-issuer.yaml`. Additionally the output of `dnsx -a -aaaa -asn -cdn -list` was added.

## Burp Collaborator Server domains (burpsuite-domains.txt)

List of Out-of-Band / OAST Burp Collaborator Server domains, found in SMTP services via Shodan query using `port:25 "Burp Collaborator Server ready"`.
