# Trillion 3D viewer
## How to Remove Trillion Viewer WITHOUT shopify

If you have previously integrated the Trillion Viewer and wish to remove it from your website, follow these steps:

### 1. Uninstall the Package (for npm/yarn users)

If you installed the viewer using npm or yarn, you can remove it using:

```shell
npm uninstall trillion-viewer
```

or

```shell
yarn remove trillion-viewer
```

### 2. Remove the Viewer Initialization Code

Locate and delete the viewer initialization code in your JavaScript files:

```js
import {TrillionViewerApp} from "trillion-viewer";

const elem = document.getElementById('trillion-viewer');
const trillionViewer = new TrillionViewerApp();
trillionViewer.init(elem);
trillionViewer.setServiceActivationKey("YOUR_API_KEY_HERE");
trillionViewer.setJewelryID('demo-ring');
trillionViewer.refresh();
```

### 3. Remove the HTML Container

Delete the `div` element from your HTML file:

```html
<!-- Remove this line -->
<div id="trillion-viewer"></div>
```

### 4. Remove CDN Integration (if applicable)

If you included the viewer via a CDN, remove the corresponding import statement:

```js
import {TrillionViewerApp} from "https://sdk.trillion.jewelry/viewer/latest/trillion-viewer.js";
```

After completing these steps, the Trillion Viewer will be completely removed from your website.




# Trillion AR Widget

This is removing instructions for Trillion SDK.

## How to Remove TrillionWidget, WITHOUT shopify

If you have previously integrated the Trillion AR Widget and wish to remove it from your website, follow these steps:

### 1. Uninstall the Package (for npm/yarn users)

If you installed the widget using npm or yarn, you can remove it using:

```shell
npm uninstall trillion-widget
```

or

```shell
yarn remove trillion-widget
```

### 2. Remove the Widget Initialization Code

Locate and delete the widget initialization code in your JavaScript files:

```js
import {TrillionWidgetApp} from "trillion-widget";

const elem = document.getElementById('trillion-widget');
const trillionWidget = new TrillionWidgetApp();
trillionWidget.init(elem);
trillionWidget.setServiceActivationKey("YOUR_API_KEY_HERE");
trillionWidget.setJewelryID('demo-pendant-ar');
trillionWidget.setJewelryType('necklace');
trillionWidget.refresh();
```

### 3. Remove the HTML Container

Delete the `div` element from your HTML file:

```html
<!-- Remove this line -->
<div id="trillion-widget"></div>
```

### 4. Remove CDN Integration (if applicable)

If you included the widget via a CDN, remove the corresponding import statement:

```js
import {TrillionWidgetApp} from "https://sdk.trillion.jewelry/widget/latest/trillion-widget.js";
```




After completing these steps, the Trillion AR Widget will be completely removed from your website.


