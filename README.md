# Intel Multi-AP manifest
Deploy all multiap repos in a single tree using google repo tool

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
repo init -u https://github.com/prplfoundation/intel_multiap_manifest.git
repo sync
repo forall -p -c 'git checkout $REPO_RREV'
```
## Build Instructions
Currently only the framework can be built in native Linux without special dependencies - see https://github.com/prplfoundation/intel_multiap_framework for build instructions.