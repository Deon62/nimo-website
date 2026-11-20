# nimo.ardena.co.ke

Static website for the Nimo app: landing page plus the pages Google Play needs.

| Page | URL | Use |
| --- | --- | --- |
| Home | `/` | Landing page |
| Privacy Policy | `/privacy/` | Play Console → App content → Privacy policy |
| Terms of Service | `/terms/` | Linked from the app and store listing |
| Delete account | `/delete-account/` | Play Console → Data safety → Account deletion URL |
| Support | `/support/` | Store listing contact / support URL |
| Payment complete | `/payment-complete/` | Paystack `callback_url`; sends the user back to the app (`nimo://`) |

Plain HTML and CSS, no build step. Preview locally with `python -m http.server` and open http://localhost:8000.

## Hosting

**GitHub Pages:** Settings → Pages → Deploy from branch `master` / root. The `CNAME` file sets the domain.

**Render (static site):** New → Static Site → this repo, build command empty, publish directory `.`, then add the custom domain.

**DNS:** add a `CNAME` record for `nimo` on `ardena.co.ke` pointing to `deon62.github.io` (GitHub Pages) or the
`*.onrender.com` host Render shows you.
