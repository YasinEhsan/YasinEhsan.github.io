# *YasinEhsan.github.io*
[Portfolio site](https://yasinehsan.com/) hosted using Git Pages.

**Version 3.0**
## Video Walkthrough
![mySite](assets/gif/mySite.gif)



**Version 2.0**
## Video Walkthrough
![mySite](assets/readme/v1.gif)
GIF created with [LiceCap](http://www.cockos.com/licecap/).


## Useful Links
- [Set up git pages with custom domain](https://medium.com/@kimcodes/setting-up-a-web-page-with-github-pages-f77d45573ab2)
- [SSL with custom domain](https://www.youtube.com/watch?v=UK5-nO4qK9g) *Using CloudFlare or LetEncrypt for SSL not necessary*
- [Set up Google Analytics](https://www.youtube.com/watch?v=mXcQ7rVn3ro)
- [Google Tag Manager](https://www.youtube.com/watch?v=WACCJaKPeGk)


## Debug Issues
- Trying to access non-SSL certified links from a secure connection will not work. Instead change the URL to without the protocol OR change http links to https.

   Change `http://resources.infolinks.com/js/infolinks_main.js` to `//resources.infolinks.com/js/infolinks_main.js` or `httpS://resources.infolinks.com/js/infolinks_main.js`

- Found warning when I ran Chrome Inspector. Apparently Google Chrome updated Smoothscroll.js. Quick Fix:
   Replace
   ```javascript
    var ischrome = /chrome/.test(navigator.userAgent.toLowerCase());
    if (ischrome) {
        ssc_addEvent("mousedown", ssc_mousedown);
        ssc_addEvent("mousewheel", ssc_wheel);
        ssc_addEvent("load", ssc_init)
    }
   ```
   with
   ```Javascript
   var ischrome = /chrome/.test(navigator.userAgent.toLowerCase());
   if (false) {                          REPLACEMENT
   	ssc_addEvent("mousedown", ssc_mousedown);
   	ssc_addEvent("mousewheel", ssc_wheel);
   	ssc_addEvent("load", ssc_init);
    }
    ```
    **Note:** isChrome is just a variable.

## License

© 2018 Yasin Ehsan

Licensed under the [Apache License](LICENSE).
