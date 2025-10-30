**IPvFooBarBaz** is a Chrome/Firefox extension that adds an icon to indicate whether the current page was fetched using IPv4 or IPv6. When you click the icon, a pop-up appears, listing the IP address for each domain that served the page elements, as well as their hostname and ASN (if available).

Everything is captured privately using the webRequest API, however Google DNS is used to fetch hostnames, as well as Cymru's IP to ASN services.

This is a fork of the original IPvFoo, and uses code from the IPvFooBar (which itself is a fork of IPvFoo).

## Screenshots
![Screenshot](/misc/screenshot_webstore_1_640x400.png?raw=true)

![Screenshot](/misc/screenshot_options.png?raw=true)

## Add to Chrome
https://chromewebstore.google.com/detail/ipvfoobarbaz/jiaodmfhmjdhefmljkipedcbpkplpfcn

## Add to Firefox
https://addons.mozilla.org/firefox/addon/ipvfoobarbaz

To use IPvFoo with Firefox's default search engine, uncheck **Settings > Search > Show search terms in the address bar on results pages**

## Add to Edge
Coming Soon
*(You can also run the [Chrome version](https://chromewebstore.google.com/detail/ipvfoobarbaz/jiaodmfhmjdhefmljkipedcbpkplpfcn) on Edge, as they are identical.)*

## Safari?

IPvFoo cannot be [ported to Safari](https://github.com/pmarks-net/ipvfoo/issues/39) because the `webRequest` API does not report IP addresses.  In theory, a Safari extension could do its own DNS lookups over HTTPS, but such behavior is beyond the scope of IPvFoo.

## Running IPvFoo unpacked from git

IPvFoo shares a common codebase for Chrome and Firefox, but `manifest.json` is browser specific.

Firefox shows this error when running the Chrome version:

> There was an error during the temporary add-on installation.  
> background.service_worker is currently disabled. Add background.scripts.

Chrome shows this error when running the Firefox version:

> 'background.scripts' requires manifest version of 2 or lower.  
> 'page_action' requires manifest version of 2 or lower.

The `use_*_manifest.sh.bat` scripts in the [manifest](src/manifest/) directory may be used to switch between versions.

<br><br><br>
Donate: https://liberapay.com/pmarks
