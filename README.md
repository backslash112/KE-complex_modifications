[![Build Status](https://travis-ci.org/pqrs-org/KE-complex_modifications.svg?branch=master)](https://travis-ci.org/pqrs-org/KE-complex_modifications)

# KE-complex_modifications

complex_modifications for Karabiner-Elements.

https://pqrs.org/osx/karabiner/complex_modifications/


## Update in dev-cun branch

Add two new json files:
1. [docs/json/right_arrow_to_screenshot.json](https://github.com/backslash112/KE-complex_modifications/commit/597666412ba675ebaad71b45ba4b3cdd5e3fe7f3)
2. [docs/json/left_command_twice.json](https://github.com/backslash112/KE-complex_modifications/commit/0623fa45802110928ca938dcbda9847c1a5d5795)

## Update docs

Run make in terminal.

```
make
```

## Add rules

1. Put a `.erb` template file to [src/json](https://github.com/pqrs-org/KE-complex_modifications/tree/master/src/json). (Or put a `.json` file to [docs/json](https://github.com/pqrs-org/KE-complex_modifications/tree/master/docs/json) directly.)
2. (Optional) Put extra description to [docs/extra_descriptions](https://github.com/pqrs-org/KE-complex_modifications/tree/master/docs/extra_descriptions).
3. Add new json to [docs/groups.json](https://github.com/pqrs-org/KE-complex_modifications/tree/master/docs/groups.json).
4. Run `make` in terminal.

### Note

`docs/index.html` does not work properly if you open it via `file://...`.<br />
Launch a local web server by `make server` in terminal and open http://localhost:8000 .<br />
(You can quit the local web server by the `control-c` shortcut in terminal.)

Karabiner-Elements cannot import the json from the local web server due to the no https connection between local web server.<br />
Please import the json via file copy. (See Local testing section.)

## complex_modifications documents

https://pqrs.org/osx/karabiner/json.html

## Local testing

1. Copy a json file to `~/.config/karabiner/assets/complex_modifications`.
2. Import rules from Karabiner-Elements Preferences.

### Example

```
$ cp docs/json/caps_lock.json ~/.config/karabiner/assets/complex_modifications
```

Then open `Karabiner-Elements Preferences > Complex Modifications > Rules > Add rule`

----------

# Karabiner-Elements Usage

## Import file from another site

1. Put a json file to your site.
2. Make a link `karabiner://karabiner/assets/complex_modifications/import?url=<JSON_URL>`.
3. Open the link from web browser.
