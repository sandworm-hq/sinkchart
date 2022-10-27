<!-- Sandworm Logo -->
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="logo-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="logo-light.png">
  <img alt="Sandworm" src="logo-dark.png" width="478">
</picture>

<!-- A spacer -->
<p>&nbsp;</p>

Beautiful Visualizations For Your App's Dependencies 🪱

> Made by the team behind [Sandworm](https://sandworm.dev/) - Easy auditing & sandboxing for your JavaScript dependencies.

## Install

```bash
yarn global add sinkchart # or npm install -g sinkchart
```

> **Warning**
> Does NOT currently work with [pnpm](https://pnpm.io/).

## Options

```
Options:
      --version          Show version number                           [boolean]
      --help             Show help                                     [boolean]
  -o, --output           The name of the output SVG file                [string]
  -d, --dev              Include dev dependencies     [boolean] [default: false]
  -v, --show-versions    Show package versions        [boolean] [default: false]
  -t, --type             Visualization type
                         [string] [choices: "tree", "treemap"] [default: "tree"]
  -p, --path             The application path
                   [string] [default: "/Users/user/projects/Sandworm/sinkchart"]
      --md, --max-depth  Max depth to represent                        [integer]
```

## Chart Types

### Treemap
* Node colors represent the dependency depth;
* Node surface represents the size of the corresponding directory under `node_modules`;
* A dotted pattern in a node background means the package is a shared dependency, required by multiple packages, and present multiple times in the chart;
* Shared dependency sizes are added to every dependend package, to properly represent the independent size structure; hence, the displayed size might be larger than the actual size on disk;
* A red package background means the package has direct vulnerabilities;
* A purple package background means the package depends on other vulnerable packages;
* Click on a node to make the tooltip persist; click outside to close it;
* When representing deep dependencies, the surface area of certain packages might reach zero, making them invisible.

![Sinkchart Treemap Chart](https://sandworm-assets.s3.us-east-1.amazonaws.com/sinkchart/demos/sinkchart-treemap.png)

### Tree
* Nodes are grouped by color based on the root dependency that they belong to;
* Red text in a package name means the package has direct vulnerabilities;
* Purple text in a package name means the package depends on other vulnerable packages;
* Click on a node to make the tooltip persist; click outside to close it;
* By default, the tree chart has a maximum depth of 7 - only dependencies up to the seventh depth level will be represented, to keep thing readable; you can override this using the `--md` option.

![Sinkchart Tree Chart](https://sandworm-assets.s3.us-east-1.amazonaws.com/sinkchart/demos/sinkchart-tree.png)

## Samples

* Apollo Client 3.7.1
  * [Tree](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/apollo%403.7.1-tree.svg)
  * [Treemap](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/apollo%403.7.1-treemap.svg)

* AWS SDK 2.1218.0
  * [Tree](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/aws-sdk-js%402.1218.0-tree.svg)
  * [Treemap](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/aws-sdk-js%402.1218.0.svg)

* Express 4.18.1
  * [Tree](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/express%404.18.1-tree.svg)
  * [Treemap](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/express%404.18.1-treemap.svg)

* Mocha 10.1.0
  * [Tree](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/mocha%4010.1.0-tree.svg)
  * [Treemap](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/mocha%4010.1.0-treemap.svg)

* Mongoose 6.7.0
  * [Tree](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/mongoose%406.7.0-tree.svg)
  * [Treemap](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/mongoose%406.7.0-treemap.svg)

* Nest.js 9.1.2
  * [Tree](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/nest%409.1.2-tree.svg)
  * [Treemap](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/nest%409.1.2-treemap.svg)

* Redis 4.3.1
  * [Tree](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/node-redis%404.3.1-tree.svg)
  * [Treemap](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/node-redis%404.3.1-treemap.svg)

* NPM CLI 9.0.0
  * [Tree](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/npm%409.0.0-tree.svg)
  * [Treemap](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/npm%409.0.0-treemap.svg)

* PM2 5.2.2
  * [Tree](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/pm2%405.2.2-tree.svg)
  * [Treemap](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/pm2%405.2.2-treemap.svg)

* React Router 6.4.2
  * [Tree](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/react-router%406.4.2-tree.svg)
  * [Treemap](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/react-router%406.4.2-treemap.svg)

* Webpack Dev Server 4.11.1
  * [Tree](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/webpack-dev-server%404.11.1-tree.svg)
  * [Treemap](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/webpack-dev-server%404.11.1-treemap.svg)

* Webpack 5.74.0
  * [Tree](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/webpack%405.74.0-tree.svg)
  * [Treemap](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/webpack%405.74.0-treemap.svg)

* Winston 3.8.2
  * [Tree](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/winston%403.8.2-tree.svg)
  * [Treemap](https://sandworm-assets.s3.amazonaws.com/sinkchart/demos/winston%403.8.2-treemap.svg)