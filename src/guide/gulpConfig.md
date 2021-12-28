# Gulp Config

Arctic Admin provides you build tools to streamline your production build and compilation process. We have configured code compilation, asset management, source and distribution path in `gulp.config.js`. You can edit the configuraion as your requirements.

## gulp commands

- Serve PUG and watch files: `gulp --layout[x]` (e.g. gulp --layout1)
- For RTL: `gulp --layout[x]-rtl --rtl` (e.g. gulp --layout1-rtl --rtl)

inside `build-tools` folder use `gulp commands`

## Config Property

| Config property |   Type   |             Descriiption             |
| :-------------: | :------: | :----------------------------------: |
| `config.dist `  | `object` | Contains distribution path of assets |
|  `config.src `  | `object` |    Contains source path of assets    |

## Bundle Options

| Bundle Options                                       | Type     | Descriiption                                                                                                                                                                                                                                             |
| :--------------------------------------------------- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `config.bundle `                                     | `object` | Contains bundle configurations                                                                                                                                                                                                                           |
| `config.bundle[bundle_name]`                         | `object` | `[bundle_name]` is the name of the bundle. You can change this name. Generated bundle name will be `[bundle_name].bundle.min.js` and `[bundle_name].bundle.min.css` <br/> <br/> Default bundles <br/><br/> - `main`<br/> - `main-dark` <br/> - `vendors` |
| `config.bundle[bundle_name].src`                     | `object` | Contains packages to be bundled.                                                                                                                                                                                                                         |
| `config.bundle[bundle_name].src[package_name]`       | `object` | `[package_name]` is name of the package. This object contains JS and style files.                                                                                                                                                                        |
| `config.bundle[bundle_name].src[package_name].js`    | `array`  | Contains JS source files of `[package_name]` package                                                                                                                                                                                                     |
| `config.bundle[bundle_name].src[package_name].style` | `array`  | Contains style source files(scss/css) of `[package_name]` package                                                                                                                                                                                        |
| `config.bundle[bundle_name].dist`                    | `object` | Contains distribution path of bundled files.                                                                                                                                                                                                             |
| `config.bundle[bundle_name].dist.style`              | `string` | Distribution path of bundled CSS (`[bundle_name].bundle.css`) file.                                                                                                                                                                                      |
| `config.bundle[bundle_name].dist.js`                 | `string` | Distribution path of bundled JS (`[bundle_name].bundle.js`) file.                                                                                                                                                                                        |

## Copy Options

| Copy Options                                 | Type     | Descriiption                                                                                                                                                                                                                                         |
| :------------------------------------------- | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `config.copy`                                | `object` | Contains assets(js, scss, css, images, fonts & etc) to be copied to dist.                                                                                                                                                                            |
| `config.copy[group_name]`                    | `object` | Name of a group of assets to be copied to dist. <span style="color:blue">Nothing depends on this names.</span> <br/> Default group names: <br/> `vendors`, `images-fonts`, `js`, `data`, `scss`                                                      |
| `config.copy[group_name].baseDir`            | `string` | Path of a base/parent directory from where child directories are copied. <br/> Child directories are specified in `config.copy[group_name].src[item_name].dir` <br/> This is required to tell gulp that copy entire directory instead of only files. |
| `config.copy[group_name].src`                | `string` | Contains the items to be copied.                                                                                                                                                                                                                     |
| `config.copy[group_name].src[item_name]`     | `string` | Contains the array of directory path. <br/> <span style="color:blue">Nothing depends on this names.</span>                                                                                                                                           |
| `config.copy[group_name].src[item_name].dir` | `array`  | An array of directory paths. This derectories are copied to <br/> `config.copy[group_name].dist`                                                                                                                                                     |
| `config.copy[group_name].dist`               | `string` | Directories are copied to this location.                                                                                                                                                                                                             |
