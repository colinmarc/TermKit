# TermKit

![TermKit Icon](https://github.com/unconed/TermKit/raw/master/Illustrator/TermKit%20Icon%20128.png)

### Goal: next gen terminal / command application

Built out of WebKit and Node.js.

Runs as a desktop app on Mac, Windows and Linux, and can be hacked into any WebKit browser (Chrome, Safari).

[Follow TermKit on Twitter](https://twitter.com/TermKit) for the latest news and updates.

For the background and architecture, please read and comment on:
http://acko.net/blog/on-termkit

![TermKit 0.3 alpha](https://github.com/unconed/TermKit/raw/master/Mockups/Shot-0.3.png)
![TermKit 0.3 alpha](https://github.com/unconed/TermKit/raw/master/Mockups/Shot-Self-Commit.png)
![TermKit 0.3 alpha](https://github.com/unconed/TermKit/raw/master/Mockups/Shot-Highlight.png)

### Warning: Alpha version, still under development. Nothing works yet.

## Some cool features

* Smart token-based input with inline autocomplete and automatic escaping
* Rich output for common tasks and formats, using MIME types + sniffing
* Asynchronous views for background / parallel tasks
* Full separation between front/back-end

## TermKit is not a...
* ...Web application. It runs as a regular desktop app.
* ...Scripting language like PowerShell or bash. It focuses on executing commands only.
* ...Full terminal emulator. It does not aim to e.g. host 'vim'.
* ...Reimplementation of the Unix toolchain. It replaces and/or enhances built-in commands and wraps external tools.

(but you could make it do most of those things with plug-ins)

## How to use:

Detailed instructions are available from these sources:

* [Mac OS X (OS X Daily)](http://osxdaily.com/2011/05/19/termkit-terminal-reimagined-how-to-install/)
* [Windows (Redpoint blog)](http://blog.redpointsoftware.com.au/termkit/)
* [Linux, Python GTK](https://github.com/unconed/TermKit/tree/master/Linux)
* [Linux, Chrome only (Easytech blog)](http://blog.easytech.com.ar/2011/05/21/playing-with-termkit-with-chrome/) 

Unfortunately, TermKit currently requires some assembly.

1. Install the Mac development tools (Xcode and friends).
2. [Install node.js](https://github.com/joyent/node/wiki/Installation).
3. If not covered in #2, install npm: `curl http://npmjs.org/install.sh | sh`
4. Clone the TermKit repository: `git clone https://github.com/unconed/TermKit.git --recursive`
5. Users of older git versions will need to type: `git submodule update --init`
6. Switch into the NodeKit daemon directory: `cd TermKit/Node`
7. (First time only.) Let npm install modules that NodeKit depends on: `npm install .`
8. Run the NodeKit daemon: `node nodekit.js`

Mac:
* Unzip and run the Mac app in Build/TermKit.zip

Linux:
* See Linux/Readme.txt

*Tip:* Press ⌥⌘C to access the WebKit console.

## API

Preliminary instructions on how to write TermKit native commands can be found here:
https://github.com/unconed/TermKit/blob/master/Node-API.md

## Credits

TermKit by [Steven Wittens](http://acko.net) ([@unconed](https://twitter.com/unconed)).

Windows port by James Rhodes ([@hachque](https://twitter.com/hachque)).

Linux Python/GTK wrapper by [Lucas S. Magalhães](https://github.com/lucassmagal).

Includes:

* “NSImage+QuickLook” by Matt Gemmell (http://mattgemmell.com/source).
* SyntaxHighlighter by Alex Gorbatchev (http://alexgorbatchev.com/SyntaxHighlighter/)
* jQuery and jQuery UI