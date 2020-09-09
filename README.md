## Lesser Known NPM Commands

We know the basic `npm` commands:
 
* `start`
* `init`, `init -y`
* `link`
* `update`
* flags, `--save-dev`
* shorthand `i`, `t`, `ci`, `-D`, `-S` etc

...but lets take a look at some other useful and lesser commands that we can add to our tool belt.

### `npm pack`

Test if our package installs without publishing

```bash
# pack your application into a .tgz
npm pack

# change to your install dir
cd ~/foo

# install using the .tgz
npm install ~/package/package.1.0.0.tgz
```

### `npm outdated`

Check to see outdated packages

```bash
# check to see what packages are outdated
npm outdated
```

### `npm ls -g --depth=0` || `npm ls --depth=0`

Check to see installed packages at a particular depth

```bash
# at a particular depth, in this case first level of tree
npm ls -g --depth=0
```

#### `npm home react`

Opens up the homepage for the package

```bash
# this will open up the home page for the package
npm home react
```

### `npm repo fp-ts`

Opens up the github repo page for the package

```bash
# this will open up the github repo page for the package
npm repo fp-ts
```

### `npm prune`

Removes packages not listed as parent package deps

```bash
# remove packages not listed as parent package dependencies
npm prune

audited 9 packages in 0.809s
found 0 vulnerabilities
```

### `npm ls`

Lists installed packages, you can use `--depth` here, nice ..

```bash
# Local with tree
npm ls

# Local, only parent
npm ls --depth=0

# Global, only parent
npm ls -g --depth=0

# List production packages only
npm ls --prod
```

### `npm install --dry-run` 

Only reports what will be install, but does not install it

```bash
# dry run
npm i --dry-run typescript

+ typescript@4.0.2
added 1 package and audited 64 packages in 1.476s
found 0 vulnerabilities

```

### `npm dedupe`

Remove duplicate packages from `node_modules`

```bash
npm dedupe
```

### `npm i expressjs/morgan`

Install a package via git repo at actual commit you want, default will be at `head`

```bash
# install package from github
npm i expressjs/morgan

# list morgan
npm ls morgan
npm-commands@1.0.0 /Users/ahadbokhari/npm-projects/npm-commands
└── morgan@1.10.0  (github:expressjs/morgan#19a6aa5369220b522e9dac007975ee66b1c38283)
```

You can also install from a specific commit or tag branch and can install the package at any point in it's history

### Note

You can also use `--json` flag to output a json style as well as replace `ls` with `ll` for a more descriptive output.

