# Custom Basemap using Mapbox

Mapbox is a highly customizable GIS system that is used by <a href="https://www.mapbox.com/showcase">many companies</a> for customizable mapping and integrated GIS services.

Purpose: Create a customized basemap in Mapbox and import into ArcGIS Online.

## Step 1: Choose a pallet.

I chose a <a href="https://coolors.co/palettes/trending">trending color pallet</a> to use to create the basemap.

<img src="/mapbox/ColorPallet_Mapbox.png" />

## Step 2: Use MapBox Styles to customize basemap.

Navigating to <a href="https://studio.mapbox.com/styles">Mapbox Styles</a>, I chose to customize the Monochrome/Sky basemap to customize.

## Step 3: Customize basemap colors.

Following the tutorial, I chose to customize the basemap using the color pallet by compenents, colors, and layers.

## Step 4: Review finished product and publish.

I saved the customized style and named it "Rudy Greyscale" based on the red-grey-black pallet. Then, I made the map style public.

<img src="/mapbox/Image_RudyGrayscaleUSA.PNG" />

Colors shown are customized to display differently based on how the zoom scale.

<img src="/mapbox/Image_RudyGrayscaleSFO.PNG"/>

## Step 5: Connect basemap Style to ArcGIS Online Map.

Open ArcGIS Online Maps, create a new map, and add style data as a WMTS server. Customize the WMTS Endpoint information using the public style key, user name, and access key.

<img src="/mapbox/Image_RudyGrayscaleEsri.PNG" />

**[This map is interactive! Find it here.](mapbox/interactive_rudygrayscale.html)**


### Resource

This worflow was completed using the Mapbox Tutorial on <a href="https://docs.mapbox.com/help/tutorials/create-a-custom-style/">How to create a custom style</a> and <a href="https://docs.mapbox.com/help/tutorials/mapbox-arcgis-qgis/">Add Mapbox maps as layers in ArcGIS and QGIS with WMTS</a>.
