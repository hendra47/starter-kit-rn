# starter-kit-rn
* Build Release
1.Place the my-release-key.keystore file under the android/app directory in your project folder.
2.Place the gradle.properties file under the android/ directory in your project folder.
3.Edit the file android/app/build.gradle in your project folder and add the signing config,
- Detail => https://facebook.github.io/react-native/docs/signed-apk-android.html
- Code =>   
- ...
signingConfigs {
        release {
            if (project.hasProperty('MYAPP_RELEASE_STORE_FILE')) {
                storeFile file(MYAPP_RELEASE_STORE_FILE)
                storePassword MYAPP_RELEASE_STORE_PASSWORD
                keyAlias MYAPP_RELEASE_KEY_ALIAS
                keyPassword MYAPP_RELEASE_KEY_PASSWORD
            }
        }
    }
- ...
signingConfig signingConfigs.release

4.command for execute apk
$ cd android
$ ./gradlew assembleRelease