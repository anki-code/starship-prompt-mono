<p align="center">

  Monochrome style for <a href="https://github.com/starship/starship">starship prompt</a>. Using single color without emoji to stay focused on command line.
</p>

<p align="center">
If you like the cheatsheet click ⭐ on the repo and <a href="https://twitter.com/intent/tweet?text=Monochrome style for Starship prompt.&url=https://github.com/anki-code/starship-prompt-mono" target="_blank">tweet</a> about it.
</p>

## Concept

* No color juggling and spam with emojis.
* Focus on input line and current directory.
* Command always starts at a fixed position.
* Output is separated by a line.
* Time matters.

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

## Credits

* [xontrib-prompt-bar](https://github.com/anki-code/xontrib-prompt-bar) - The bar prompt for xonsh shell with customizable sections and Starship support.
* [shell-prompt-theme-bar](https://github.com/anki-code/shell-prompt-theme-bar) - The shell prompt appearance conception called Bar.
