# yaml-parser
Basic YAML-parser written in Bash using GNU Coreutils.  
I wrote this for projects which would be strictly Bash or POSIX compliant, so using [`yq`](https://github.com/mikefarah/yq) in this case wouldn't be an option.

# Features
- Supports reading of YAML files content in `.yml` & `.yaml` format.
- Supports reading values of YAML keys.
- Supports writing values to YAML keys.

# Unsupported
- Reading YAML arrays (planned in the future)
- Writing values to YAML arrays (planned in the future)

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
