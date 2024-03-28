# yaml-parser
Basic YAML-parser written in SH shell, using GNU Utilities.  
I wrote this for projects which are strictly coded in shell language (mostly Bash), so using [`yq`](https://github.com/mikefarah/yq) in this case wouldn't be an option.  
I try to be POSIX-compliant as much as possible in order to improve compatibility, but I can't guarantee that yaml-parser will work on every POSIX-based OS.

# Features
- **Supports reading of YAML files content in `.yml` & `.yaml` format.**
- **Supports reading values of YAML keys.**
- **Supports writing values to YAML keys.**

# Unsupported
- **Reading YAML arrays**
- **Writing values to YAML arrays**
- **Anything else that I don't know**

# Usage
```
# See help to display this "Usage" info:
yaml-parser
yaml-parser help
yaml-parser --help
yaml-parser -h

# Read YAML file content:
yaml-parser "file.yml"

# Read YAML value from YAML key:
yaml-parser "file.yml" "key"

# Write YAML value to YAML key:
yaml-parser "file.yml" -w "key" "value"
yaml-parser "file.yml" --write "key" "value"

# Write quoted YAML value to YAML key:
yaml-parser "file.yml" -w "key" "\"value\""
yaml-parser "file.yml" --write "key" "\"value\""

# Do multiple operations with yaml-parser:
yaml-parser "file1.yml" && yaml-parser "file2.yml"
```

# Installation

Only tested on Linux with GNU Utilities.

If local install command doesn't work, you will probably need to add `$HOME/.local/bin` directory to path in shell profile.
Alternatively, modify the command to install `yaml-parser` to `$HOME/bin` directory instead.  
System install command should work for most Linux distributions.

MacOS, FreeBSD & OpenBSD support is unknown.

**Local (only current user has access):**
```sh
curl -o "$HOME/.local/bin/yaml-parser" --create-dirs https://raw.githubusercontent.com/fiftydinar/yaml-parser/main/yaml-parser && chmod +x "$HOME/.local/bin/yaml-parser"
```

**System:**
```sh
sudo curl -o "/usr/local/bin/yaml-parser" --create-dirs https://raw.githubusercontent.com/fiftydinar/yaml-parser/main/yaml-parser && sudo chmod +x "/usr/local/bin/yaml-parser"
```

# Uninstallation

**Local:**
```sh
rm "$HOME/.local/bin/yaml-parser"
```

**System:**
```sh
sudo rm "/usr/local/bin/yaml-parser"
```
