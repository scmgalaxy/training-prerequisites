### Install Sublime Text

Using APT, it's time to install [Sublime Text](http://www.sublimetext.com/), a sophisticated text editor for code, markup and prose.

To get started, run the following command.

```
sudo apt-get install -y sublime-text-installer
```

Once installed, use the Dash to launch Sublime Text.

![](../assets/ubuntu-sublime-01.png)

Next, navigate to the `Preferences > Settings - User` menu item.

Ensure the file contains the following preferences.

```
{
  "font_size": 18.0,
  "ensure_newline_at_eof_on_save": true,
  "rulers": [80],
  "tab_size": 2,
  "translate_tabs_to_spaces": true,
  "trim_trailing_white_space_on_save": true,
  "update_check": false
}
```

**WARNING:** Punctuation errors with either curly-brackets, double-quotes, colons, square-brackets, or commas will be highlighted in red. If one of these symbols is missing, Sublime Text will highlight the next closest symbol. Analyze the above example preferences carefully. :eyes:

Remember to save the file and you'll see something like this.

![](../assets/ubuntu-sublime-02.png)

When you're done, close the file.


### subl

You'll find it insanely useful to open files and directories into Sublime Text from the Terminal.

To verify Sublime Text is wired up correctly, run the following command:

```
subl ~/.config/fish/config.fish
```

And Fish's startup file will open in Sublime Text like this.

![](../assets/ubuntu-sublime-03.png)


### Edit config.fish

Many command line tools, like Git, use the `EDITOR` environment variable to open your preferred text editor.

While Fish's startup file is handy, add the following settings.

```
# Sublime Text
set -gx EDITOR 'subl -w'
```

Save the file and you'll see something like this.

![](../assets/ubuntu-sublime-04.png)

Now, relaunch the Terminal and verify these settings with the following command.

```
echo $EDITOR
```

And you'll see something like this.

![](../assets/ubuntu-sublime-05.png)

### [⇐ Previous](fish.md) | [Next ⇒](git.md)
