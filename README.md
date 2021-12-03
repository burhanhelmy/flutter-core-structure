# flutter-core-structure

Thing should be considered

- Folder structure
- Environment variable
- Navigation
- Theme
- Network
- Testing

My approach is to go to folder by feature:


__Folder structure__


```
|- ▼ lib
|  |- main.dart
|  |- app.dart // combine all config and util 
|  |- ▼ config // app specific
|  |  |- ▼ theme
|  |  |  |- theme.dart
|  |  |  |- dark.dart
|  |  |  |- light.dart
|  |  |  |- colors.dart
|  |  |  
|  |  |- ▼ route
|  |  |  |- route.dart
|  |  |  |- route_guard.dart
|  |  |  |- routes.dart
|  |  |  
|  |  |- ▼ environment
|  |     |- environment.dart
|  |     |- prod.dart
|  |     |- uat.dart
|  |     |- uat.dart
|  |     |- sit.dart
|  |     
|  |- ▼ util // should only reusable item be put here
|  |  |- util.dart
|  |  |- ▼ ui 
|  |  |  |- dialogs.dart // example
|  |  |  |- buttons.dart // example
|  |  |  
|  |  |- ▼ services
|  |  |  |- ▼ session
|  |  |  |  |- session.dart
|  |  |  |- ▼ network
|  |  |  |  |- network.dart
|  |  |  |  |- http_service.dart
|  |  |  |  |- interceptor_service.dart
|  |  |  |  |- urls.dart
|  |  |  |  
|  |  |  |- ▼ data
|  |  |     |- data.dart // example
|  |  |     |- sql_lite_service.dart // example
|  |  |     |- shared_preferences_service.dart // example
|  |  |
|  |- ▼ modules
|  |  |- ▼ authentication
|  |  |  |- authentication.dart
|  |  |  |- screens
|  |  |  |- widgets
|  |  |  |- blocs
|  |  |  |- repository
|  |  |  |- models
|  |  |  |- ▼ utils
|  |  |     |- const // enums etc
|  |  |   
|  |  |- ▼ splash
|  |  |  |- splash.dart
|  |  |  |- screens
|  |  |  |- blocs
|  |  |  |- repository
|  |  |  |- models
|  |  |  |- ▼ utils
|  |  |     |- const 
|  |  |   
|  |  |- ▼ onboarding
|  |     |- // same as above
|  | 
|- ► web
|- ► ios
|- ► android
|- ► assets
|- ▼ i18n
|  |-  en.json
|
|- ▼ test
   |- ▼ test_util
   |  |- test_util.dart
   |  |- app.dart // to prep app to be testable as a widget
   |  |- mock.dart // all mock class
   |- test_widget
   |- test_integration
   |- ▼ test_unit
      |- ▼ bloc
      |- ▼ class_and_functions
```