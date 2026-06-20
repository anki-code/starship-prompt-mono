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

## Supported modules

starship-prompt-mono includes explicit configurations for these modules, all styled with a consistent monochrome grey:

| Module | Symbol | Purpose |
| ------ | ------ | ------- |
| `[username]` | — | Current user (shown only when root or remote) |
| `[hostname]` | — | Hostname (shown only over SSH) |
| `[directory]` | — | Working directory, truncated to 4 segments |
| `[time]` | — | Current date and time (`%F %T`) |
| `[cmd_duration]` | `⏱` | Command execution time (threshold: 10 s) |
| `[git_branch]` | `git` | Active git branch |
| `[git_status]` | — | Git working tree status |
| `[git_commit]` | — | Current commit hash |
| `[git_state]` | — | Git operation in progress (rebase, merge, etc.) |
| `[nodejs]` | `node` | Node.js version |
| `[rust]` | `rs` | Rust version |
| `[golang]` | `go` | Go version |
| `[python]` | `py` | Python version |
| `[aws]` | `aws` | AWS profile |
| `[gcloud]` | `gcp` | GCP active config |
| `[kubernetes]` | `k8s` | Kubernetes context |
| `[docker]` | `docker` | Docker context |
| `[terraform]` | `tf` | Terraform workspace |
| `[package]` | `package` | Package version for the current project |
| `[jobs]` | `⚙` | Background jobs (shown when ≥ 1) |
| `[shlvl]` | — | Shell nesting level (shown when ≥ 2) |

## Credits

* [xontrib-prompt-bar](https://github.com/anki-code/xontrib-prompt-bar) - The bar prompt for xonsh shell with customizable sections and Starship support.
* [shell-prompt-theme-bar](https://github.com/anki-code/shell-prompt-theme-bar) - The shell prompt appearance conception called Bar.
