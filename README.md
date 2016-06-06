Instapaper.zsh (w/ Qutebrowser userscript support)
---

A simple ZSH script for adding URLs to Instapaper via CLI.

With support for functioning as a [Qutebrowser](https://qutebrowser.org) userscript, create a keyboard short to save the current page to [Instapaper](https://instapaper.com).

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

Symlink `instapaper` bin installed above to `~/.local/share/qutebrowser/userscripts/` and make executable:

    $ ln -sf ~/.bin/instapaper ~/.local/share/qutebrowser/userscripts/instapaper

Test it out by running:

    :spawn --userscript instapaper qute-add

Add a keyboard shortcut by opening `~/.config/qutebrowser/keys.conf`

    vim +437 ~/.config/qutebrowser/keys.conf

and copying this into the [normal] section (line 47-437).

    spawn -u instapaper qute-add
        sI

Now open Qutebrowser and test out the keyboard shortcut. You can change `sI` so whatever keyboard shortcut you like.

- Enjoy!
t1mxg0d

Licence: GPL v3
