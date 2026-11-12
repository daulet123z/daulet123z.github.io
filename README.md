# Portfolio: landing pages for small businesses

A one-page portfolio that links to four landing page projects. Plain HTML, CSS and JavaScript, no build step.

| Project | Live site | Code |
|---|---|---|
| Larkhaven Coffee (coffee shop) | [daulet123z.github.io/coffee-shop-landing](https://daulet123z.github.io/coffee-shop-landing/) | [coffee-shop-landing](https://github.com/daulet123z/coffee-shop-landing) |
| Brass & Bristle (barbershop) | [daulet123z.github.io/barbershop-landing](https://daulet123z.github.io/barbershop-landing/) | [barbershop-landing](https://github.com/daulet123z/barbershop-landing) |
| Velvet & Bloom (beauty salon) | [daulet123z.github.io/beauty-salon-landing](https://daulet123z.github.io/beauty-salon-landing/) | [beauty-salon-landing](https://github.com/daulet123z/beauty-salon-landing) |
| Brightnook (cleaning service, Bootstrap 5) | [daulet123z.github.io/cleaning-service-landing](https://daulet123z.github.io/cleaning-service-landing/) | [cleaning-service-landing](https://github.com/daulet123z/cleaning-service-landing) |

## Structure

```
index.html        Page content: hero, projects, services, process, contact
css/style.css     Styles; colors, fonts and spacing are in :root at the top
js/main.js        Reveal-on-scroll animation and footer year
assets/           Project screenshots (desktop 1200×750, mobile 390×844) and favicon
```

## Run locally

```bash
python -m http.server 5500
```

Then open <http://localhost:5500>.

## Editing

- **Your name:** replace `daulet123z` in the logo and footer of `index.html`.
- **Fiverr link:** the "Hire me" button in the header and "Hire me on Fiverr" in the Contact section point to the public profile `https://www.fiverr.com/daulet_turarbek`. To link a specific gig instead, change both `href` values.
- **Add a project:** copy one `<article class="project">` block, then change the texts, links and the two screenshots. Every second project automatically shows its image on the other side.
- **Screenshots:** a desktop shot at 1440×900 scaled to 1200 px wide, and a phone shot at 390×844. Compress them as JPG (quality around 75–80).
- **Colors and fonts:** edit the `:root` block in `css/style.css`. If you change fonts, also update the Google Fonts `<link>` in `index.html`.

## Deploy to GitHub Pages

To make this page the main address `https://daulet123z.github.io/`, publish it from a repository named exactly `daulet123z.github.io`:

```bash
git init -b main
git add .
git commit -m "Portfolio page"
gh repo create daulet123z/daulet123z.github.io --public --source . --push
```

Then in the repository open **Settings → Pages** and choose **Deploy from a branch**, branch `main`, folder `/ (root)`. The three project sites keep their own addresses under the same domain.
