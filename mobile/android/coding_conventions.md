## Coding conventions for Android app or library

### Project structure
```
 |  
 |- models
 |- api
 |-- Urls.java // this file contains all the static urls and a method called getBaseUrl() required in case of multiple env
 |- utils // all the code that is being used across the application
 |- adapters // contains all the list adapters
 |- views
 |-- compoents // contains all the custom visual components
 |-- fragments
 |-- activities
 |- Applicaiton.Java
 ```

### Some base classes that we use

#### IListAdapter , BaseListAdapter
