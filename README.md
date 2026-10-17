# HustleLink NG — GitHub Pages starter

A mobile-friendly static business directory for discovering Nigerian small businesses and contacting sellers through WhatsApp. It uses plain HTML, CSS, and JavaScript, so no build tools or paid hosting are required.

## Publish using GitHub from an Android phone

1. Sign in at https://github.com or create a free account.
2. Tap **+** → **New repository**.
3. Name the repository `hustlelink-ng`.
4. Set it to **Public** and create the repository.
5. Open the new repository and choose **Add file** → **Create new file**.
6. Name the file `index.html`.
7. Open the `index.html` file from this project in a text editor, copy all its contents, and paste it into GitHub's editor.
8. Commit the file to the `main` branch.
9. Open repository **Settings** → **Pages**.
10. Under **Build and deployment**, select **Deploy from a branch**, choose branch `main` and folder `/ (root)`, then save.
11. Wait for GitHub Pages to publish. The address is usually `https://YOUR-USERNAME.github.io/hustlelink-ng/`.

GitHub may change mobile menus. If a button is hidden, use Chrome's three-dot menu and select **Desktop site**.

## Connect your Google Form

1. Create a Google Form for seller registration at https://forms.google.com.
2. Copy the public responder link.
3. In `index.html`, find:
   `const REGISTRATION_FORM_URL = "PASTE_YOUR_GOOGLE_FORM_URL_HERE";`
4. Replace the placeholder text with your Google Form URL, keeping the URL inside the quotation marks.
5. Commit the change to GitHub. Pages will redeploy automatically.

## Replace example businesses before launch

The site contains clearly labeled sample businesses and sample WhatsApp numbers to demonstrate the layout. They are not real sellers and must be replaced before public launch.

In `index.html`, find `const businesses = [` and replace each example object with a business that has agreed to be listed. Each object uses these fields:

- `name`: business name
- `category`: one of the categories shown in the category buttons
- `location`: town/city text
- `description`: short description
- `price`: price range or starting price
- `emoji`: an emoji for the card
- `phone`: WhatsApp number in international format, digits only (Nigeria: 234 followed by the number without the initial 0)

Example:
```js
{name:"Ada's Cakes",category:"Food & Groceries",location:"Lagos",description:"Cakes for birthdays and events. Pre-order required.",price:"From ₦8,000",emoji:"🎂",phone:"2348012345678"}
```

Do not use a seller's phone number or publish their details without permission. Check that each WhatsApp link opens the intended business.

## Important limitations

- This is a static site. Seller form submissions do not automatically appear on the directory. Review submissions and manually update `businesses` in `index.html`.
- It does not process payments, verify businesses, or guarantee the quality of sellers.
- Use the public site to test demand before paying for custom domains, ads, or a more advanced app.
- GitHub Pages is static hosting; do not put private keys, passwords, or sensitive customer data in this repository.
