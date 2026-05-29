# Carson's Portfolio Website: Start Here

Everything for your site lives in ONE folder, with no subfolders. That's on purpose: GitHub's web uploader can't create folders easily, so keeping it all flat makes uploads painless. The page (`index.html`) looks for every image and PDF right next to it.

---

## FIRST: fix the live site (the images and links)

Right now your site is missing its images and downloads because the page was looking inside `images/` and `files/` folders that didn't upload. I've fixed the page so it now looks for everything in the same folder. Here's how to get the working version live:

1. Go to your repository on GitHub (the `carsonbkeppel.github.io` repo).
2. Click **Add file** then **Upload files**.
3. Open this `website` folder on your computer, select **every file inside it at once** (click one, then Ctrl+A on Windows or Cmd+A on Mac), and drag them all into the upload box. They'll land at the top level, exactly where the page expects them.
4. Scroll down, type a short note like "fix paths," and click **Commit changes**.
5. If GitHub asks about replacing existing files, say yes. If you see leftover files from before with different names, you can delete them, but they won't hurt anything.
6. Wait 1 to 2 minutes, then refresh https://carsonbkeppel.github.io and the images and download links will all work.

---

## Adding your two photos

The page already has two spots waiting for you, with placeholder boxes until you add the pictures:
- A **professional photo** next to your bio. Save it as **`carson-portrait.jpg`**
- An **In-N-Out photo** next to the In-N-Out section. Save it as **`carson-candid.jpg`**

To add them: rename your two photos to those exact names, then upload them to the GitHub repo the same way as above (Add file, Upload files, drag them in, Commit). The page will pick them up automatically. Tip: an upright (taller-than-wide) photo looks best for the portrait, but the page will crop either one to fit neatly.

---

## How to update text yourself

Open `index.html` in a plain-text editor. On Mac, TextEdit works but it nags about HTML; the free **VS Code** (code.visualstudio.com) is easier and opens it as plain code with no warnings. Or just tell me the change and I'll make it.

Text on the site lives between angle-bracket tags:

```html
<h2>Down to earth, creative, and calm when it counts.</h2>
```

Edit only the words between the `>` and the `<`, then save:

```html
<h2>Whatever you want it to say now.</h2>
```

The main editable spots: the `HERO` section (headline and intro), the `ABOUT` section (your bio and the In-N-Out story), the `CASE STUDIES / CAMPAIGNS` section, and the `CONTACT` section (email, phone, links).

## How to swap an image

Give your new image the **exact same filename** as the one you're replacing, then upload it to the repo. The page updates automatically. To use a new filename instead, find the matching `src="..."` line in `index.html` and change the filename there.

Keep images under about 1 MB so the site loads fast. You can shrink them free at squoosh.app.

## How to change a link

Links look like `href="..."`:
- Email: `href="mailto:carsonbkeppel@gmail.com"`
- Phone: `href="tel:+19167495271"`
- LinkedIn: `href="https://www.linkedin.com/in/carsonkeppel"`
- Featured video: search for `mFNKECTe5JU` and replace it with a new YouTube video ID (the part of a YouTube link after `watch?v=`).

## How to replace the resume or portfolio PDF

Upload the new PDF to the repo with the exact same name (`Carson_Keppel_Resume.pdf` or `Carson_Keppel_Portfolio.pdf`) and it just works. Otherwise update the matching `href="..."` line in `index.html`.

---

## Updating the live site later

Any time you change something: go to the repo, click **Add file** then **Upload files**, drag the changed file(s) in, and **Commit changes**. The site refreshes in a minute or two. You can also edit `index.html` right on GitHub by opening the file and clicking the pencil icon.

## Connecting a custom domain later (when you buy one)

1. In your repo: **Settings**, then **Pages**, then **Custom domain**. Type your domain and **Save**.
2. At your domain registrar's DNS settings, add four **A records** for the root (`@`) pointing to GitHub's IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`. Add one **CNAME record** for `www` pointing to `carsonbkeppel.github.io`.
3. Back in **Settings**, then **Pages**, check **Enforce HTTPS** once it's available.

Your `carsonbkeppel.github.io` link keeps working and forwards to the new domain. Nothing breaks.

---

## Quick reference

| I want to change... | Do this |
|---|---|
| Headline / intro | edit the `HERO` section in index.html |
| My bio / In-N-Out story | edit the `ABOUT` section in index.html |
| Stats (3.92, +50%, etc.) | edit the `.fact` blocks in the ABOUT section |
| Featured video | search `mFNKECTe5JU` in index.html |
| A design image | upload a replacement with the same filename |
| My photos | save them as carson-portrait.jpg and carson-candid.jpg, then upload |
| Email / phone / links | edit the `CONTACT` section in index.html |
| Resume / portfolio PDF | upload a replacement with the same filename |
| Colors | edit the `:root` block near the top of index.html |

Questions, or want a change made for you? Just ask.
