# How to Completely Remove Trillion 3D Viewer from Your Shopify Site

## Overview

This guide provides step-by-step instructions on how to completely remove the Trillion 3D Viewer from your Shopify site. Following these steps will ensure that all Trillion-related elements, scripts, and files are fully removed from your store.

## Steps to Remove Trillion 3D Viewer

### 1. Remove the Preview Image

1. Go to **Shopify admin panel → Products**.
2. Select the product where the 3D Viewer was enabled.
3. Find the preview image that was added (`trillion_viewer_3d_preview.<extension>`).
4. Delete the preview image.

### 2. Delete the Trillion Viewer Snippet

1. Go to **Shopify admin panel → Online Store → Themes → Click three dots → Edit code**.
2. In the `Snippets` folder, locate the file **`trillion_viewer.liquid`**.
3. Delete the `trillion_viewer.liquid` file.

### 3. Remove the Activation Key Reference

1. Open the `trillion_viewer.liquid` file (if not yet deleted) and remove any references to the activation key.
2. If any references remain in `theme.liquid`, remove them.

### 4. Remove the Script from Theme Code

1. Open **`theme.liquid`** from the `Layout` folder.
2. Locate and remove the following lines:
   ```liquid
   {%- if request.page_type == 'product' -%}
     {%- render 'trillion_viewer' -%}
   {%- endif -%}
   ```
3. Save the file.

### 5. Remove SKU Modifications (if applied)

If you modified SKU handling in `trillion_viewer.liquid`, ensure no leftover SKU changes affect your store:

1. If you changed SKU retrieval in `trillion_viewer.liquid`, those changes will no longer apply.
2. Double-check any custom JavaScript files or Shopify settings where SKU modifications may have been applied.

### 6. Verify Removal

- Clear your browser cache and refresh your website.
- Navigate to a product page where the 3D viewer was previously visible to confirm it is no longer displayed.
- Open the browser developer console (`F12` on Windows or `CMD+Option+I` on macOS) and check the console/network tab to ensure no Trillion-related scripts are being loaded.
