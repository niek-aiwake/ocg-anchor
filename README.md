# ocg-anchor

Extern anker voor de evidence log van de Ontological Compliance Gateway
(OCG). Specificatie: `docs/evidence-spec.md` §7 in de (private) OCG-repo.

- `keys/ocg-signer.pub`: de publieke Ed25519-sleutel van de signer (base64),
  met de `keyid` in `keys/KEYID`. Vastgelegd in de eerste commit.
- `checkpoints/<tree_size>.json`: ondertekende checkpoints (DSSE-envelope,
  JCS) met `tree_size` en `root_hash` van de log. Geen persoonsgegevens.

Regels: alleen nieuwe bestanden toevoegen; nooit wijzigen, verwijderen of
force-pushen. Branch protection op `main` dwingt dat af. Een getuige-kopie
buiten de server slaat alarm bij een non-fast-forward.
