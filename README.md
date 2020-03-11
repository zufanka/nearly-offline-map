# A (nearly) offline map

Based on: leaflet.js, mapbox

![map](https://i.imgur.com/XqqHB6V.png)

You should be able to run this example **out of the box** after you put in your own Mapbox API key.

An offline map in **one html file**, without having to run a (localhost) server. Developed to be able to explore sensitive geospatial data without having to upload them anywhere in the cloud.

**All data is in one .html file**, as you can not serve external files to javascript due to CORS rules. You have to turn your icons into a base64 encoded string and paste your geojson in the file it's entirety.

This particular maps is using a mapbox base map. This can be changed to any other base map.

## What you need
* a **geojson** of your data. A handy tool for geojsons: [geojson.io](http://geojson.io)
* a mapbox **API key**
* **icons** base64 encoded

## Icons
Icons have to be put in the .html file in a base64 encoded string format

The format is `data:image/png;base64, <string>` This is how you get the string on linux:

```bash
base64 iconname.png 
```

To copy it as well:
```bash
base64 iconname.png | tr -d "\n" | xclip -selection c
```

## Popups

If you want the popups to have more information, you can add another property to the geojson with some HTML in it.
