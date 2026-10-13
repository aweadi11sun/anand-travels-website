# Anand Travels website — first version

A responsive static bilingual (English/Hindi) website for a group bus rental company. Built with plain HTML, CSS, and JavaScript so it can be hosted on Cloudflare Pages without a build step.

## Preview locally

Open `index.html` in a browser. For a more realistic local server preview, run from this directory:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Before publishing — important customizations

1. **WhatsApp number:** Configured as `917030835151` (Anand Travels).
2. **Video:** Put the company video at `media/anand-travels.mp4`. The video section will show the player automatically when the file is available. Use a compressed MP4 (H.264/AAC) and keep it reasonably small for visitors on mobile data. Alternatively, ask me to change it to a YouTube/Vimeo embed.
3. **Business details:** Confirm service area, actual fleet types, seating capacity, amenities, contact number, and any business address before launch. The current copy avoids making specific claims about fleet capacity or amenities.
4. **Images:** The current design uses remote Unsplash images for a visual first draft. Replace these with real photos of Anand Travels' buses and trips for a more authentic business site. Make sure you have permission to use all photos and any identifiable passenger footage.
5. **Domain:** Connect `anandtravelsnagar.in` after you register it and configure Cloudflare.

## Deploy to Cloudflare Pages

1. Create a GitHub repository and upload the contents of this folder (the `index.html`, `README.md`, and `media` folder).
2. In Cloudflare Dashboard, go to **Workers & Pages → Create → Pages → Connect to Git** (the exact menu wording may vary).
3. Authorize GitHub and select the repository.
4. For a plain static site, leave the build command blank and set the output directory to `/` or the repository root as prompted.
5. Deploy. Cloudflare will provide a `*.pages.dev` address.
6. In the Pages project, add your custom domain after the domain is registered. Follow the exact DNS/nameserver instructions Cloudflare shows for your setup; don't change nameservers based on guesswork.

## Language toggle

The header includes a Hindi/English toggle. It translates visible page copy, navigation, reviews, quote calculator labels/results, enquiry form labels and placeholders, and WhatsApp enquiry labels. The selected language is remembered in the browser.

## Notes

- This is a static website. The enquiry form builds a WhatsApp message in the visitor's browser; it does not save submissions to a database.
- Google Fonts and Unsplash images require internet access. Replace remote assets with local copies if you want a fully self-contained deployment.
