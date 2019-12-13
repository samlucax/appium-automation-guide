# Appium Mobile Automation Guide
[![N|Solid](https://www.keytorc.com/wp-content/uploads/2014/08/appium.png)](http://appium.io)

Trying to help others to understand the World of Appium

### Starting emulators

Use the npm packages `start-ios-simulator` & `start-android-emulator`. Links below:
- https://github.com/wswebcreation/start-ios-simulator
- https://github.com/wswebcreation/start-android-emulator

### Resources

|Platforms|Setup                                                |Drivers              |Capabilities                                   |Locators                               |Waits       |Actions |Gestures             |
|---------|-----------------------------------------------------|---------------------|-----------------------------------------------|---------------------------------------|------------|--------|---------------------|
|Android  |brew install gradle                                  |Selendroid (depre)   |app                                            |id                                     |            |        |scroll (TouchActions)|
|Android  |brew cask install android-platform-tools             |UiAutomator1 (depre) |packageName                                    |Android UiAutomator (UiAutomator2 only)|            |        |swipe (TouchActions) |
|Android  |brew cask install android-sdk                        |UiAutomator2         |                                               |Android View Tag (Espresso only)       |            |        |                     |
|Android  |brew install android-ndk                             |EspressoDriver (beta)|                                               |                                       |            |        |                     |
|Android  |brew cask install intel-haxm                         |                     |                                               |                                       |            |        |                     |
|Android  |sdkmanager "platform-tools" "platforms;android-28”   |                     |                                               |                                       |            |        |                     |
|Android  |sdkmanager "build-tools;28.0.1”                      |                     |                                               |                                       |            |        |                     |
|         |                                                     |                     |                                               |                                       |            |        |                     |
|iOS      |brew install carthage                                |UiAutomation ( < 9.3)|automationName                                 |iOS Predicate                          |            |        |scroll (js executor) |
|iOS      |brew tap facebook/fb (opcional)                      |XCUITest (> 9.3)     |useNewWDA                                      |iOS ClassChain                         |            |        |swipe (js executor)  |
|iOS      |brew install fbsimctl (opcional)                     |                     |waitForQuiescence                              |IOS UIAutomation                       |            |        |                     |
|iOS      |brew install libimobiledevice (real devices)         |                     |xcodeOrgId (real devices)                      |                                       |            |        |                     |
|iOS      |npm install -g ios-deploy (real devices)             |                     |xcodeSigningId (real devices)                  |                                       |            |        |                     |
|iOS      |brew install ios-deploy (real devices)               |                     |permissions (xcuitest / sim. utils)            |                                       |            |        |                     |
|iOS      |brew tap wix/brew (simulator utils)                  |                     |iosInstallPause (xcuitest / sim. utils)        |                                       |            |        |                     |
|iOS      |brew install wix/brew/applesimutils (simulator utils)|                     |connectHardwareKeyboard (xcuitest / sim. utils)|                                       |            |        |                     |
|         |                                                     |                     |                                               |                                       |            |        |                     |
|         |                                                     |                     |                                               |                                       |            |        |                     |
|Any      |brew install node                                    |                     |deviceName                                     |accessibilityId                        |implicitWait|click   |                     |
|Any      |npm i appium                                         |                     |udid                                           |className                              |explicitWait|sendKeys|                     |
|Any      |npm i wd                                             |                     |browser                                        |name                                   |            |        |                     |
|Any      |brew cask install java8                              |                     |                                               |xpath                                  |            |        |                     |
|Any      |brew install maven                                   |                     |                                               |-custom (usando find plugins)          |            |        |                     |
|Any      |                                                     |                     |                                               |Image (base 64)                        |            |        |                     |
|Any      |                                                     |                     |                                               |priority (page factory order)          |            |        |                     |



### SOS links

|Theme   |Plataform                                           |Reference              |
|-------|-----------------------------------------------------|---------------------|
|Alertas & Permissões|iOS                                                  |https://github.com/appium/appium-xcuitest-driver/pull/750|
|Idle state / App animations |iOS                                                  |https://github.com/appium/appium/issues/8929|
|Mobile Gestures|iOS                                                  |https://github.com/appium/appium/blob/master/docs/en/writing-running-appium/ios/ios-xctest-mobile-gestures.md|
|Mobile Gestures (2)|iOS                                                  |http://appium.io/docs/en/writing-running-appium/ios/ios-xctest-mobile-gestures/index.html|
|autoAcceptAlerts capability example (não funciona mais)|iOS                                                  |https://bitbar.com/appium-tip-9-how-to-automatically-dismiss-dialogs-and-autoaccept-alerts/|
|autoAcceptAlerts capability issue|iOS                                                  |https://github.com/appium/appium/issues/6863|
|Desabilitar 'waiting for idle state' no app|iOS                                                  |https://stackoverflow.com/questions/41277026/disabling-waiting-for-idle-state-in-ui-testing-of-ios-apps|
|Implicit & Explicit Wait|Any                                                  |http://www.qaautomated.com/2016/11/implicit-explicit-wait-with-appium.html|
|WebDriverAgent - Failure to determine system application: (null)|iOS                                                  |https://github.com/facebook/WebDriverAgent/issues/1013|
|WebDriverAgent - Lentidão pra iniciar o teste|iOS                                                  |https://github.com/facebook/WebDriverAgent/issues/1047|
|WebDriverAgent - Failure getting list of active applications|iOS                                                  |https://github.com/appium/appium/issues/11923|
|XCUITest Setup para iOS|iOS                                                  |http://appium.io/docs/en/drivers/ios-xcuitest/#migrating-from-the-uiautomation-driver|
|XCUITest Setup para iOS - Real devices|iOS                                                  |http://appium.io/docs/en/drivers/ios-xcuitest-real-devices/|
|AppleSimulatorUtils|iOS                                                  |https://github.com/wix/AppleSimulatorUtils|
|Migrando de UiAutomation para XCUITest|iOS                                                  |http://appium.io/docs/en/advanced-concepts/migrating-to-xcuitest/index.html|
|XCUITest Desired caps expecíficas|iOS                                                  |https://github.com/appium/appium-xcuitest-driver#desired-capabilities|
|Element Find Plugins|Any                                                  |http://appium.io/docs/en/advanced-concepts/element-finding-plugins/index.html|
|Appium Classifier Plugin|Any                                                  |https://github.com/testdotai/appium-classifier-plugin|
|iOS Predicate|iOS                                                  |http://appium.io/docs/en/writing-running-appium/ios/ios-predicate/index.html|
|XCUITest Posts - Perfecto Mobile|iOS                                                  |https://developers.perfectomobile.com/display/TT/XCUITest+Automation|
|Locators Documentação|Any                                                  |https://appium.github.io/java-client/io/appium/java_client/pagefactory/HowToUseLocators.html|
|PageFactory tree|Any                                                  |https://appium.github.io/java-client/io/appium/java_client/pagefactory/package-tree.html|
|ClassChaining Optimization|iOS                                                  |https://developers.perfectomobile.com/display/TT/XCUITest+Class+Chaining+and+Optimization|
|Android Setup - high level setup|Android                                              |https://gist.github.com/patrickhammond/4ddbe49a67e5eb1b9c03|
|WebDriverAgent|iOS                                                  |https://github.com/facebook/WebDriverAgent|
|accessibilityId é pra Android (content description) e iOS (accessibility ID)|Any                                                  |https://appiumpro.com/editions/20|
|Setting up App State|Any                                                  |https://appiumpro.com/editions/023|
|Explicação Arquitetura do Appium|Any                                                  |https://discuss.appium.io/t/cross-platform-mobile-test-automation-using-appium/14810|

### seek knowledge [todo]

- courses

#### About this project
I'm just sharing everything I'd searched and learned during a mobile project for Android and iOS. I hope it helps someone as well as helped me. If you have some fix ou improvement, enjoy this repo and contribute with a PR! :)
