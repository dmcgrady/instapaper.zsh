Simple Instapaper CLI
---

A simple ZSH script for adding URLs to Instapaper.

With support for functioning as a Qutebrowser userscript.

### Installation

a) Copy script to a local bin directory, for ex:

    $ git clone https://github.com/t1mxg0d/instapaper.zsh
    $ cp instapaper.zsh/instapaper ~/.bin/instapaper
    $ chmod +x ~/.bin/instapaper

b) Install HTTPie, a required depencency. Install using your usual package
manager or using `pip`:

    $ pip install httpie

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

Copy or symlink `instapaper` to `~/.local/share/qutebrowser/userscripts/` and make executable:

    $ cp instapaper ~/.local/share/qutebrowser/userscripts/
    $ chmod +x ~/.local/share/qutebrowser/userscripts/instapaper

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

Licence: G
