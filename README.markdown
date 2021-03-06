webdown
=======

webdown is a static website generator from markdown sources.

Usage
-----

    usage: webdown [options] <source> <destination>

    options:
      -l, --layout <file>         Layout for each generated page
      -q, --quiet                 Do not display any message
      -h, --help                  Display this message
      -V, --version               Print version and exit

The `<source>` is a directory containing the source file hierarchy and
`<destination>` the directory where the HTML will be generated.

To use a layout for each page, you could call *webdown* with the `-l/--layout`
parameter. The templating system is very poor and it only let you replace some
variables:

    {{ TITLE }}   : The title of the current page
    {{ CONTENT }} : The whole generated HTML

The current title is retrieved from the first line of the markdown file. So if
you content starts with:

    Here is the title and H1
    ========================

    Here is the content in a paragraph.

The `{{ TITLE }}` variable will be replaced with `Here is the title and H1`.

For more information checkout the manual page: `man webdown`.

License
-------

Copyright (C) 2012-2013 Juan M Martínez

This program is free software. It comes without any warranty, to the extent
permitted by applicable law. You can redistribute it and/or modify it under
the terms of the Do What The Fuck You Want To Public License, Version 2, as
published by Sam Hocevar. See http://sam.zoy.org/wtfpl/COPYING for more
details.

