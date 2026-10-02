# Inventari live → repository — 2 tetor 2026

Ky dokument dallon atë që u vëzhgua live nga ajo që vetëm ekziston në GitHub. `main` nuk konsiderohet automatikisht version production.

| Produkti | URL live | Runtime i vëzhguar | Repository / branch | Përfundimi i provenance |
|---|---|---|---|---|
| SmartSearch | https://smartsearch.al/ | Cloudflare, Next.js/OpenNext, D1 | `gentmeci/smartsearch.al` / `main` | Bundle-i publik përputhet me build-in e `f4d573d2...`; Worker version ID kërkon rivërtetim |
| AskGenie | https://askgenie.al/ | Cloudflare para PHP 8.4/Laravel; MySQL sipas repo | `gentmeci/askgenie-platform` / `main` | Familja e kodit përputhet; SHA aktiv nuk është ekspozuar |
| MerrMakine | https://merrmakine.com/en | Cloudflare, Next.js/OpenNext, D1 | `gentmeci/merrmakine.com` / `main` | Disa asete nuk përputhen me build-in e `68bd6c6`; mos sinkronizo source pa version ID |
| MerrMakine Laravel | jo domaini live aktual | Laravel/VPS target i veçantë | `gentmeci/merrmakine-laravel` / `main` | Ruaje të ndarë; mos e mbishkruaj me Next.js |
| meci.al | https://meci.al/ | WordPress/PHP pas Cloudflare | `gentmeci/meci-al` / `main` | Snapshot zhvillimi i WordPress; live DB/uploads/config jashtë Git |
| vaj.al | https://vaj.al/ | WordPress/Cloudron pas Cloudflare | `gentmeci/vaj-al` / `main` | `main` dokumentohet si kopje e WordPress-it live; DB/uploads/config jashtë Git |
| Vaj Site (i palançuar) | `meci-olive-vaj-al.meci-associa-5380.chatgpt.site` | 401, privat | `gentmeci/vaj-al` / `cloudflare-static`; PR #1 hapur | Nuk është `vaj.al` live dhe 401 nuk është defekt production |

## Kufijtë operacionalë

- Mos ndërro domain, route, database, secret ose branch production pa evidence të versionit dhe miratim.
- Për Cloudflare regjistro gjithmonë: commit SHA, upload/version ID, deployment ID, compatibility flags, migrations dhe rollback version.
- Për WordPress ruaj ndarjen kod/database/uploads/config dhe bëj snapshot të hostit para çdo release të ardhshëm.
- “Vaj Site” mbetet preview i veçantë deri në miratim; PR #1 nuk duhet trajtuar si defekt i faqes WordPress live.

## Raportet e hollësishme

- [SmartSearch](https://github.com/gentmeci/smartsearch.al/blob/codex/live-audit-2026-10-02/docs/AUDIT_2026_10_02.md)
- [AskGenie](https://github.com/gentmeci/askgenie-platform/blob/codex/live-audit-2026-10-02/docs/AUDIT_2026_10_02.md)
- [MerrMakine Next.js](https://github.com/gentmeci/merrmakine.com/blob/codex/live-audit-2026-10-02/docs/AUDIT_2026_10_02.md)
