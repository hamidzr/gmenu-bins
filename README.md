# gmenu / GoMenu

`gmenu` (GoMenu) is a dynamic GUI menu application compatible with and inspired by `dmenu`. Designed with a focus on flexibility and ease of use, it brings a simple, efficient interface for quick command execution and option selection.

[Check out the latest release](https://github.com/hamidzr/gmenu-bins/releases) for the most recent version of GoMenu.

## Features

- **Dynamic Menu**: Creates a quick and responsive GUI menu for various command-line or GUI-based tasks.
- **Fuzzy Search**: Enhanced fuzzy search for better user experience.
- **Auto-Pick Options**: Automatically picks a single list of options and pre-applies a query when provided.
- **Instance Locking**: Ensures a single instance with the same title, improving resource management.
- **Focus Management**: Closes automatically when focus is lost, keeping your workspace clutter-free.
- **Customization Options**: Includes configurable colors, font sizes, and prompt settings to tailor the interface to your preferences.


## CLI

```shell
gmenu --help

gmenu is a fuzzy menu selector

Usage:
  gmenu [flags]

Flags:
      --auto-accept            Auto accept if there's only a single match.
  -h, --help                   help for gmenu
  -q, --initial-query string   Initial query to search for
  -m, --menu-id string         Menu ID
  -o, --preserve-order         Preserve the order of the input items
  -p, --prompt string          Prompt of the menu window (default "Search")
  -s, --search-method string   Search method (default "fuzzy")
  -t, --title string           Title of the menu window (default "gmenu")
```

## TODO

Here are some planned improvements and features for `gmenu`:

- [ ] **Window ID and PID Reporting**: Option to report created window's ID and PID for better process tracking.
- [ ] **Multiple Selection**: Ability to select multiple items.
- [ ] **Ctrl+C Escape Behavior**: Make Ctrl+C work like Esc for quick exits.
- [ ] **Focus Border Customization**: Remove focus border color for input to match aesthetics.
- [ ] **Improved Fuzzy Matching**: Enable character presence check and relative count for better search relevance.
- [ ] **CLI Support**: Add CLI mode to support similar behavior directly in the terminal.
- [ ] **dmenu Compatibility Survey**: Explore `dmenu` options to enhance compatibility.
  - **Prompt Support**: Add an option for prompt text similar to `dmenu`.
- [ ] **Preserve Input Order**: Maintain original input order on startup and after resets.
- [x] **Enhanced Fuzzy Search**: Avoid matching single characters alone unless they are near a separator. => does it need to be configurable?
- [x] **Auto-Pick Options**: Automatically pick from a single list of options and pre-apply a query if available.
- [x] **Remember Last Entry**: Automatically select the last entry used, or position it as the first option.
- [x] **Close on Focus Loss**: The menu automatically closes when it loses focus.
- [x] **Instance Lock Based on Name**: Ensures instance locking based solely on the menu name.
- [x] **Title-Based Instance Control**: Only one instance with the same title allowed.
- [x] **Improved Fuzzy Search**: Simplified fuzzy search to ignore some characters, such as spaces and underscores.

## Original Inspiration

`gmenu` is inspired by:

- [suckless dmenu](https://tools.suckless.org/dmenu/)
- [dmenu-mac](https://github.com/s7ephen/dmenu-mac)
- [rofi](https://github.com/davatorium/rofi)
