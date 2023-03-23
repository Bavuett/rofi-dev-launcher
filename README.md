# Rofi Dev Launcher

Rofi Dev Launcher is a script that lets you launch projects on your preferred Development Environment using [Rofi](https://github.com/davatorium/rofi).

## Dependencies

These are the dependencies you need to install in order to run the script.

- [Rofi](https://github.com/davatorium/rofi);
- [Python](https://www.python.org/).

## Installation 

Open a terminal and run the commands listed below.

```sh
# Clone the repository (or download the script from the releases page).
git clone https://github.com/Bavuett/rofi-dev-launcher.git
# Make the script executable.
cd rofi-dev-launcher
chmod +x rofi-dev-launcher
# Move the script to a directory in your PATH.
mv rofi-dev-launcher /usr/local/bin
```

## Usage

### Running the Script

To use the script, you define two environment variables: `ROFI_EDITOR` and `ROFI_DIRECTORY`. These can be defined in your shell's configuration file (such as `~/.bashrc`) or while running the script.

```sh
ROFI_DIRECTORY=[YOUR DIR] ROFI_EDITOR=[YOUR EDITOR] rofi -show dev -modi dev:rofi-dev-launcher
```

`ROFI_EDITOR` is the command that will be used to open the project. For example, if you want to use Visual Studio Code, you would set `ROFI_EDITOR` to `vscode`. 

You can find all the supported editors [here](rofi-dev-launcher) in the `EDITORS` constant you can find at the beginning. If you want to use an editor that is not supported, you can add it to the script and - if you'd like - submit a pull request so others can use it too.

`ROFI_DIRECTORY` is the directory where the script will look for projects. It can be a relative or absolute path, so you can use `~` to refer to your home directory without having to type the full path.

### Integration with Window Managers

You can use the script with your Window Manager by adding a shortcut to it. For example, in [i3](https://github.com/i3/i3), you can add the following line to your configuration file to bind the script to the `Mod+Shift+w` shortcut.

```
bindsym $mod+Shift+w exec --no-startup-id "ROFI_DIRECTORY=[YOUR DIR] ROFI_EDITOR=[YOUR EDITOR] rofi -show dev -modi dev:rofi-dev-launcher"
```

## Contributing

If you think that people can benefit from a feature you added or have any suggestions, feel free to open an issue or a pull request.

Please remember to follow the [Code of Conduct](https://github.com/Bavuett/.github/blob/main/CODE_OF_CONDUCT.md) when interacting with the community.

## License

This project is licensed under the [MIT License](LICENSE).
