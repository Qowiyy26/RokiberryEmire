# RokiberryEmpire

A React + Vite storefront prototype for a handmade jewellery and beads brand.

## Run locally

Install the dependencies and start the Vite development server:

```sh
npm install
npm run dev
```

Create a production bundle with `npm run build`.

## What is included

- Responsive black, gold, navy, and ivory storefront with six image-led collections, product catalogue, testimonials, and editorial brand sections.
- Client-side category filters, saved pieces, search, and price sorting.
- Product cards with colour stories, ratings, wishlist buttons, WhatsApp price enquiries, and add-to-bag actions for priced items.
- Seventeen products from the supplied photos are included locally under `public/goods/` and used in the catalogue and gallery.
- Shopping bag with quantity controls and subtotal calculation.
- Product admin panel for adding, editing, and deleting goods, setting prices, and uploading product photos.
- Custom design request form that opens a prefilled email or WhatsApp message to the business.
- Newsletter interaction and Instagram gallery links.
- Business contact links for WhatsApp, email, and Instagram.
- Hero entrance, scroll reveals, and subtle hover motion with reduced-motion support.
- Supplied brand logo in the header and footer at `public/images/rokiberryempire-logo.png`.
- React components and state are currently kept together in `src/main.jsx`; visual styles live in `src/styles.css`.

## Prototype boundaries

The imported goods have no listed prices until the business sets them in Admin; customers can ask about unpriced items through WhatsApp. Admin asks for a password on first use, stores a PBKDF2 password verifier in this browser, and locks after 15 minutes without activity. Products added or changed in Admin are saved to this browser's local storage. This is a front-end gate only: users with browser or source access can bypass it, and changes do not sync to other devices. Use server-side authentication and a shared database before relying on it to protect real business data. Cart, saved pieces, and form feedback are temporary browser state. Custom design requests open the visitor's email app or WhatsApp with the request prefilled; the visitor must tap Send, and any reference photo must be attached in that app. The form does not send automatically or upload/store files. Checkout, accounts, order tracking, protected product administration, and payment processing need a backend before real customer orders can be accepted. Some editorial photography and fonts load from Unsplash and Google Fonts.
