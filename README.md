# Mehboob Qazi — personal portfolio (presentation-based update)

Responsive SaaS-inspired portfolio, retaining **React + Vite, CSS, JavaScript, Framer Motion, Three.js via React Three Fiber**.

**Source of truth:** `Mehboob_Executive_Profile.pptx` (1 slide); changes traced in `SOURCE_MAPPING.md`.

## Run locally

Node.js 20.19+ or 22+ recommended. Extract the ZIP and, from the extracted project folder, run:

```bash
npm install
npm run dev
```

Open the **Local:** URL printed in your terminal (typically `http://localhost:5173`). Keep the terminal open while browsing.

For deployment:

```bash
npm run build
npm run preview
```

Upload the generated `dist/` contents to a static hosting provider. If deploying below a subpath (for example, GitHub Pages project path), configure Vite `base` and asset URLs accordingly.

## Personal details and profile photo

All editable content is in **`src/data/profile.js`**.

The hero now includes the photo you uploaded from LinkedIn, copied unchanged to **`public/mehboob-qazi-photo.jpg`**. It is not extracted from the PowerPoint (which did not include a photo). The site uses it automatically through:

```js
profilePhoto: '/mehboob-qazi-photo.jpg',
photoIsPlaceholder: false,
```

To replace the photo later, put a new image in `public/` and update the `profilePhoto` field to the matching filename. No other changes are required.

Edit the `linkedIn` and `github` properties once you have full verified URLs. The placeholders remain non-clickable until provided. An employer name for the April 2005 – June 2012 period wasn't given on the PowerPoint, so the timeline explicitly says *Employer not specified*.

## Included content

- Name and presentation headline: Mehboob Qazi · Program Manager / Technical Lead.
- TCS (July 2012 – Present), earlier experience (April 2005 – June 2012).
- Roles and responsibilities: Program Manager, Technical Lead, Module Lead, Development.
- Skills: Azure Databricks, Synapse, PySpark, Python, SQL/PL-SQL, ETL; architecture and program delivery.
- Industry domains, project highlights, certifications, and published email/phone/location.

See `SOURCE_MAPPING.md` for every content decision and remaining missing personal details.

## Design / accessibility

The hero uses a lightweight 3D canvas with your actual uploaded photo; illustrations are decorative. Anchors, skip link, visible keyboard focus states, responsive mobile navigation and reduced-motion support are preserved. Clipboard functionality for the email button falls back to `mailto:` when unavailable. No backend or form submission is included.
