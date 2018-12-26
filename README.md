Instapaper.zsh (w/ Qutebrowser userscript support)
---

A simple ZSH script for adding URLs to Instapaper via CLI.

With support for functioning as a [Qutebrowser](https://qutebrowser.org) userscript, create a keyboard short to save the current page to [Instapaper](https://instapaper.com).

See also: [pinboard.zsh](https://github.com/t1mxg0d/pinboard.zsh) for a similar script for adding bookmarks to [Pinboard.in](https://pinboard.in) via ZSH and Qutebrowser.

### Installation

a) Install `zsh` and `curl` if not yet installed

b) Copy `instapaper` script to a local bin directory or run the installer

    $ git clone https://github.com/t1mxg0d/instapaper.zsh
    $ cd instapaper.zsh
    $ chmod +x install
    $ ./install

c) Export these two variables to your enviornment:

    export INSTAPAPER_USER=<username>
    export INSTAPAPER_PASS=<password>

### Usage

To add a URL to instapaper just run:

    $ instapaper add <url>

For example:

    $ instapaper add https://github.com/t1mxg0d/instapaper.zsh/master/README.md
    > Instapaper - Saving: https://github.com/t1mxg0d/instapaper.z....
    > Instapaper - Article saved! {bookmark_id: 732753757}

    Article is now accessible at: https://www.instapaper.com/read/732753757

### Qutebrowser userscript

Symlink `instapaper` bin installed above to `<QUTEBROWSER_DATA_FOLDER>/userscripts/`. You can find out the location to your qutebrowser data folder by checking :version. If the `userscripts` folder doesn't exist, you must create it.

    $ ln -sf <INSTALL_PATH>/instapaper <QUTEBROWSER_DATA_FOLDER>/instapaper

You can find out the `<INSTALL_PATH>` by executing `which instapaper` in the command line.

Test it out by running:

    :spawn --userscript instapaper {url}

Add a keyboard shortcut:
    bind sI spawn --userscript instapaper {url}

Now open Qutebrowser and test out the keyboard shortcut. You can change `sI` so whatever keyboard shortcut you like.

- Enjoy!
t1mxg0d

Licence: GPL v3
