# filipvariciuc1.github.io

Hosts the public key for a personal Tesla Fleet API app (Tesla Auto phone key).
Public key only; nothing secret lives here.

Served at
https://filipvariciuc1.github.io/.well-known/appspecific/com.tesla.3p.public-key.pem
(EC, NIST P-256, as Tesla requires). Tesla reads it from that exact path when the app
registers this domain, so the path and file name must not change.

## Before changing anything

- **Rotating the key** means generating a new P-256 pair, replacing the `.pem` here, and
  registering the domain with Tesla again; the car-side virtual key has to be re-added too.
  The private half never goes in this repo.
- **Do not add a `CNAME`, `index.html` or `404.html` here.** This is the user site, so the
  whole domain is shared with project sites such as
  [cameras-app](https://filipvariciuc1.github.io/cameras-app/), whose home and privacy pages
  back a Google OAuth consent screen. A custom domain here would move all of them.
- `.nojekyll` turns Jekyll off so files are published as-is, dot-folder included.
