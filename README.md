# 🥞 &nbsp; flutter-core-structure

```
👨‍🍳  This is a living document and might need an update when the time is come.
```

## 🧠 &nbsp; Thing should be considered:

- Scalability
- Collaboration
- Testability

</br>

## 🚀 &nbsp; I decide to go with [folder by feature](https://softwareengineering.stackexchange.com/questions/338597/folder-by-type-or-folder-by-feature) approach.

</br>

## 📁 &nbsp; Folder structure


```
|- ▼ lib
|  |- main.dart
|  |- app.dart // combine all config and util 
|  |- ▼ config // app specific
|  |  |- ▼ theme
|  |  |  |- dark.dart
|  |  |  |- light.dart
|  |  |  |- colors.dart
|  |  |  
|  |  |- ▼ route
|  |  |  |- route_guard.dart
|  |  |  |- routes.dart
|  |  |  
|  |  |- ▼ environment
|  |     |- prod.dart
|  |     |- uat.dart
|  |     |- uat.dart
|  |     |- sit.dart
|  |     
|  |- ▼ util // should only reusable item be put here
|  |  |- ▼ ui 
|  |  |  |- dialogs.dart // example
|  |  |  |- buttons.dart // example
|  |  |  
|  |  |- ▼ services
|  |     |- ▼ session
|  |     |  |- session.dart
|  |     |
|  |     |- ▼ translation
|  |     |  |- translation.dart
|  |     |  
|  |     |- ▼ network
|  |     |  |- ▼ http 
|  |     |  |  |- http_service.dart
|  |     |  |  |- interceptor_service.dart
|  |     |  |  |- urls.dart
|  |     |  |
|  |     |  |- ▼ GraphQL
|  |     |     |- query.dart
|  |     |     |- interceptor_service.dart
|  |     |     |- urls.dart
|  |     |  
|  |     |- ▼ data
|  |        |- firestore.dart // example
|  |        |- sql_lite_service.dart // example
|  |        |- shared_preferences_service.dart // example
|  |   
|  |- ▼ modules
|     |- ▼ authentication
|     |  |- presentation // screen, view or page
|     |  |- widgets
|     |  |- blocs
|     |  |- repository
|     |  |- models
|     |  |- ▼ utils
|     |     |- const // enums etc
|     |   
|     |- ▼ splash
|     |  |- presentation // screen, view or page
|     |  |- blocs
|     |  |- repository
|     |  |- models
|     |  |- ▼ utils
|     |     |- const 
|     |   
|     |- ▼ onboarding
|        |- // same as above
|    
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
   | 
   |- test_widget
   |- test_integration
   |- ▼ test_unit
      |- ▼ bloc
      |- ▼ class_and_functions
```
