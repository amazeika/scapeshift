Scapeshift
==========

Scapeshift is a webscraper rubygem designed for the Magic: The Gathering Oracle "Gatherer" card index.
Since Wizards doesn't want to make an API for this system for various reasons, I've gone ahead and made
a pseudo-API here.

Usage
-----

Usage is as simple as can be:

    # Grab the complete list of expansion sets
    @sets = Scapeshift::Crawler.crawl :meta, :type => :sets

    # Grab the card set for an expansion
    @alara_cards = Scapeshift::Crawler.crawl :cards, :set => 'Shards of Alara'

    # Grab a single named card
    @card = Scapeshift::Crawler.crawl :single, :name => 'Counterspell'

Documentation
-------------

This gem uses Yardoc syntax for documentation. You can generate these docs
with `rake yard`. Point any webserver at the `docs/` directory to browse.

Simple, with Thin:

    $ cd /path/to/scapeshift
    $ cd docs/
    $ thin -A file -d start

Copyright
---------

Copyright (c) 2010 Josh Lindsey. See LICENSE for details.