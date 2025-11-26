# `msm`: a minimal snippet manager for `fish`

Fish-native implementation of [`msm`](https://github.com/mnalli/msm.fish/blob/main/README.md).

## Installation

To install it, you can simply copy [`conf.d/msm.fish`](conf.d/msm.fish) under
your fish installation `conf.d` directory.

```fish
curl -L https://raw.githubusercontent.com/mnalli/msm.fish/refs/heads/main/conf.d/msm.fish > $__fish_config_dir/conf.d/msm.fish
```

### Using [Fisher](https://github.com/jorgebucaran/fisher)

```fish
fisher install mnalli/msm.fish
```

### Using nemo

...

## Configuration

In your `config.fish`, you can add configuration variables and bindings:

```fish
set -g MSM_PREVIEW batcat --decorations=never --color=always -l fish
set -g MSM_STORE $__fish_user_data_dir/snippets.fish
```

Define key bindings for interactive functions:

```fish
bind \ea msm_capture
bind \ez msm_search_interactive
```

## Usage

With `fish`, you can add a newline in the command line with `Alt-Enter` by default.

Examples

```fish
git rebase -i
```

```fish
# interactive rebase
git rebase -i
```

```fish
# multiline snippet example
echo this is a
echo multiline snippet
```

## Error display

If a snippet validation error occurs during capture, the stderr output will
pollute what is displayed on the command line. To clear the screen while
maintaining the current command line content, you can use `CTRL-l` (`clear-screen`).
