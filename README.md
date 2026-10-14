# Signature Builder

Design an email signature, fill in your details, then copy it into Gmail, Outlook, Apple Mail or Thunderbird. It is one HTML file that runs in your browser: nothing is uploaded, nothing is stored, and the page makes no requests to anywhere.

## Using it

Download `index.html` and open it in any current browser. There is nothing to install.

1. **Design.** Choose a layout (side by side, stacked, compact or boxed), an accent and text colour, fonts, size, labels, a divider, and a badge showing your initials, or a logo or photo uploaded from your computer. Tick what the signature should include and set the order of the contact lines. A sample person fills the preview so you can judge the design before typing anything.
2. **Your details.** Fill in the boxes for what you ticked. Blank boxes are left out. Then:
   - **Copy signature** and paste into your mail app's signature settings (instructions for each app are on the page)
   - **Copy plain text** for iPhone and iPad Mail, which keep almost no formatting
   - **Copy HTML code** for anything that takes raw HTML
   - **Download .html** to keep a copy, or to point Thunderbird at
   - **Download .txt** for a plain version

## Picking up later

The page keeps nothing once the tab closes. **Save settings** on the Design tab downloads a small `.json` file with your design and details. **Open settings…** loads it back. The same file is an easy way to give a team one consistent design: send it round and each person opens it and changes the details.

## How the signature is built

Mail apps render HTML very differently, so the output sticks to what they all handle:

- Tables and inline styles only. No stylesheets, classes or web fonts.
- Fonts are limited to ones every mail app already has (Arial, Helvetica, Verdana, Tahoma, Trebuchet MS, Georgia, Times New Roman, Courier New).
- The initials badge is a coloured table cell rather than an image, so it shows even where images are blocked.
- A logo or photo can be uploaded from your computer or taken from a web address. An upload is resized to twice its display width (sharp on high-resolution screens), compressed, has any rounded or circle shape cut into the image itself so it looks the same in Outlook, and is then built into the signature. Nothing leaves your browser.
- Apple Mail and Outlook keep an uploaded image when you paste. Gmail removes pasted images, so for Gmail paste the signature and then add the image with the image button in Gmail's signature editor, using **Download resized image**. An image at a web address works everywhere, though some recipients only see it after clicking "show images", so nothing important should live only in the image.
- Rounded corners and circles show as squares in classic Outlook for Windows, which renders email with Word.

Send yourself a test email before relying on it.

## Privacy

Everything happens in the page. There are no analytics, cookies, fonts or scripts loaded from elsewhere, and what you type is never sent anywhere. The page works under a `default-src 'none'` Content Security Policy.

## Licence

MIT No Attribution. Use it, change it, ship it, no credit needed.
