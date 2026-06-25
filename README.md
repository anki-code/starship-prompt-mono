<p align="center">

  Monochrome style for <a href="https://github.com/starship/starship">starship prompt</a>. Using single color without emoji to stay focused on command line.
</p>

## Concept

* No color juggling or emoji spam.
* Focus on the input line and current directory.
* The command prompt always starts at a fixed position.
* Output is separated by a divider line.
* Time matters.

If you like the idea click ⭐ on the repo and spread the word about it.

## Appearance

<img width="1170" alt="image" src="https://github.com/user-attachments/assets/e3aafd9f-c6ad-4ca0-a902-9e7767201212" />

<p align="center"><sup>(starship-prompt-mono with <a href="https://github.com/xonsh/xonsh/">xonsh shell</a>)</sup></p>

## Install

```xsh
mkdir -p ~/.config
wget https://raw.githubusercontent.com/anki-code/starship-prompt-mono/refs/heads/main/starship.toml
vim starship.toml  # Set your shell character: `@` - xonsh, `$` - bash, `%` - zsh, `~>` - fish.
# Run the shell with starship support.
```

## Notes

### Using with xonsh

Use starship-prompt-mono with xonsh via [xontrib-prompt-starship](https://github.com/anki-code/xontrib-prompt-starship).
To make an accent to the input take a look [LolcatProcessor](https://github.com/xonsh/xonsh/discussions/6050).

### How to add env variable

Add `$env_var` to `format`:

```xsh
# ~/.config/starship.toml
format = """$username$hostname$directory$fill[$all](grey)$time$line_break$env_var$character"""

[env_var.MYPROJECT]
variable = "MYPROJECT"
format = "[$env_value]($style)"
style = "#777777"
default = ""
```

## Credits

* [xontrib-prompt-bar](https://github.com/anki-code/xontrib-prompt-bar) - The bar prompt for xonsh shell with customizable sections and Starship support.
* [shell-prompt-theme-bar](https://github.com/anki-code/shell-prompt-theme-bar) - The shell prompt appearance conception called Bar.
