# Rivercare Visualisations using JavaScript GEXF Viewer for Gephi #

**Credit**: GEXF viewer forked from raphv/gexf-js under MIT license


## Current Visualisations
http://rivercare.herokuapp.com/index.html#visualisations/blueNoGov.gexf
http://rivercare.herokuapp.com/index.html#visualisations/blueGov.gexf
http://rivercare.herokuapp.com/index.html#visualisations/greenNoGov.gexf
http://rivercare.herokuapp.com/index.html#visualisations/greenGov.gexf
http://rivercare.herokuapp.com/index.html#visualisations/blueGroupsNoGov.gexf
http://rivercare.herokuapp.com/index.html#visualisations/blueGroupsGov.gexf
http://rivercare.herokuapp.com/index.html#visualisations/greenGroupsNoGov.gexf
http://rivercare.herokuapp.com/index.html#visualisations/greenGroupsGov.gexf

### Sample use of visualisations

http://www.arcgis.com/apps/MapJournal/index.html?appid=df8a0221a00d44c8891813cc1ad7c4fc

## How to use ?

### For deploying graphs

1. Export your graph from Gephi as a GEXF file
2. Put it in the visualisations folder of the gexf-js directory and push to github
3. You can view the deployed Gexf files by pointing your browser to index.html#visualisations/Filename.gexf
    ie. http://rivercare.herokuapp.com/index.html#visualisations/blueNoGov.gexf
   Also possible is:
   https://hcollins345.github.io/rivercare/index.html#visualisations/FILENAME.gexf

### For testing

See *Known Issues with GEXF viewer* below.

## Known Issues with GEXF viewer

**The issue below is the source of 90% of support emails I receive, please read carefully**

Gexf-JS won't work on chrome if launched from your local drive (with a file:/// URI scheme).
This is a known security limitation, and there are 2 known workarounds:

1. Use Firefox.
2. Use a server (upload it or use a local server). If you have Python on your computer, the simplest is to launch a SimpleHTTPServer with the Command Line:

    $ cd /path/to/gexf-js
    $ python -m SimpleHTTPServer

There used to a third workaround (The --allow-file-access-from-files flag), but it is no longer available on newest Chrome versions since 2014.

### Compatibility

Gexf-JS uses the canvas element, which might cause compatibility issues with older browsers.

It has been tested with the latest Chrome, Firefox and Internet Explorer versions.

It doesn't work with Internet Explorer 8 or older.
