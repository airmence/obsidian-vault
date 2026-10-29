A terminal is a text-based way to interact with a computer. You enter commands, and the computer displays the results. It’s useful for managing files, installing software, troubleshooting, and running programs.

## How the pieces fit together

1. Terminal emulator: The app that opens the terminal window and displays text. Examples include Kitty, Ghostty, Alacritty, WezTerm, and GNOME Terminal.
2. Shell: The program running inside the terminal that reads and interprets what you type. Examples include Bash, Zsh, Fish, and Nushell.
3. Command: An instruction or program you run in the shell, such as `ls` to list files or `pwd` to show your current directory.

For example, when I open Kitty and type `ls`, Kitty displays the terminal, the shell receives the command, and `ls` lists the files.

## Terminal emulator examples

|Terminal emulator|Description|
|---|---|
|Kitty|Feature-rich terminal emulator with support for tabs, windows, and graphics features|
|Ghostty|Modern terminal emulator designed for speed and native integration with desktop environments|
|Alacritty|Minimal, GPU-accelerated terminal emulator focused on performance|
|WezTerm|Customizable terminal emulator with tabs, panes, and scripting|
|GNOME Terminal|Traditional graphical terminal commonly used with the GNOME desktop|

A terminal emulator is mostly a matter of preference: people may choose one for its appearance, features, performance, or integration with their desktop.

## Terminal multiplexer

A terminal multiplexer is a tool for organizing terminal sessions into windows or panes. tmux and GNU Screen are examples. They run _inside_ a terminal emulator; they are not terminal emulators themselves. A multiplexer can also keep a session running while you disconnect and reconnect.

## Related notes
[[Basics command]]
[[bash]]