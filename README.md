# St. Joseph's Schola — Website

A hand-coded, production-ready marketing website for a classical Catholic boys' boarding school (grades 8–12). No build step, no frameworks, no external dependencies. Open `index.html` in any browser or upload the whole folder to any static host.

## Folder structure

```
/index.html              Home
/pages/
  about.html             About — story, identity, philosophy, faculty
  business.html          Business & Entrepreneurship (flagship page)
  academics.html         Classical Academics
  farm.html              Farm & Land
  spiritual-life.html    Spiritual Life
  boarding-life.html     Boarding Life
  admissions.html        Admissions + inquiry form
  contact.html           Contact + message form + map
/css/
  styles.css             Single shared stylesheet (palette + type via CSS custom properties)
  site.js                Mobile nav, scroll-fade animation, footer year
/images/                 Empty — drop real photography here (filenames listed below)
```

## How to edit the look

All colors and type live as CSS custom properties at the top of `css/styles.css` under `:root`. Change the palette there once and it updates site-wide. The current palette is deep green + navy with a warm cream base and gold used sparingly. Typography uses high-quality system serifs (no web-font download required); to swap in a web font, add one `<link>` in each page `<head>` and update `--serif` / `--sans`.

---

## PLACEHOLDERS TO REPLACE

Everything below is marked in the HTML with square brackets `[LIKE THIS]` so you can find-and-replace.

### School contact info (appears in the footer of EVERY page + the Contact page)
- `[STREET ADDRESS]`
- `[TOWN]` — the Kansas town
- `[ZIP]`
- `[PHONE]` — display phone number
- `[PHONE-DIGITS]` — digits only, used in the `tel:` link on Contact (e.g. `13165551234`)
- `[EMAIL]` — general email
- `[ADMISSIONS EMAIL]` — admissions email (Contact page)
- `[DAYS & HOURS]` — office hours (Contact page)

### Identity (Home)
- `[LATIN MOTTO]` and `[English translation of the school motto]` — patron/motto section
- Patron saint is set to **St. Joseph the Worker** as requested. Change in the patron section of `index.html` if needed.

### Campus roadmap years (Home)
- `[YEAR]` appears 4× in the development roadmap (Phases I–IV)

### Faculty bios (About) — all names, degrees, and details are placeholders
- `[HEADMASTER NAME]`, `[CHAPLAIN NAME]`, `[DIOCESE]`
- `[ENTERPRISE DIRECTOR NAME]`, `[INDUSTRY]`
- `[LATIN MASTER NAME]`, `[FARM DIRECTOR NAME]`, `[DEAN OF MEN NAME]`, `[BACKGROUND]`
- `[DEGREE, INSTITUTION]` (3×) and `[NAME]` (used within several bios)

### Admissions / tuition (Admissions)
- `[ANNUAL TUITION]`, `[ENROLLMENT DEPOSIT]`, `[AID DETAILS / DEADLINE]`
- `Fall [YEAR]` — placeholder text in the "Desired Year of Entry" field

### Map (Contact)
- `[MAP EMBED]` — replace the placeholder block with an embedded Google Map or a static map image

---

## FORMS — connect before going live

Three forms currently post to placeholder anchors. Point each `action` at your mail handler, form service, or CRM:
- Admissions inquiry form (`admissions.html`) → `action="#admissions-endpoint"`
- Contact message form (`contact.html`) → `action="#contact-endpoint"`
- Newsletter signup (footer, all pages) → `action="#newsletter-endpoint"`

The "Make a Gift" / "Support the Campaign" buttons currently link to `#contact-endpoint` — point them at your donation platform.

## SOCIAL LINKS — add real URLs

Footer social icons (Facebook, Instagram, YouTube) and the footer/social `href="#"` values are placeholders. Add your real profile URLs.

---

## IMAGES — drop real photography into `/images/`

There are no `<img>` tags yet; every image is a labeled placeholder block styled in CSS, each with descriptive alt text and a suggested filename. When you have real photography, replace each placeholder `<div class="img-ph">…</div>` with an `<img src="images/FILENAME" alt="…">` (or `../images/FILENAME` on interior pages). Suggested filenames by page:

- **Home:** `campus-golden-hour.jpg` (hero — also supports video), `students-pitching-a-business-plan.jpg`, `st-joseph-the-worker-patron.jpg`, `capital-campaign-chapel-rendering.jpg`
- **Business:** `boys-running-farm-market-stand.jpg`, `students-running-farm-pnl.jpg`
- **About:** `about-campus-walk-golden-hour.jpg`, `boy-at-morning-mass.jpg`, plus six faculty portraits (`faculty-*.jpg`)
- **Academics:** `latin-class.jpg`, `logic-seminar-debate.jpg`
- **Farm:** `boys-working-the-farm-sunrise.jpg`, `animal-husbandry-barn.jpg`, `crops-and-harvest.jpg`, `farm-to-table-kitchen.jpg`, `land-stewardship-fencing.jpg`, `trades-workshop.jpg`, `weekend-market-stand.jpg`, `farm-as-business-ledger.jpg`
- **Spiritual Life:** `chapel-mass-candlelight.jpg`, `spiritual-direction.jpg`
- **Boarding Life:** `common-meal-refectory.jpg`, `bunkhouse-interior.jpg`, `shared-meals.jpg`, `athletics-rugby.jpg`, `the-outdoors.jpg`, `evening-recreation.jpg`, `mentorship-houses.jpg`, `authentic-masculinity-brotherhood.jpg`
- **Admissions:** `admissions-family-visit.jpg`
- **Contact:** `contact-school-gate.jpg`

The crest is a text placeholder ("SJ" in a gold circle). Replace the `.crest` markup in the header/footer with your real crest image when ready.

---

## Notes
- Mobile-first and responsive; navigation collapses to a toggle menu under ~1040px.
- Accessible: semantic HTML5, labeled form fields, alt text on every image placeholder, skip-to-content link, and reduced-motion support.
- The verification pass confirmed all internal links resolve and no broken image references exist.
