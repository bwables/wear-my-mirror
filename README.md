# Wear My Mirror

Student art you wear on your own face. A phone gallery for **ART 104A · Digital Media I · Davis & Elkins College**, Fall 2026.

Visitors scan a QR code, turn on their camera and swipe through student pieces. Face tracking runs on the visitor's phone. Nothing is recorded or uploaded unless the visitor takes a photo and saves or shares it.

---

## Publish it (once, about 10 minutes, no coding)

1. Sign in at **github.com**. Click **+** (top right) > **New repository**.
2. Name it `wear-my-mirror`, choose **Public**, and click **Create repository**.
3. On the new page, click **uploading an existing file**. Drag in everything from this folder: `index.html`, `poster.html`, `clips.json`, `qrcode.js`, `README.md` and the `clips` folder. Click **Commit changes**.
4. Go to **Settings > Pages**. Under **Build and deployment**, set Source to **Deploy from a branch**, Branch to **main** and folder **/ (root)**. Click **Save**.
5. Wait about a minute. Your gallery is at
   `https://YOUR-USERNAME.github.io/wear-my-mirror/`
6. Open that address on your phone and try the demo.

## Print the poster

Open `https://YOUR-USERNAME.github.io/wear-my-mirror/poster.html` in Chrome. The QR code already points to your gallery. Click **Print**, then under **More settings** turn on **Background graphics** and set **Margins** to **None**. Print on US Letter.

---

## Add a student piece

Only add work from students who returned the signed release form.

1. **Make a phone-size copy** in Adobe Media Encoder: Format **H.264**, size **720 × 720**, 30 fps, Bitrate **VBR, 1 pass, target 2 Mbps**. Keep the name `Lastname_Mirror.mp4`. (PNG stills on black also work.)
2. **Upload it**: on GitHub, open the `clips` folder > **Add file > Upload files** > drag in the MP4 > **Commit changes**.
3. **Add the credit**: open `clips.json`, click the pencil icon, and add an entry inside `"pieces": [ ]`. Put a comma between entries:

```json
{
  "pieces": [
    {
      "file": "clips/Smith_Mirror.mp4",
      "credit": "Jordan Smith",
      "sentence": "Look into my mirror and you'll wear my grandmother's tomato vines, because her garden is where I felt safe."
    },
    {
      "file": "clips/Lee_Mirror.mp4",
      "credit": "Sam L.",
      "sentence": "Look into my mirror and you'll wear static, because that's what anxiety sounds like."
    }
  ]
}
```

4. Click **Commit changes**. The gallery updates in about a minute. On your phone, reload the page.

The `_example` block at the top of `clips.json` is ignored; leave it or delete it.

**If the gallery shows only the demo after an edit**, `clips.json` has a typo, usually a missing comma or quote. Paste it into jsonlint.com to find the line.

**To remove a piece**, delete its entry from `clips.json` and its file from `clips`.

**To link to one piece**, add its number to the address: `.../wear-my-mirror/#3`.

---


## A class-only set

Pieces from students who said no to the public gallery can still be used in class. List them in `class.json` (same format as `clips.json`) and share this link with the class only:

`https://YOUR-USERNAME.github.io/wear-my-mirror/?set=class`

It isn't listed anywhere public, but anyone with the link can open it, so treat it as unlisted, not private. To use the class set for everything, copy the public entries into `class.json` too.

## How it fits the class template

Same contract as the Mirror Player: a 1080 × 1080 square on black, eyes at (480, 540) and (600, 540), the face oval kept mostly clear. Black disappears; only light shows. Anything the class made for the mirror works here unchanged.

## Credits

Face tracking: Google MediaPipe Face Detector (Apache 2.0), loaded from jsDelivr. QR codes: qrcode-generator by Kazuhiko Arase (MIT), included as `qrcode.js`. Fonts: Instrument Serif and Instrument Sans (Google Fonts, SIL Open Font License).
