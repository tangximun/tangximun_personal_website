# Adding personal photographs

Keep original photos in these folders, then reference them in the matching data file:

- `assets/images/profile/` — profile image assets. The current portrait is included at `xi-mun-portrait.jpg`, with a published-media copy in `site-data.js`; the public page intentionally has no upload prompt.
- `assets/images/journey/` — travel photos. In `journey-data.js`, add a `photos` array to the location, for example `{ src: 'assets/images/journey/prague.jpg', caption: { en: 'Prague', zh: '布拉格' }, date: '', context: '' }`.
- `assets/images/experience/` — work photos. In `content-data.js`, add `{ src: 'assets/images/experience/example.jpg', caption: { en: '...', zh: '...' } }` to the matching experience's `photos` array.
- `assets/images/projects/` — project galleries. Add a `photos` array to the matching project in `content-data.js`, using entries such as `{ src: 'assets/images/projects/campaign.jpg', caption: { en: 'Campaign still', zh: '企划图片' }, context: { en: 'Social campaign', zh: '社交企划' } }`. Use **Edit this site → Add a project** to attach a cover image/video; those uploads are stored in this browser and included in export/publish.
- `assets/images/general/` — other site media.

Use relative paths, keep filenames simple, and copy the image into the project before referencing it. Missing journey/experience images are skipped automatically. The current browser also has a project cover in its local media database; include browser media in the published media file to show it in another browser.
- `assets/images/animals/` — animal-care gallery photos. Add or replace image files here and update the matching `photos` entries in the `skills` data in `content-data.js`; each entry uses `src` and an accessible `alt` description. Captions are optional and the current gallery is unlabeled.
