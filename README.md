# NectarJS Modules repository

This repo is the main repo to publish and share your NectarJS modules

# How to do

- Create a repo for your own module
- Fork this repository
- Add your module repository as a submodule : `git submodule add https://github.com/me/my_nectar_module my_nectar_module`
- Make a PR

# Rules 

- A module should have the required properties :
```json
"nectar":
  {
    "env": ["std", "android", "ios", "node", "wasm", "test"],
    "read_only": [],
    "lib": ["-Isomelib", "mydep.cpp"]
  }
```
- A module cannot have offensive or forbidden content

# How it works

- Every hours, a pull of this repo and all submodules is done; and all submodules are zipped on modules.nectarjs.org
- Then, with NectarJS, you can simply install every module with: `nectar -i module_name`
