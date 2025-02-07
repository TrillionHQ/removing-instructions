# How to Completely Remove Trillion AR from Your Shopify Site

## Overview

This guide provides step-by-step instructions on how to completely remove the Trillion AR Try-On widget from your Shopify site. Following these steps will ensure that all Trillion-related buttons, scripts, and files are fully removed from your store.

## Steps to Remove Trillion AR

### 1. Remove Added Files

#### a. Delete the AR Page Template
1. Go to Shopify admin panel: **Online Store → Themes → Click three dots → Edit code**.
2. In the `Templates` folder, locate the file **`trillion_tryon.liquid`**.
3. Delete the `trillion_tryon.liquid` file.

#### b. Delete the Trillion Button Snippet (if used)
1. In the `Snippets` folder, locate the file **`trillion_tryon_button.liquid`**.
2. Delete the `trillion_tryon_button.liquid` file.

#### c. Delete the Custom Script File (if used)
1. In the `Assets` folder, find **`script-for-custom-button.js`**.
2. Delete the `script-for-custom-button.js` file.

### 2. Remove the AR Button from the Theme
1. Identify where the Trillion button was added. It was likely inserted in a product-related file such as:
   - `product.liquid`
   - `product-form.liquid`
   - `product__form.liquid`
2. Open the file and search for the following code:
   ```liquid
   {% render 'trillion_tryon_button' %}
   ```
3. Delete this line of code and save the file.

### 3. Remove the Trillion AR Script References (if applied)
1. Open the `Layout` folder and locate **`theme.liquid`**.
2. Find and remove any `<script>` tags referencing Trillion, such as:
   ```html
   <script src="{{ 'script-for-custom-button.js' | asset_url }}" defer type="module"></script>
   ```
3. Save the file.

### 4. Remove SKU Modifications (if applied)
If you modified SKU handling in either the `trillion_tryon_button.liquid` file or the `script-for-custom-button.js` file, these modifications should no longer affect your store since the files have been deleted. However, double-check any custom JavaScript files or Shopify settings where these modifications may have been applied.

### 5. Delete the Trillion AR Page (if created)
1. Go to Shopify admin panel: **Online Store → Pages**.
2. Locate the page titled **"Trillion Tryon"**.
3. Click on the page and press **Delete page**.

### 6. Verify Removal
- Clear your browser cache and refresh your website.
- Navigate to a product page where the AR button was previously located to confirm it is no longer visible.
- Open the browser developer console (`F12` on Windows or `CMD+Option+I` on macOS) and check the console/network tab to ensure no Trillion-related scripts are being loaded.

## Conclusion
Following these steps ensures the complete removal of Trillion AR from your Shopify store, including all buttons, scripts, and associated files. If you experience any issues, ensure that you have deleted all relevant files and references in your theme code.
