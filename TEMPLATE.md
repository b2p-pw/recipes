#### App `metadata.json`

``` json
{
    "package": "my-app",
    "description": "My cool app can do awesome things.",
    "author": ["App author", "App author team"],
    "maintainers": ["My self", "My team"],
    "license": "MIT",
    "homepage": "https://my-app-homepage.cool",
    "repository": "https://github.com/app-team/my-app",
    "target": "b2p",
    "default": {
        "version": "1.0.0",
        "flavor": "vanilla"
    },
    "tags": ["cli", "app", "cool"],
    "categories": ["Utilities", "Development"]
}
```

#### Lib `metadata.json`

``` json
{
    "package": "my-lib",
    "description": "My cool lib can do awesome things.",
    "author": ["Lib author", "Lib author team"],
    "maintainers": ["My self", "My team"],
    "license": "MIT",
    "homepage": "https://my-lib-homepage.cool",
    "repository": "https://github.com/lib-team/my-lib",
    "target": "l2p",
    "default": {
        "version": "1.0.0",
        "flavor": "vanilla"
    },
    "tags": ["cli", "lib", "cool"],
    "categories": ["Utilities", "Development"]
}
```

#### App `manifest.json`

``` json
{
    "package": "my-app",
    "version": "1.0.0",
    "flavor": "vanilla",
    "environment": {
        "kernel": "Windows NT",
        "depends": {
            "net": ">=7.15"
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
        "installer": "recipe.yaml",
        "remover": "remove-directory"
    }
}
```

#### `checksums.sha256`

``` sha256
a1b2c3d4e5f6...  manifest.json
b8d9c0e1f2a3...  recipe.yaml
```