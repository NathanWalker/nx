# ngrx
--------

## Overview

Generates a ngrx feature set containing an `init`, `interfaces`, `actions`, `reducer` and `effects` files. 

You use this schematic to build out a new ngrx feature area that provides a new piece of state.

## Command

```sh
ng generate ngrx FeatureName [options]
```

##### OR

```sh
ng generate f FeatureName [options]
```

### Options

Specifies the name of the ngrx feature (e.g., Products, User, etc.)

- `name`
  - Type: `string`
  - Required: true

Path to Angular Module. Also used to determine the parent directory for the new **+state** 
directory; unless the `--directory` option is used to override the dir name.

>  e.g. --module=apps/myapp/src/app/app.module.ts

- `--module`
  - Type: `string`
  - Required: true

Specifies the directory name used to nest the **ngrx** files within a folder.

- `--directory`
  - Type: `string`
  - Default: `+state`

#### Examples

Generate a `User` feature set and register it within an `Angular Module`.

```sh
ng generate ngrx User -m apps/myapp/src/app/app.module.ts
ng g ngrx Producrts -m libs/mylib/src/mylib.module.ts
```


Generate a `User` feature set within a `user` folder and register it with the `user.module.ts` file in the same `user` folder.

```sh
ng g ngrx User -m apps/myapp/src/app/app.module.ts -directory user
```
