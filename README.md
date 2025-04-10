<p align="center">

  Monochrome style for <a href="https://github.com/starship/starship">starship prompt</a>. Using single color without emoji to stay focused on command line.
</p>

## Concept

* No color juggling and spam with emojis.
* Focus on input line and current directory.
* Command always starts at a fixed position.
* Output is separated by a line.
* Time matters.

## Appearance

<img width="1170" alt="image" src="https://github.com/user-attachments/assets/e3aafd9f-c6ad-4ca0-a902-9e7767201212" />

## Install

```xsh
mkdir -p ~/.config
wget https://raw.githubusercontent.com/anki-code/starship-prompt-mono/refs/heads/main/starship.toml
vim starship.toml  # Set your shell character: `@` - xonsh, `$` - bash, `%` - zsh, `~>` - fish.
# Run the shell with starship support.
```

## Credits

* [xontrib-prompt-bar](https://github.com/anki-code/xontrib-prompt-bar) - The bar prompt for xonsh shell with customizable sections and Starship support.
* [shell-prompt-theme-bar](https://github.com/anki-code/shell-prompt-theme-bar) - The shell prompt appearance conception called Bar.
