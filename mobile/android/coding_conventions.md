## Coding conventions for Android app or library

### Naming conventions

| Identifier Type | Naming Convention                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Example                                                                                             |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| Packages        | The prefix of a unique package name is always written in all-lowercase ASCII letters and should be one of the top-level domain names, currently com, edu, gov, mil, net, org, or one of the English two-letter codes identifying countries as specified in ISO Standard 3166, 1981.Subsequent components of the package name vary according to an organization's own internal naming conventions. Such conventions might specify that certain directory name components be division, department, project, machine, or login names.                                                                                                                  | com.sun.eng com.apple.quicktime.v2 edu.cmu.cs.bovik.cheese                                          |
| Classes         | Class names should be nouns, in mixed case with the first letter of each internal word capitalized. Try to keep your class names simple and descriptive. Use whole words-avoid acronyms and abbreviations (unless the abbreviation is much more widely used than the long form, such as URL or HTML).                                                                                                                                                                                                                                                                                                                                               | class Raster;  class ImageSprite;                                                                   |
| Interfaces      | Interface names should be capitalized like class names.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | interface RasterDelegate;  interface Storing;                                                       |
| Methods         | Methods should be verbs, in mixed case with the first letter lowercase, with the first letter of each internal word capitalized.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | run();  runFast();  getBackground();                                                                |
| Variables       | Except for variables, all instance, class, and class constants are in mixed case with a lowercase first letter. Internal words start with capital letters. Variable names should not start with underscore _ or dollar sign $ characters, even though both are allowed.Variable names should be short yet meaningful. The choice of a variable name should be mnemonic- that is, designed to indicate to the casual observer the intent of its use. One-character variable names should be avoided except for temporary "throwaway" variables. Common names for temporary variables are i, j, k, m, and n for integers; c, d, and e for characters. | int i;  char c;  float myWidth;                                                                     |
| Constants       | The names of variables declared class constants and of ANSI constants should be all uppercase with words separated by underscores ("_"). (ANSI constants should be avoided, for ease of debugging.)                                                                                                                                                                                                                                                                                                                                                                                                                                                 | static final int MIN_WIDTH = 4; static final int MAX_WIDTH = 999; static final int GET_THE_CPU = 1; |

#### Sequence of code blocks
The following table describes the parts of a class or interface declaration, in the order that they should appear. See "Java Source File Example" on page 19 for an example that includes comments.[link](http://www.oracle.com/technetwork/java/codeconventions-141855.html#1852)

1. Class/interface documentation comment ( /*.../)
2. Class or interface statement
3. Class/interface implementation comment ( /.../), if necessary
4. Class (static) variables
5. Instance variables
6. Constructors
7. Methods
 



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
