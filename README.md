# Linuxfabrik's IcingaWeb2 Theme

![Screenshot](./screenshots/login.png)

## Installation

```bash
MODULE_NAME="linuxfabrik"
MODULE_VERSION="v1.0.0"
MODULE_AUTHOR="Linuxfabrik"
MODULES_PATH="/usr/share/icingaweb2/modules"
MODULE_PATH="${MODULES_PATH}/${MODULE_NAME}"
RELEASES="https://github.com/${MODULE_AUTHOR}/icingaweb2-theme-${MODULE_NAME}/archive"
mkdir "$MODULE_PATH" \
&& wget -q $RELEASES/${MODULE_VERSION}.tar.gz -O - \
   | tar xfz - -C "$MODULE_PATH" --strip-components 1
icingacli module enable "${MODULE_NAME}"
```

For details, have a look at https://icinga.com/docs/icinga-web/latest/doc/08-Modules/.
