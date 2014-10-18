# Tmux sessionist

Lightweight tmux utilities for switching and creating sessions.

### Features

- `prefix + g` - prompts for session name and switches to it. Performs 'kind-of'
  name completion.<br/>
  Faster than the built-in `prefix + s` prompt for long session lists.
- `prefix + shift + c` - prompt for creating a new session by name.
- `prefix + shift + s` - switches to the last session.<br/>
  The same as built-in `prefix + shift + l` that everyone seems to override with
  some other binding.

### Configuration

By default tmux-sessionist will use the same start-directory as the current
session directory. To configure it to use the current pane directory, add the
following to your tmux configuration:

    set -g @sessionist-use-pane-directory

### Installation with [Tmux Plugin Manager](https://github.com/tmux-plugins/tpm) (recommended)

Add plugin to the list of TPM plugins in `.tmux.conf`:

    set -g @tpm_plugins "              \
      tmux-plugins/tpm                 \
      tmux-plugins/tmux-sessionist     \
    "

Hit `prefix + shift + i` to fetch the plugin and source it. You can now use the plugin.

### Manual Installation

Clone the repo:

    $ git clone https://github.com/tmux-plugins/tmux-sessionist ~/clone/path

Add this line to the bottom of `.tmux.conf`:

    run-shell ~/clone/path/sessionist.tmux

Reload TMUX environment:

    # type this in terminal
    $ tmux source-file ~/.tmux.conf

You can now use the plugin.

### Other plugins

You might also find these useful:

- [pain control](https://github.com/tmux-plugins/tmux-pain-control) - useful standard
  bindings for controlling panes
- [logging](https://github.com/tmux-plugins/tmux-logging) - easy logging and
  screen capturing

### License

[MIT](LICENSE.md)
