# Xi Mun — Personal Portfolio

A small, static personal website. For a reliable local preview (especially the interactive WebGL journey map), serve the folder over HTTP rather than opening `index.html` directly:

```powershell
py -m http.server 8765
```

Then open <http://localhost:8765> in your browser. The journey basemap needs an internet connection and WebGL.

English is the default language. Use **中文** in the top bar to switch the site to Simplified Chinese; the chosen language is remembered in that browser.

## Update the site

- Select **Edit this site** in the top right to click and rewrite the introductory text, About text, and contact note.
- Use **Add a project** to add portfolio items, links, cover images, or video files. Choose **Video** to put a project in the dedicated Videos filter. Select the pencil on a project card to edit or remove it. Project gallery photos can be added as a `photos` array in `content-data.js`.
- The existing profile image is loaded from this browser’s saved media. It no longer has a public upload prompt.
- Add more images or videos as projects with **Add a project**. Use **Edit this site** to update the editable introductory copy and About text.
- Languages have a compact section directly below About. Education and professional references remain as dedicated sections; reference phone links open WhatsApp.
- All phone links open WhatsApp. The header and footer use the supplied calligraphic signature image at `assets/xi-mun-signature.png`.
- Education now has a dedicated section with Taylor’s University, University of Hradec Králové, Taylor’s College and Ave Maria Convent logos and details. The experience timeline also includes the Superprof Chinese tutoring role.
- The Journey map uses OpenFreeMap’s Positron vector basemap through MapLibre GL and Leaflet. It needs an internet connection but no API key. The map displays OpenFreeMap, OpenMapTiles, and OpenStreetMap attribution. OpenFreeMap’s public instance currently states there are no request/view limits and permits commercial use; it is provided as-is without an availability guarantee. If tiles fail, the site switches to its interactive illustrated fallback.
- Use **Export backup** in edit mode to save your site text, projects, and uploaded media to a JSON file. **Import backup** restores that file in this browser.
- The edit experience saves changes in the current browser. To publish those changes, select **Download publish file** in edit mode, then upload the downloaded `site-data.js` beside `index.html`, replacing the existing file. The website reads that file for every visitor. Keep **Export backup** files somewhere safe so uploaded media and edits are recoverable.

## Publish

This is a static site with no build step. Upload this folder to a static web host. After making edits, replace `site-data.js` on the host with the generated publish file. The bilingual resume downloads are `assets/resumes/Ximun_Tang_Resume_EN.pdf` and `assets/resumes/Ximun_Tang_Resume_ZH.pdf`.

The current English and Chinese resume PDFs both show WCGPA 3.86/4.00; the education card uses that current source figure.

## Portfolio content and photos

Default project data, work experience, categorized skills, and language data live in `content-data.js`. Browser edits and published project media are stored separately in `site-data.js`, so downloading a publish file does not erase the structured profile content. Journey destinations and optional photo data are in `journey-data.js`.

Use the section navigation to move through the portfolio. On narrower screens, the header collapses into a menu. The English/中文 control switches the page language. Work experience cards open keyboard-accessible details, and photo galleries/lightboxes appear only when real photos are configured.

See [assets/images-README.md](assets/images-README.md) for the photo folder layout and exact data format. The existing profile portrait is included at `assets/images/profile/xi-mun-portrait.jpg` and in the published media data; the animal-care gallery uses five supplied photos in `assets/images/animals/`. Use **Download publish file** to include later browser-stored edits when publishing. Bilingual resume PDFs are included in `assets/resumes/`.
