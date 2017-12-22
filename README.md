# Cordova sqlite evmax parallel reader test app

**AUTHOR:** [@brodybits (Christopher J. Brody aka Chris Brody)](https://github.com/brodybits)

LICENSE: GPL or commercial

**NOTE:** This project includes JQuery (2.2.4) and Bootstrap (3.3.6) under the MIT license. Otherwise there is no code copied from other sources.

**IMPORTANT:** Whitelist and intent items are omitted from this test app.

## Dependencies

- Bootstrap (3.3.6) - included (MIT license)
- JQuery (2.2.4) - included (MIT license)
- Cordova sqlite plugin - please add the desired version from the Cordova CLI as described below

## To add another plugin

```shell
cordova plugin add my-plugin-id --save
```

## How to run

1. Add the desired Cordova sqlite plugin version, for example:

```shell
cordova plugin add cordova-sqlite-storage --save
```

2. Add the desired platform(s), for example:

```shell
cordova platform add android
```

3. Do `cordova prepare` (may not always be necessary but good to be on the safe side):

```shell
cordova prepare
```

4. Run it on your mobile emulator or device, for example:

```shell
cordova run android
```

## Functionality

- Upon startup: open a database and CREATE the test table
- alert dialog test
- Echo test
- Self test
- Location reload
- String test 1
- String test 2 (string as a SQL parameter)
- Show record count (query parallel database reader)
- Add record
- Add 100 records from JavaScript object after delay
- Delete all records
- Follow link to page 2
- Change window.location to page 2

## Multi-page test

It is possible to switch between two pages using "follow link" buttons. The main page also has a button to go to page 2 by changing `window.location`. There is also a button on both pages to try `location.reload()`.

The sqlite plugin should continue to work after the user changes to another page or triggers `location.reload()`.
