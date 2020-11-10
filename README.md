# OBSOLETE

WARNING: These instructions are obsolete and likely don't work well anymore.
The prplmesh repository has been moved to https://gitlab.com/prpl-foundation/prplMesh
A lot of repositories that were once separate have been combined into this one, removing the need for a manifest file.
Instead of using `repo`, it's recommended now to just use `git clone` to get that code.
See the project at the new location for more info

# prplMesh manifest
Deploy all prplMesh repos in a single tree using google repo tool

## Requirements
Download & install google repo - https://source.android.com/setup/build/downloading

## Initialize & sync
Optional - to avoid ssh keys and password reprompt, add the following to ~/.gitconfig:
```
[url "https://github.com/"]
        insteadOf = git@github.com:

[url "https://github.com/"]
        insteadOf = ssh://git@github.com/

```
Then run the following commands to fetch the code:
```
repo init -u https://github.com/prplfoundation/prplMesh-manifest.git
repo sync
repo forall -p -c 'git checkout $REPO_RREV'
```

## Build Instructions
Each component can be built with CMAKE, or use maptools.py build command - see [prplMesh-tools](https://github.com/prplfoundation/prplMesh-tools)
