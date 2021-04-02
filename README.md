# Highlight RMS Supporters
A cross-platform utility to highlight RMS support letter signers.

# Table Of Contents

- [Prebuilt Extensions/Userscripts](#prebuilt-extensionsuserscripts)
- [Design](#design)
- [Developing](#developing)
- [Installation](#installation)
- [Settings](#settings)
- [License](#license)
- [Contributing](#contributing)

# Prebuilt Extensions/Userscripts

Pre-built extensions and userscripts are provided under the [dist](/dist) directories.

# Design

This browser extension/userscript fetches and parses a list of signers to the RMS support letter, and then uses local storage to store stylesheets to highlight their names on Github or Gitlab.

# Developing

In order to create a simple, cross-platform browser extension with code re-use, we have a single `src` folder and `icons` directory, which are then distributed with the platform-specific manifests to create the package. All the tools to generate these dist packages can be found under `tools`.

The following dependencies are required for building your own `dist` packages:
- Node.js
- Bash
- Rollup.js

Rollup.js may be installed by:

```bash
npm install --global rollup
```

# Installation

Chrome and Firefox do not allow installing packages outside the app stores for security reasons. However, the preferred way is installing a Tampermonkey userscript.

First, if desired, build the desired extensions. If using the prebuilt files, skip this step.

```bash
# Build the Tampermonkey extension.
tools/make-userscript.sh

# Build the Firefox extension.
tools/make-firefox.sh

# Build the Chrome/Chromium extension.
tools/make-chromium.sh
```


# License

GPL license



