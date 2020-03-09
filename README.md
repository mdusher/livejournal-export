# Export your LiveJournal blog data

[Livejournal provides a method to export your posts as 
XML](http://www.livejournal.com/export.bml). However 
this has to be done manually for every month of your blog. 
Also [comments are exported separately](http://www.livejournal.com/developer/exporting.bml).
I wrote this tool to make exporting more convenient.

## export.py

This script will do the exporting. Run it after you 
have provided cookies and years as described below.
You will end up with full blog contents in several 
formats. `posts-html` folder will contain basic HTML
of posts and comments. `posts-markdown` will contain
posts in Markdown format with HTML comments and metadata 
necessary to [generate a static blog with Pelican](http://docs.getpelican.com/).
`posts-json` will contain posts with nested comments 
in JSON format should you want to process them further.

## config.py

First of all you will have to log into Livejournal 
and copy values of cookies `ljloggedin` and `ljmastersession` 
to the file auth.py.

Also update the `start` and `end` year values to the years you would like
to archive.

## Requirements
  `Python 3`
* `html2text`
* `markdown`
* `beautifulsoup4`
* `requests`

```
pip install html2text markdown beautifulsoup4 requests
```
