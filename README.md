# tmux-tabicon-theme

Theme collection for [tmux-tabicon](https://github.com/mocaffy/tmux-tabicon). These themes provide automatic icon display based on process names.

[日本語](README_ja.md)

## Available Themes

- `normal` - Basic icon set
- Check the `themes` directory for additional themes

## Prerequisites

- [TPM (Tmux Plugin Manager)](https://github.com/tmux-plugins/tpm) installed
- [tmux-tabicon](https://github.com/mocaffy/tmux-tabicon) plugin installed

## Installation

1. Install TPM (if not already installed):
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

2. Clone this theme repository:
```bash
git clone https://github.com/mocaffy/tmux-tabicon-theme.git ~/.config/tmux/tabicon-theme/
```

3. Add the following to your tmux.conf:
```tmux
# Set theme directory
set -g @tmux-tabicon-themes-dir ~/.config/tmux/tabicon-theme/

# Configure plugin
set -g @plugin 'mocaffy/tmux-tabicon'

# Select theme (optional, defaults to 'normal')
set -g @tmux-tabicon-theme 'normal'

# Initialize TPM (should be at the end of tmux.conf)
run '~/.tmux/plugins/tpm/tpm'
```

4. Apply the configuration:
   - If tmux is running: Press prefix + I (capital I) to install plugins
   - Or restart tmux

## Customization

To create your own theme, refer to the existing themes in the `themes` directory.
Each theme can include:

- Process name to icon mappings
- Icon color settings
- Other display format customizations

## License

This project is released under the [MIT License](LICENSE).