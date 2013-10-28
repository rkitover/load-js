load.js
=======

This is a dynamic javascript and css loader that is used from javascript.

It uses the document.write() technique to immediately load js and css resources.

Examples
--------

    <script type='text/javascript' src='http://rkitover.github.com/load-js/load.js'></script>

    <script type='text/javascript>
        // all your load calls should be in their own <script> block

        loader.load_css('http://foo.com/some.css')

        loader.load_js('/js/some.js')

        // will not be loaded twice!
        loader.load_js('/js/some.js')

        loader.load_jquery() // latest 1.x, only if window['jQuery'] is unset

        loader.load_jquery('1.8.6') // specific version

        loader.load_jquery_ui() // loads jquery first, uses jquery-ui 1.10.3 by default, only if jQuery.ui is unset

        loader.load_jquery_ui('1.9.2') // specific version
    </script>

    <script type='text/javascript'>
        // stuff loaded in preceding <script> block immediately usable from the next!

        $('<div>').append('Yay!').dialog({ modal: true })
    </script>
