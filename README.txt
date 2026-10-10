PANZY STATIC PREVIEW - NETLIFY DEPLOYMENT
========================================

This is a self-contained, free static storefront preview. Its index.html is
at the folder root, and every image the storefront uses is in
panzy-preview-assets. The WordPress theme ZIP stays outside this folder.

OPTION 1: DEPLOY FROM THE EXISTING GITHUB REPOSITORY
----------------------------------------------------
Upload/commit this complete "panzy-netlify-preview" folder, including its
panzy-preview-assets subfolder, to the repository. Do not upload only the
HTML files or the image links will 404.

In Netlify's site build settings, set the Base directory to the path, from the
repository root, of the folder that contains this README and netlify.toml.
For the current repository layout, if the folder is inside "Panzy 3 merge
web", use:

Panzy 3 merge web/panzy-netlify-preview

The included netlify.toml publishes the folder itself. Leave the Build command
empty; no build or dependency install is required. Save the settings and
trigger a new deploy from Netlify's Deploys page.

OPTION 2: DEPLOY THIS FOLDER DIRECTLY
-------------------------------------
For a one-time preview, drag the complete "panzy-netlify-preview" folder into
Netlify's manual deploy/drop area. Alternatively, upload the CONTENTS of this
folder (including panzy-preview-assets, netlify.toml, and index.html) to a new
GitHub repository's root; in that case, leave Netlify's Base directory empty.

CHECK THE DEPLOY
----------------
After deploy, / should show the homepage. Confirm the logo and hero image
directly at:
/panzy-preview-assets/panzy-logo.png
/panzy-preview-assets/hero-living.jpg

If / returns Netlify's 404 page, the deployed output does not contain
index.html at its root: confirm this folder is committed to the selected Git
branch and set Base directory to the folder containing index.html. If the
pages load but image URLs return 404, upload/commit the complete
panzy-preview-assets folder alongside the HTML files.

ALTERNATIVE: UPLOAD THIS FOLDER'S CONTENTS TO A NEW REPOSITORY ROOT
-----------------------------------------------------------------
If you create a separate GitHub repository just for the preview, upload the
contents of this folder (not an additional enclosing folder) to the repository
root. Connect that repository in Netlify and leave Base directory empty.

PAGES
-----
Home:          /
Shop:          /shop.html
Categories:    /categories.html
About:         /about.html
Contact:       /contact.html

LIMITATIONS
-----------
This is a static demonstration. Its sample storefront/cart interactions are
not a live WooCommerce store and do not accept real orders or payments. For a
managed catalogue, checkout, and orders, install panzy-theme.zip on WordPress
with WooCommerce and configure the store there.
