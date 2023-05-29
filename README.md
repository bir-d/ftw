# ftw
File Type Wrangler -- a simple way to define and execute actions for certain file types
# Usage
Once installed, create a config file at `~/.ftw_config` and populate it with your desired file types and actions. Then simply run it: `ftw <FILE>`. I suggest adding it as the default execution method for a TUI file browser such as [fff (relevant section linked).](https://github.com/dylanaraps/fff#bash-and-zsh).

The priority order is file extension > MIME subtype > MIME type
# Config
Configuration is via JSON stored by default at `~/.ftw_config`. Each object can be an extension or mime type and specifies a command to be executed. Use `@a` to insert the given file into the command.
## Example:
```
{"zip": "unzip @a"} # file extension
{"x-shellscript": "bash @a"} # MIME subtype
{"text": vim @a} # MIME type
```
## Install
* Install dependencies via your favorite method -- you will need `file` and `jq`.
* Place `ftw` somewhere on your path.
* Thats it!
