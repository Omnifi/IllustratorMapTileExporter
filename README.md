# Illustrator Map Tile Exporter

This `JSX` script will export your illustrator file into map tiles ready to be used in leafletjs, mapbox etc.

## How it works

The script loops over each zoom layer and creates a temporary artboard for each map tile, then it exports it as a `PNG24`.

Once saved it then deletes the artboard.

The tiles are name in the following format: `{z}-{x}-{y}.png`

By default the exported tiles are 256px x 256px but that is easily changed in the script.

## Installation

First download the file.

If you don't want to clone the project simply click on `maptilexporter.jsx` and then hit the "raw" button - "right-click" - "save-as" and save it somewhere making sure it has the extension `.jsx`

Then you can either run it in Illustrator (File > Scripts > Other Scrit...)
or copy the file to ~Applications/Illustrator(version)/Presents/(lang)/Scripts - and then restart illustrator.

## Useage

1. Open your file
2. Run the script
3. Select Zoom levels to export
4. Select output folder
5. Click generate!

## Assumptions and Tips

The script makes the following assumptions:

- your file has one artboard
- the artboard is square (although this doesn't matter so much)
- the artboard is big. _Seriously big_. I recommend you have an artboard size of 10000x10000px if you want to zoom to level 5.
- you will select an empty folder to export the files into.

It is not recommended to run this script at lower zoom levels than 5 or 6 as this will generate a huge amount of tiles.

The number of map tiles per zoom level is exponential so this isn't ideal for generating real map tile layers but is better suited to small custom map instances.