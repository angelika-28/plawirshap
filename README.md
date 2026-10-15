# Pailful Flowers

A flower shop website made with plain HTML and CSS. There is no JavaScript, nothing to install and no build step.

## Files

| File | What it does |
| --- | --- |
| `index.html` | The whole page: header, shop, delivery, order form, about, visit |
| `styles.css` | All styling |
| `favicon.svg` | The small flower icon in the browser tab |
| `vercel.json` | Vercel settings (clean URLs and basic security headers) |

## How it works without JavaScript

- **Filtering and sorting** use hidden radio buttons. The CSS shows or reorders the products depending on which one is selected.
- **Product details** open as pop-ups when you select a product. Each pop-up is a section of the page that CSS shows when it is the link target. Use the close button, or select outside the pop-up, to return to the shop.
- **Ordering** uses email links. Selecting **Order by email** opens the customer's own email app with the order message already written. The order form near the bottom does the same for orders with several items.
- **The flowers** are SVG drawings inside `index.html`, so there are no image files to host.

There is no shopping cart or online payment, because those need a server or JavaScript. You reply to each email to confirm the total and take payment.

## Preview on your computer

Open `index.html` in a browser. The fonts load from Google Fonts, so you need an internet connection to see them.

## Upload to GitHub

**Without the command line**

1. Sign in at github.com and select **New repository**. Name it `flower-shop`, then select **Create repository**.
2. On the new repository page, select **uploading an existing file**.
3. Drag in everything from this folder (the files, not the folder itself) and select **Commit changes**.

**With the command line**

```bash
cd pailful-html-css
git init
git add .
git commit -m "Add flower shop site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/flower-shop.git
git push -u origin main
```

## Import into Vercel

1. Sign in at vercel.com with your GitHub account.
2. Select **Add New**, then **Project**, and pick the `flower-shop` repository.
3. Leave the settings as they are: Framework Preset **Other**, no build command, no output directory.
4. Select **Deploy**. Your site is live in under a minute at a `.vercel.app` address.

After that, every push to `main` redeploys the site automatically. To use your own domain, open the project in Vercel and go to **Settings**, then **Domains**.

## Make it yours

Open `index.html` in any text editor and use find and replace.

- **Shop email:** replace `hello@example.com` everywhere it appears.
- **Shop address, phone number and hours:** edit the "Visit the shop" section near the bottom.
- **Delivery fee and free-delivery amount:** edit the "Delivery you can count on" section.
- **Text:** the About and Delivery wording is sample text. Replace it with your own details and claims. The address, phone number, hours and email are placeholders.
- **A product's name, price or description:** each product appears in three places: its tile in the grid, its pop-up near the end of the file, and its order link. Search for the product name to find all three.
- **Colors and fonts:** the palette is defined at the top of `styles.css`.

Prices are written into the page text, so if you want a long catalog that is easy to update, a small JavaScript or static-site setup would suit it better. You can ask for that later.
