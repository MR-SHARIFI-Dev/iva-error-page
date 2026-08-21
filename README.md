<div align="center">
  <img src="assets/iva-eror-logo.svg" width="92" alt="IVA EROR PAGE logo">
  <h1>IVA EROR PAGE</h1>
  <p><strong>When things break, good design should still respond.</strong></p>
  <p>Professional single-file error pages for cPanel, DirectAdmin, Apache, Nginx and Linux servers.</p>
  <p><a href="README.fa.md">Persian</a> · <strong>English</strong></p>
  <p><img alt="HTML" src="https://img.shields.io/badge/HTML5-single--file-E34F26?style=flat-square&logo=html5&logoColor=white"> <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-vanilla-F7DF1E?style=flat-square&logo=javascript&logoColor=111"> <img alt="RTL" src="https://img.shields.io/badge/RTL-ready-24a148?style=flat-square"> <img alt="License" src="https://img.shields.io/badge/license-MIT-ff4d3d?style=flat-square"></p>
</div>

![IVA EROR PAGE repository poster](assets/iva-eror-page-poster.png)

IVA EROR PAGE is a bilingual error-page laboratory and open-source collection. Select a status, preview it live, and download a production-ready standalone HTML file. Every generated page includes its CSS internally and has zero dependencies.

## Included templates

| Status | Template |
|---|---|
| 400 | Bad Request |
| 401 | Authentication Required |
| 403 | Access Forbidden |
| 404 | Page Not Found |
| 408 | Request Timeout |
| 429 | Too Many Requests |
| 500 | Internal Server Error |
| 502 | Bad Gateway |
| 503 | Service Unavailable |
| 504 | Gateway Timeout |
| OFF | Offline Page |
| MTN | Maintenance Page |

## Features

- One production file: `index.html`
- Strictly separated English and Persian interfaces
- Live preview and one-click template downloads
- Copy complete HTML to clipboard
- RTL and LTR layouts
- Responsive desktop, tablet and mobile design
- Error-specific colors, telemetry, glitch and signal effects
- Dark and light themes
- No external libraries, trackers, API keys or build tools
- GitHub Pages deployment workflow
- Custom SVG logo, social poster, issue template and documentation

## Run locally

Open `index.html` directly or run:

```bash
python -m http.server 8080
```

## cPanel installation

Download the desired template, upload it to `public_html`, and assign it from **Advanced → Error Pages**. Alternatively, add:

```apache
ErrorDocument 404 /404.html
ErrorDocument 500 /500.html
ErrorDocument 503 /503.html
```

## DirectAdmin installation

Upload the matching file to the domain error directory, commonly:

```text
/domains/example.com/public_html/404.shtml
```

Your provider may use `404.html` or a dedicated errors directory.

## Nginx installation

```nginx
error_page 404 /404.html;
error_page 500 502 503 504 /500.html;

location = /404.html {
    root /var/www/example.com/public;
    internal;
}
```

Validate and reload Nginx after updating the configuration.

## GitHub Pages

Set **Settings → Pages → Source** to **GitHub Actions** and push to `main`.

## Customization

Search the downloaded file for `IVA EROR PAGE`, `/`, and `#ff4d3d` to change the brand, home link and accent color.

Read [CONTRIBUTING.md](CONTRIBUTING.md) and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) before contributing. Released under the [MIT License](LICENSE).
