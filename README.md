
### Setup for your environment

  - [ ] use `docs/example.local.properties` to build a `local.properties` file
  - [ ] place local properties file in `/android`


### Initial build specs

    depending on your version of java you may need to updgrade to the latest gradle.

    also removed wrapper :
    ```
      task wrapper(type: Wrapper) {
          gradleVersion = '5'
          distributionUrl = distributionUrl.replace("bin", "all")
      }
    ```
    _duplicate declaration_

###  Debugging react native

`adb shell input keyevent 82` - opens developer menu on device
full restart from a device - may need to go into the apps menu and fully delete
the app, espc if name is the same

clean script:

`rm -rf $TMPDIR/react-* && rm -rf $TMPDIR/metro-* && rm -rf $TMPDIR/haste-* && watchman watch-del-all && rm -rf node_modules/ && npm install && npm start -- --reset-cache`

_if sha is incorrect ->_

  reset cache

yarn start -- --reset-cache

