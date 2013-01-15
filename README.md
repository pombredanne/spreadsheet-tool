# ScraperWiki Spreadsheet Tool #

This takes the best bit of Alumina and makes it… bigger!

Install this into a box, or run it locally, to see your SQLite database, full screen, as a spreadsheet.

## How to use ##

This tool expects to call the SQLite API endpoint of a ScraperWiki box. It thus needs the full URL (including publish_token if applicable) of the box containing your data, supplied as a URI-encoded JSON object in the location hash.

The best way of explaining how to create such a hash is probably via some javascript code:

    var base_url = "http://myserver.com/spreadsheet-tool";
    var settings = {
      "dataset_box_url": "http://box.scraperwiki.com/example-data/pUb1i5hT0k3n/"
    }
    var hash = encodeURIComponent(JSON.stringify(settings))
    console.log('URL to visit: ' + base_url + '#' + hash);

Try copying and pasting it into your browser's Javascript console, or a node.js console, to see what the URL (with hash!) should look like.