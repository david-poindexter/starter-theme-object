﻿# starter-theme-object

[![License: MIT](https://img.shields.io/badge/LICENSE-MIT-informational.svg)](https://opensource.org/licenses/MIT)

**starter-theme-object** is a Theme Object starter project for [DNN Platform](https://github.com/dnnsoftware/Dnn.Platform) (formerly known as DotNetNuke) made by and for the [DNN Community](https://dnncommunity.org).

## Installation

### Installation Option #1

Clone this repo into a clean directory of your choice.

```bash
git clone https://github.com/DNNCommunity/starter-theme-object.git .
```

### Installation Option #2

Use **dnn-cli**, which is [available as an npm package](https://www.npmjs.com/package/@dnncommunity/dnn-cli).  **dnn-cli** it can be installed via **yarn** or **npm**.

---
#### Install dnn-cli...

...via **yarn**:

```bash
yarn global add @dnncommunity/dnn-cli
```

...via **npm**:

```bash
npm install -g @dnncommunity/dnn-cli
```
---

Once **dnn-cli** is installed, this starter project can be installed into an empty directory of your choice.

```bash
cd <directory path>
dnn theme-object
```

## Usage

1. Install DNN in a `.\Website` folder (root of directory in which this project is cloned)
2. Open solution file in Visual Studio 2019 (Run as Adminstrator...)
3. Build in `Debug` or `Release` mode

### Debug

By default this will compile the project and deploy it to the `.\Website` folder.  
- DLL and PDB files will be deployed to `.\Website\bin`
- All other relevant files will be deployed to `.\Website\DesktopModules\ThemeObjects\starter-theme-object`

### Release

By default this will create a theme object install package and place in `.\Website\Install\Skin` so it will be in **Available Extensions** within DNN (SETTINGS > Extensions > Available Extensions).

### Implementation

To implement the theme object within a theme, the following two items are required.

1. Register the theme object at the top of the desired ASCX file within the theme.

```html
<%@ Register TagPrefix="dnn" TagName="my_theme_object" Src="~/DesktopModules/ThemeObjects/starter-theme-object/my_theme_object.ascx" %>
```

2. Utilize the following theme object code within the same ASCX file for which the above was registered.

```html
<dnn:my_theme_object id="myThemeObject1" runat="server" />
```

## Contributing
Pull requests are welcome. Please open an issue first to document the bug or enhancement details.

## License
[![License: MIT](https://img.shields.io/badge/LICENSE-MIT-informational.svg)](https://opensource.org/licenses/MIT)