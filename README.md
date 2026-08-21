# Fruitty's Travel & Adventures — website

Your WhatsApp (1 876 797 3938) and email (fruittystravelsandadventures@gmail.com)
are already wired into the contact buttons.

## Publish it free on GitHub Pages
1. Go to github.com and create a free account (if you don't have one).
2. Click the **+** in the top right → **New repository**. Name it `fruittys-travel`, keep it Public, click **Create repository**.
3. On the repo page, click **uploading an existing file** and drag in `index.html` and the `trips` folder. Commit the changes.
4. Go to the repo's **Settings** tab → **Pages** (left sidebar).
5. Under **Source**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
6. Your live link appears in a minute or two, e.g. `https://yourusername.github.io/fruittys-travel/`

---

## Setting up the inquiry form (5 minutes, free)
The homepage has a "send the details directly" form that emails you every
time someone fills it out — this is your lead intake / CRM.

1. Go to **formspree.io** and create a free account (up to 50 submissions/month free).
2. Click **New Form**, name it anything (e.g. "Fruitty's Travel Inquiries"), and confirm your email — that's where entries land.
3. Formspree gives you a form endpoint that looks like `https://formspree.io/f/abcd1234`.
4. Open `index.html`, find this line near the bottom:
   ```
   <form class="inquiry-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
   Replace `YOUR_FORM_ID` with the code Formspree gave you.
5. Re-upload `index.html` to your GitHub repo (same steps as before — upload, commit).

From then on, every inquiry lands straight in your inbox with the person's name, contact, destination, dates, and message.

---

## Setting up a client trip page (per client, free)
This is your "TravelJoy-style" client portal — a private page per client showing their itinerary and a button to pay their balance through Fygaro.

1. In the `trips` folder, duplicate `template.html`. Rename the copy something like `janedoe-negril.html`.
2. Open the new file and replace:
   - The title and heading with the client's name and trip
   - Trip dates, group size, destination
   - The day-by-day itinerary
   - Trip total / deposit paid / balance due
   - `FYGARO_LINK_HERE` → the invoice link you generate for that client in Fygaro
3. Delete the instructions comment block near the top before uploading.
4. Upload the finished file into the `trips` folder in your GitHub repo.
5. Send the client their private link directly, e.g.:
   `https://fruittystravelsandadventures.github.io/Fruittys-travels/trips/janedoe-negril.html`

**Note on privacy:** these pages aren't listed anywhere on your main site or
search engines, so only someone with the exact link can see it — but the
link isn't password-protected. Don't put anything on a trip page you
wouldn't want forwarded, and don't reuse the same link for two clients.

An example filled-out page is included at `trips/example-jane-ochorios.html`
so you can see how it looks before making your first real one.

## Making edits later
Come back here and tell me what changed — new package, new client trip, different wording — and I'll update the file for you to re-upload.
