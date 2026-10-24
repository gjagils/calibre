# Calibre

Calibre desktop (`ghcr.io/linuxserver/calibre`) via de standaard pipeline:
GitHub Actions → GHCR → Tailscale → Portainer (stack `calibre`) op de Synology. Web-GUI op poort 7081.

## Updates

- **Nieuwe Calibre-versie:** Dependabot kijkt dagelijks. Minor/patch-updates (9.17 → 9.18) worden automatisch
  gemerged en uitgerold (`dependabot-automerge.yml`). Een major-update (10.x) blijft als PR staan.
- **Security-rebuilds van dezelfde versie:** de deploy-workflow bouwt elke maandag 04:00 opnieuw.
- **Terugdraaien:** revert de update-commit op main; de pipeline rolt de vorige versie weer uit.

## Stack-env (Portainer)

| Variabele | Betekenis |
|---|---|
| `CUSTOM_USER` | Gebruikersnaam voor de web-GUI |
| `PASSWORD` | Wachtwoord voor de web-GUI |

Back-up van vóór de overstap (Calibre 9.3.1): `/volume1/docker/_backups/calibre-2026-10-24`.
