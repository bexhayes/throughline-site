# Throughline website: how to edit and publish

The whole site is one page, `index.html`, plus a thank-you page, `thanks.html`, and a folder of photos, `images/`.

## Editing the text

All the words live in `index.html`, in sections marked like this:

```
<!-- ===================== COPY: HERO ===================== -->
```

Only change text **between** the tags, for example the words inside `<p class="body">…</p>`. Leave everything in angle brackets alone.

Placeholders in square brackets, like `[X]` or `[15]`, still need real details.

### Using an AI chatbot to edit

Paste this at the start of your message, then paste `index.html` and say what you want changed:

> You are editing a website file. Rules: change only the visible text I ask about, inside the sections marked COPY. Do not change any HTML tags, class names, the STYLES section, the form, the logo, or image file names. Do not add or remove sections. Return the complete file.

Before publishing, check the preview link Netlify gives you. If anything looks broken, roll back (see below).

## Changing photos

Put photos in the `images/` folder with exactly these names. JPG, roughly 2000px on the long edge, compressed (squoosh.app is free) to under 400KB each.

| File name | Where it shows | Shape |
|---|---|---|
| hero-1-main.jpg | Hero, big image on the left | Landscape |
| hero-2-side.jpg | Hero, right, top | Any (cropped to fit) |
| hero-3-square.jpg | Hero, right, bottom | Any (cropped to fit) |
| case-peak-design.jpg | Track record section | Portrait |
| about-luke.jpg | About section | Portrait |
| share.jpg | Preview image when the link is shared | 1200 x 630 |

Brand photos (Peak Design, Rumpl and so on) need the brand's permission before going live.

## Changing the accent colour

In `index.html`, find `--accent:#8FA060;` near the top and change the colour code. The logo arrow is set separately: search for `#8FA060` and change those too.

## Publishing (one-time setup)

1. **GitHub:** create a free account, make a new repository called `throughline-site`, and upload these files.
2. **Netlify:** sign up with your GitHub account, choose "Add new site", "Import an existing project", and pick `throughline-site`. No build settings are needed. Click Deploy.
3. **Domain:** in Netlify, go to Domain management, add `throughline-advisory.com`, and follow the steps to point the domain at Netlify (you change the DNS settings where you bought the domain).
4. **Contact form:** after the first deploy, go to Netlify, Forms, and turn on email notifications to Luke's inbox. Then send a test message from the live site.

After that, every change saved in GitHub goes live automatically within a minute.

## Rolling back

In Netlify, open Deploys, click an earlier deploy and choose "Publish deploy". The site goes back to that version straight away.
