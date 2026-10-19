# nofracing.se

The NOF Racing website. Plain HTML and CSS, hosted free on GitHub Pages.

## Files

- `index.html`: the English page
- `sv/index.html`: the Swedish page
- `style.css`: all styling
- `assets/`: logo and icons
- `CNAME`: tells GitHub Pages to serve the site on nofracing.se
- `.nojekyll`: serve files as they are, no Jekyll build

## Put it online

1. Create a new **public** repository on github.com, for example `nofracing`.
2. Push this folder to it:

   ```
   git remote add origin https://github.com/LinusWillmont/nofracing.git
   git push -u origin main
   ```

3. In the repository, open **Settings > Pages**.
   Set **Source** to "Deploy from a branch", branch `main`, folder `/ (root)`, and save.
4. Under **Custom domain**, check that it says `nofracing.se`. GitHub reads it from the CNAME file.

## DNS at Simply.com

In the Simply.com control panel, open **DNS** for nofracing.se and add these records.
Remove any existing A, AAAA or CNAME records for `@` and `www` first. Leave MX and TXT records for email alone.

| Type  | Name | Value                  |
|-------|------|------------------------|
| A     | @    | 185.199.108.153        |
| A     | @    | 185.199.109.153        |
| A     | @    | 185.199.110.153        |
| A     | @    | 185.199.111.153        |
| AAAA  | @    | 2606:50c0:8000::153    |
| AAAA  | @    | 2606:50c0:8001::153    |
| AAAA  | @    | 2606:50c0:8002::153    |
| AAAA  | @    | 2606:50c0:8003::153    |
| CNAME | www  | linuswillmont.github.io |

DNS can take up to a few hours. When GitHub shows the domain as verified, tick **Enforce HTTPS** in Settings > Pages.

Optional but recommended: verify the domain under your GitHub account
(**Settings > Pages > Add a domain**) so nobody else can claim it on GitHub Pages.
GitHub gives you a TXT record to add at Simply.com.

## Editing

Change text in `index.html`, then commit and push. The site updates within a minute or two.
