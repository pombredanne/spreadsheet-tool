# ScraperWiki Spreadsheet Tool #

This takes the best bit of Alumina and makes it… bigger!

Install this into your box to see your database, full screen, as a spreadsheet.

## How to install ##

This library is intended to be cloned into the `http/` directory of a ScraperWiki box. Like so:

    $ cd /my-data-project/http/
    $ git clone git://github.com/scraperwiki/spreadsheet-tool.git

Make sure the `sqliteEndpoint` variable at the top of the `/js/spreadsheet-tool.js` file is pointing the database you want to access:

    // to access your box's database:
    sqliteEndpoint = "../../sqlite";

    // to access another box's database:
    sqliteEndpoint = "https://box.scraperwiki.com/<owner>/<box>/sqlite";

You can then visit the spreadsheet by visiting:

    https://box.scraperwiki.com/my-name/my-data-project/http/spreadsheet-tool/

Or, if your box has a `publish_token` set:

    https://box.scraperwiki.com/my-name/my-data-project/<publish_token>/http/spreadsheet-tool/