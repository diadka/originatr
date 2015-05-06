#fuckr: Grindr™ for Mac and Windows

fuckr is a Grindr™ client for desktop built with Node Webkit, node-xmpp and Angular.

##Run
First, install node-webkit (eg. `npm install -g nodewebkit`). Then

    cd fuckr/
    npm install
    nw .

##Package
Preferably, rum `npm dedupe` in fuckr subdir to save up ~50MB. Then, change platform in `package.js` and:

    npm install
    node package.js

And for mac users: 

    npm install -g appdmg
    appdmg dmg.json

Due to C++ dependencies of node module dependencies, you shouldn't package for any other platform.

##Reverse engineering grindr
If there's anything you wanna know about Grindr that's not in the code, you can easily analyse the HTTP part with [mitmproxy](http://mitmproxy.org/)'s [regular proxy](https://mitmproxy.org/doc/modes.html) mode and the XMPP part with... just Wireshark (and [ettercap](http://www.kioptrix.com/blog/ettercap-command-line-basics/) to save time) since grindr XMPP client doesn't bother encrypting!


##Credits
Package structure and landing page originally copied from [Kyle Power's](https://twitter.com/mfkp/)'s [Tinder++](https://github.com/mfkp/tinderplusplus).
