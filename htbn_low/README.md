# Low level programming

## betty linter
```git clone https://github.com/holbertonschool/Betty.git```
- `cd` into the Betty directory  
- install the linter with `sudo ./install.sh`  
- emacs a new file called `betty`, and copy the script below: 

```
#!/bin/bash
# Simply a wrapper script to keep you from having to use betty-style
# and betty-doc separately on every item.
# Originally by Tim Britton (@wintermanc3r), multiargument added by
# Larry Madeo (@hillmonkey)

BIN_PATH="/usr/local/bin"
BETTY_STYLE="betty-style"
BETTY_DOC="betty-doc"

if [ "$#" = "0" ]; then
    echo "No arguments passed."
    exit 1
fi

for argument in "$@" ; do
    echo -e "\n========== $argument =========="
    ${BIN_PATH}/${BETTY_STYLE} "$argument"
    ${BIN_PATH}/${BETTY_DOC} "$argument"
done
```
-  change permissions to apply to all users with `chmod a+x betty`  
-  ```mv betty /bin/```

## emacs config for betty
emacs a new file called `.emacs`, and copy the script below: 

```
(setq c-default-style "bsd"
      c-basic-offset 8
      tab-width 8
      indent-tabs-mode t)
(require 'whitespace)
(setq whitespace-style '(face empty lines-tail trailing))
(global-whitespace-mode t)
```

## shortcuts
```
git config --global user.name ""  
git config --global user.email ""  
git config --global credential.helper store  
```
