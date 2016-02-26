Markdown Extra filter
=============================

Provides Markdown Extra filter integration for Backdrop input formats. The
Markdown Extra syntax is designed to co-exist with HTML, so you can set up
input formats with both HTML and Markdown support. It is also meant to
be as human-readable as possible when left as "source".

There are many different Markdown implementations. Markdown Extra filter
uses [PHP Markdown extra](http://michelf.ca/projects/php-markdown/extra/)
that includes many common and useful extensions to the original Markdown.
This includes tables, footnotes and definition lists.

**Important note about running Markdown with other input filters**

Markdown Extra may conflict with other input filters, depending on the order
in which filters are configured to apply. If using Markdown Extra produces
unexpected markup when configured with other filters, experimenting with
the order of those filters will likely resolve the issue.

The "Limit allowed HTML tags" filter is a special case:

For best security, ensure that it is run after the Markdown Extra filter
and that only markup you would like to allow in via HTML and/or Markdown
Extra is configured to be allowed via the it.

If you on the other hand want to make sure that all converted Markdown
text is perserved, run it after the Markdown Extra filter. Note that
blockquoting with Markdown Extra doesn't work when run after "Limit allowed
HTML tags". It converts the ">".

License
-------

The Backdrop module code is GPL v2 software, but the php-markdown library is distributed under separate copyright held by Michel Fortin.
