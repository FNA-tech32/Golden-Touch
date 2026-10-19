# Golden Touch

Static website for Golden Touch, a nail studio and cosmetics salon in Kassel. Visitors can browse treatments, view the gallery, and book an appointment online. The site is available in German, Russian, and English.

## Pages

| File | Purpose |
| --- | --- |
| `index.html` | Public site: services, gallery, reviews, booking, contact |
| `admin.html` | Staff panel for appointments and service prices |
| `impressum.html` | Legal notice |
| `datenschutz.html` | Privacy policy |
| `agb.html` | Terms of service |

## Run locally

Root links such as `/admin.html` and `/impressum.html` need a local web server. From this folder:

```bash
npx serve
```

Then open the URL printed in the terminal (usually `http://localhost:3000`).

## Stack

- HTML pages styled with Tailwind CSS loaded from a CDN
- Custom styles in `assets/css/style.css` and `assets/css/admin.css`
- Client behavior in `assets/js/main.js` and `assets/js/admin.js`
- Bookings stored in Supabase
- Confirmation mail sent with EmailJS

Connection values for Supabase and EmailJS live in `assets/js/main.js`. Keep those keys out of documentation and public commits when you rotate them.

## Languages

The default language is German. Visitors can switch to Russian or English.

- Short interface copy uses `data-de`, `data-ru`, and `data-en` attributes on the HTML.
- Service lists, gallery labels, reviews, and FAQ answers are defined in `assets/js/main.js`.

## Contact details

Studio address, phone, WhatsApp, email, and Instagram are written in:

- `index.html` — contact section, booking shortcuts, map, footer, and the schema.org block
- `impressum.html`, `datenschutz.html`, and `agb.html` — legal pages
- `assets/js/main.js` — `ADMIN_EMAIL`, the address that receives booking notifications

Update all of those together when the studio details change.

Current public details:

- Address: Obere Königsstraße 8, 34117 Kassel
- Phone and WhatsApp: +49 561 430 2180
- Email: kontakt@goldentouch.de
- Instagram: @golden.touch.studio

## Folder layout

```
assets/css/          site and admin styles
assets/js/           public site and admin scripts
assets/images/       photos used on the homepage
supabase_procedures.sql   service-price table for Supabase
```
