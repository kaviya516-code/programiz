# AURIXE storefront

A responsive public AURIXE storefront, ready to deploy as a static Netlify site. It includes product discovery, category filtering, sorting, search, product quick views, selectable sizes, and a persistent client-side shopping bag.

## Run locally

Open `index.html` in a browser, or deploy this folder directly to Netlify.

## Deploy to Netlify

1. Log into Netlify and select **Add new site → Deploy manually**.
2. Drag the entire `aurixe` folder into Netlify.
3. Netlify will create a public `*.netlify.app` link. You can rename it in **Site configuration**.

## Important production next step

This deliverable is the public storefront. The catalogue currently uses local sample data in `app.js` and the shopping bag uses browser storage. A real, secure admin dashboard requires a database and authentication service (for example Supabase) configured with server-side/row-level access policies. Do **not** add an admin password to frontend JavaScript or make product write endpoints public.

Recommended production architecture: Netlify frontend + Supabase Auth/Postgres/Storage, with public read policies limited to active products and admin-only write policies enforced in the database.
