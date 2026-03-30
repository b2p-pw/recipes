#### App `metadata.json`

``` json
{
  "metadata_version": 1,
  "package": "my-app",
  "target": "b2p",
  "display_name": "My App!",
  "description": "My cool app can do awesome things.",
  "kernels": ["windows-nt"],
  "architectures": ["arm64", "i686", "x86_64"],
  "tags": ["cli", "app", "cool"],
  "categories": ["entertainment"],
  "aliases": ["my-coolest-app", "cool-app"],
  "authors": ["App author", "App author team"],
  "maintainers": ["My self", "My team"],
  "licenses": ["GPL-3.0-only"],
  "homepage": "https://my-app-homepage.cool",
  "repository": "https://github.com/app-team/my-app",
  "default": {
    "bsd": {
      "flavor": "vanilla",
      "recipe_version": "1.0.0"
    },
    "gnu-linux": {
      "flavor": "vanilla",
      "recipe_version": "1.0.0"
    },
    "windows": {
      "flavor": "vanilla",
      "recipe_version": "1.0.0"
    }
  }
}
```

#### App `manifest.json`

``` json
{
  "manifest_version": 1,
  "b2p_requirement": ">=1.0.0",
  "package": "my-app",
  "recipe_version": "1.0.0",
  "flavor": "vanilla",
  "environment": {
    "kernel": "windows-nt",
    "depends": {
      "net@runtime": ">=7.15 <8.0"
    }
  },
  "runtime": {
    "shims": [
      {
        "name": "bin-1",
        "binary": "bin/binary 1.exe",
        "args": "--path 'C:\\'"
      },
      {
        "name": "bin-2",
        "binary": "bin/binary 2.exe"
      }
    ],
    "backup": {
      "files": [
        "config.ini",
        "data/data.json"
      ]
    }
  },
  "scripts": {
    "upgrader": "remove-and-upgrade",
    "remover": "remove-directory"
  }
}
```

#### Lib `metadata.json`

``` json
{
  "metadata_version": 1,
  "package": "my-lib",
  "target": "l2p",
  "display_name": "My Lib!",
  "description": "My cool lib can do awesome things.",
  "kernels": ["bsd", "linux", "windows-nt"],
  "architectures": ["any"],
  "tags": ["cli", "lib", "cool"],
  "categories": ["utilities", "development"],
  "aliases": ["my-coolest-lib", "cool-lib"],
  "authors": ["Lib author", "Lib author team"],
  "maintainers": ["My self", "My team"],
  "licenses": ["Apache-2.0", "MIT"],
  "homepage": "https://my-lib-homepage.cool",
  "repository": "https://github.com/lib-team/my-lib",
  "default": {
    "bsd": {
      "flavor": "vanilla",
      "recipe_version": "1.0.0"
    },
    "gnu-linux": {
      "flavor": "vanilla",
      "recipe_version": "1.0.0"
    },
    "windows": {
      "flavor": "vanilla",
      "recipe_version": "1.0.0"
    }
  }
}
```

#### Lib `manifest.json`

``` json
{
  "manifest_version": 1,
  "b2p_requirement": ">=1.0.0",
  "package": "my-lib",
  "recipe_version": "1.0.0",
  "flavor": "vanilla",
  "environment": {
    "kernel": "windows-nt",
    "depends": {
      "net@framework": ">=4.8 <5.0",
      "choice_1": [
        { "mingw-w64": ">=12.0" },
        { "msvc": ">=17.0" }
      ],
      "choice_2": [
        { "vscode": "any" },
        { "clion": ">=2023.1" },
        { "neovim": "any" }
      ]
    }
  },
  "scripts": {
    "upgrader": "remove-and-upgrade",
    "remover": "remove-directory"
  }
}
```

#### Generic `label.md`

``` md
# My App

> A short, punchy tagline that describes the flavor of this software.

## ✨ Highlights

- **Key Feature 1:** Why is this app special?
- **Key Feature 2:** What problem does it solve?
- **Key Feature 3:** Why download the `b2p` version?

## 🚀 Quick Taste

Example command to show the app in action:

    my-app --help

## 📝 About

A more detailed description of the ingredients and what the user can expect after the installation.
```

#### Generic `recipe.idx`

``` shell

```