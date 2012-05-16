node-markdown
=============

**node-markdown** is based on [Showdown](http://attacklab.net/showdown/) parser and is meant to parse [Markdown](http://daringfireball.net/projects/markdown/) syntax into HTML code.

Installation
------------

This is a [node-markdown](https://github.com/andris9/node-markdown) fork, so it isn't on npm package manager.

Just clone and install it.

Usage
-----

Include Markdown parser

    var md = require("node-markdown").Markdown;

Parse Markdown syntax into HTML

    var html = md({
        text: "**markdown** string"
    });

Allow only [default set](http://github.com/andris9/node-markdown/blob/master/lib/markdown.js#L38) of HTML tags to be used

    var html = md({
        text: "**markdown** string", 
        strip: true
    });

Allow only specified HTML tags to be used (default set of allowed attributes is used)

    var html = md({
        text: "**markdown** string", 
        strip: true, 
        allowedTags: "p|strong|span"
    });

Allow specified HTML tags and specified attributes

    var html = md({
        text: "**markdown** string", 
        strip: true, 
        allowedTags: "p|strong|span",
        allowedAttributes: {
            "a": "href",        // 'href' for links
            "*": "title|style"  // 'title' and 'style' for all
        }
    });
