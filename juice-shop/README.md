# OWASP Juice Shop: Testing Log

## Setup
```bash
docker run -d -p 3000:3000 bkimminich/juice-shop
```
Open `http://localhost:3000`. Proxy traffic through Burp Suite.

## Scope
Local instance only (`localhost:3000`).

## Findings

| ID | Vulnerability | Location | Severity | Write-up |
|---|---|---|---|---|
| JS-01 | SQL injection (login) | /rest/user/login | High | [findings/js-01.md](findings/) |
| JS-02 | Broken access control | admin section | High | |
| JS-03 | IDOR | basket / user data | Medium | |
| JS-04 | XSS | search / feedback | Medium | |
| JS-05 | Sensitive data exposure | exposed files / API | Medium | |

_The rows above are targets to aim for. Edit them to match what you actually find._

## Finding write-up format (per file in `findings/`)
- Title and severity
- Affected endpoint
- Steps to reproduce (with Burp screenshots)
- Impact
- Recommended fix
