# yaml-parser
Basic YAML-parser written in Bash shell, using GNU Utilities.  
I wrote this for projects which would be strictly Bash compliant, so using [`yq`](https://github.com/mikefarah/yq) in this case wouldn't be an option.  
I try to be POSIX-compliant as much as possible, but that's something I can't guarantee or support.

# Features
- Supports reading of YAML files content in `.yml` & `.yaml` format.
- Supports reading values of YAML keys.
- Supports writing values to YAML keys.

# Unsupported
- Reading YAML arrays (planned in the future)
- Writing values to YAML arrays (planned in the future)
- Anything else that I don't know (as I'm not an advanced user of YAML files)

# Usage
```
# See help for some useful info:
yaml-parser
yaml-parser help
yaml-parser --help
yaml-parser -h

# Read YAML file content:
yaml-parser document.yml

# Read YAML value from YAML key:
yaml-parser document.yml key

# Write YAML value to YAML key:
yaml-parser document.yml -w key value
yaml-parser document.yml --write key value
```

# Installation

**Local (only current user has access):**
```sh
wget --directory-prefix="$HOME/.local/bin/" https://raw.githubusercontent.com/fiftydinar/yaml-parser/main/yaml-parser && chmod +x "$HOME/.local/bin/yaml-parser"
```

**System:**
```sh
sudo wget --directory-prefix="/usr/local/bin/" https://raw.githubusercontent.com/fiftydinar/yaml-parser/main/yaml-parser && sudo chmod +x "/usr/local/bin/yaml-parser"
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
