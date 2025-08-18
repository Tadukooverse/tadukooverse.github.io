---
title: Tadukoo Util Alpha Changelog
project: TadukooUtil
version_range: Alpha
blurb: Tadukoo Util's Alpha changelog
changelog:
- version: Alpha v.0.4
  blurb: Dictionary and Java 16
  released: April 17, 2021 9:22 PM
  github: https://github.com/Tadukooverse/TadukooUtil/releases/tag/0.4-Alpha
  details: |
    ### Tadukoo Util
    #### Dictionary
    Created Dictionary, an interface used for storing and retrieving valid words.
    
    Also created AbstractDictionary and several implementations for the Standard Charsets.
    
    ### Technical/Other
    Updated to Java 16
- version: Alpha v.0.3.1
  blurb: Character Util and More String Utils
  released: February 6, 2021 5:29 PM
  github: https://github.com/Tadukooverse/TadukooUtil/releases/tag/v.0.3.1-Alpha
  details: | 
    ### Tadukoo Lang
    #### Character Util
    Created Character Util, a class with utility methods for dealing with characters.
    
    It includes the following methods:
    - isUpperCase
    - isLowerCase
    - isLetter
    - isNumber
    - toUpperCase
    - toLowerCase
    
    ### More String Util methods
    Methods were added to String Util to deal with different cases.
    
    The following methods were added:
    - isPascalCase
    - toPascalCase
    - isCamelCase
    - toCamelCase
    - isSnakeCase
    - toSnakeCase
    
    ### Technical/Other
    Removed Tadukoo View from dependency management
- version: Alpha v.0.3
  blurb: More Tadukoo Functions
  released: December 19, 2020 7:47 PM
  github: https://github.com/Tadukooverse/TadukooUtil/releases/tag/v.0.3-Alpha
  details: | 
    This release of Tadukoo Util contains some code cleanup and the addition of throwing functional interfaces with up to 10 parameters.
- version: Alpha v.0.2.2
  blurb: Reorganization
  released: December 13, 2020 8:39 PM
  github: https://github.com/Tadukooverse/TadukooUtil/releases/tag/v.0.2.2-Alpha
  details: | 
    This release of Tadukoo Util is an official release of the following modules (all of them):
    - Tadukoo Lang - provides common basic utilities such as StringUtil and Tuples
    - Tadukoo Functions - provides ThrowingFunctions, ThrowingPredicates, etc. for better use than Java's non-throwing versions
    - Tadukoo Util -  provides common utilities that are more advanced, such as MultiMap, ManyToManyMap, and pojo classes
    
    There are no code changes, other than removal of some classes in Tadukoo Util and moving of the throwing interfaces from Tadukoo Util to Tadukoo Functions.
    
    Note that the following modules have moved to other projects:
    - Tadukoo Annotation Processor - is now in [Tadukoo Annotations](/projects/TadukooAnnotations)
    - Tadukoo Database - is now called "Tadukoo MySQL" in [Tadukoo Database](/projects/TadukooDatabase)
    - Tadukoo File Format - is now in [Tadukoo Parsing](/projects/TadukooParsing)
    - Tadukoo Look & Feel - is now in [Tadukoo View](/projects/TadukooView)
    - Tadukoo View - was split into multiple modules in [Tadukoo View](/projects/TadukooView)
- version: Alpha v.0.2.1
  blurb: Fixes + Improvements
  released: December 12, 2020 7:28 PM
  github: https://github.com/Tadukooverse/TadukooUtil/releases/tag/v.0.2.1-alpha
  details: |
    This release represents the third release for Tadukoo Util, and is an official release of the following modules:
    - Tadukoo Annotation Processor - provides @AnnotationProcessor and AnnotationUtil for making Annotations
    - Tadukoo Lang - provides common basic utilities such as StringUtil and Tuples
    - Tadukoo Util - provides common utilities that are more advanced, such as MultiMap, ManyToManyMap, and Throwing Functional Interfaces
    - Tadukoo View - provides utilities for drawing items to the screen, and for building forms
    
    While the following modules are included, they should not be considered officially released with this release, and will be completed in future Alpha releases leading up to Beta. Use 
    them at your own risk, understanding they may change entirely.
    - Tadukoo Database - utilities for communicating with a SQL database
    - Tadukoo File Format - allows you to create your own file formats
    - Tadukoo Look & Feel - a customizable Look & Feel
    
    The first set of modules will be fully supported, while the second set will not. Tadukoo Util (the project) is in kind of a weird state at the moment, See 
    [the Tadukooverse Master Plan](/about/tadukooverse-master-plan.html) for more details on what's going on.
    
    Note that now Tadukoo Util releases are available from Maven Central.
    
    ### Tadukoo Util
    #### MappedPojo Constructors
    AbstractMappedPojo, AbstractOrderedMappedPojo, and AbstractForm now have constructors that take in a MappedPojo. When taking in the MappedPojo, they use its map to set their map values. 
    This can be used by subclasses to more easily cast to a subclass if needed, e.g.:
    ```
    MappedPojo pojo; // <- Pretend this is a pojo that already exists, and that it's an instance of AbstractMappedPojo
    PojoSubclass realPojo = new PojoSubclass(pojo); // <- PojoSubclass is a subclass of AbstractMappedPojo, and is using the new constructor to get the mapped values to easily turn pojo into a PojoSubclass
    ```
    
    This is also used in a new MappedPojo method - getPojoItem(String key, Class<T extends MappedPojo> clazz), which will convert the item to the proper pojo class if it's not already and store it in the 
    MappedPojo if a conversion happened.
    
    There's another new MappedPojo method for dealing with tables - getTableItem(String key, Class<T extends MappedPojo> clazz), which will convert the item into a proper Table with T items instead of 
    generic MappedPojos (that are added to the Table by some methods)
    #### Time Utils
    Created DateUtil and MonthUtil with utilty methods for dealing with Dates and Months, respectively.
    ### Tadukoo View
    #### Sizable Paint
    SizablePaint is a new interface used as a general class to hold a SizablePaint. It has a single method: getPaint(Dimension size), used to create classes for general paints that can 
    vary by size.
    
    SizableColor was created as a simple SizablePaint that's just a solid color. This is used for places where SizablePaint is needed, but you just want a solid color instead.
    
    Gradient now extends SizablePaint (doesn't change Gradient's getPaint method or anything like that, just now it is a SizablePaint).
    
    Gradient classes were moved to a different subpackage (now in com.github.tadukoo.util.view.paint.gradient)
    
    PaintUIResource is now an extension of SizablePaint (again, no change to its getPaint method, just now it is a SizablePaint).
    
    TadukooButtonUI is now expecting a SizablePaint to be used to paint, instead of a PaintUIResource. This is because PaintUIResource is meant only for default UI settings, and not for 
    general use (such as being contained in a button class as it will be eventually).
    
    ShapedBevelBorder, ShapedLineBorder, and ShapedEtchedBorder now use SizablePaint instead of PaintUIResource.
    
    #### Shaped Borders Moved
    ShapedBevelBorder, ShapedLineBorder, and ShapedEtchedBorder were moved from Tadukoo Look & Feel to Tadukoo View. This is so you can set borders on the custom components in Tadukoo View 
    without requiring Tadukoo Look & Feel.
    
    #### Gradient Changes
    Gradient now has methods for getting the cycleMethod, colorSpace, and gradientTransform values, and LinearGradient and RadialGradient have methods for getting their specific parameters.
    
    GradientUIResource has the methods for cycleMethod, colorSpace, and gradientTransform as well.
    
    GradientBuilder now has a type parameter for what type of Gradient it returns when building, so you don't have to cast it.
    
    #### Date Form
    Created DateForm, a Form that uses a drop-down menu for month and integer JSpinners for day and year
    
    #### New Form Fields
    ##### Number Form Fields
    Created NumberFormField, which uses JSpinner to display a number. It takes minValue, maxValue, and stepSize for the spinner model to use.
    
    It has implementations for Integers, Shorts, Longs, Floats, and Doubles.
    
    ##### Date Form Field
    Date Form Field is a form field that uses the new Date Form to display a Date. It takes in minYear and maxYear for the Date Form to use.
    
    ### Bug Fixes
    Gradients actually work now (previously building them caused a NullPointerException).
    
    ### JUnit Testing
    New JUnit tests for FontFamily and FontFamilies
    
    New JUnit tests for LinearGradient and RadialGradient
    
    New JUnit tests for Orientation
    
    ### Technical/Other
    Updated JUnit dependencies to the latest
    
    Leckerli One font is now using the TTF constant instead of hard-coding "ttf"
    
    Updated to Java 15 and no longer use preview features
- version: Alpha v.0.2
  blurb: Complete Tadukoo View
  released: November 7, 2020 9:07 PM
  github: https://github.com/Tadukooverse/TadukooUtil/releases/tag/v.0.2-Alpha
  details: |
    - The main changes with this release are in Tadukoo View, but there were additions to Tadukoo Lang and Tadukoo Util as well
    - This release represents the second release for Tadukoo Util and is an official release of the following modules:
      - Tadukoo Annotation Processor - provides @AnnotationProcessor and AnnotationUtil for making Annotations
      - Tadukoo Lang - provides common basic utilities such as StringUtil and Tuples
      - Tadukoo Util - provides common utilities that are more advanced, such as MultiMap, ManyToManyMap, and Throwing Functional Interfaces
      - Tadukoo View - provides utilities for drawing items to the screen, and for building forms
    - While the following modules are included, they should not be considered officially released with this release, and will be completed in future Alpha releases leading up to Beta. 
    Use them at your own risk, understanding they may change entirely.
      - Tadukoo Database - utilities for communicating with a SQL database
      - Tadukoo File Format - allows you to create your own file formats
      - Tadukoo Look & Feel - a customizable Look & Feel
    
    The first set of modules will be fully supported, while the second set will not. Tadukoo Util (the project) is in kind of a weird state at the moment, See 
    [the Tadukooverse Master Plan](/about/tadukooverse-master-plan.html) for more details on what's going on.
    
    This version is now deployed to Maven Central.
- version: Alpha v.0.1
  blurb: Finish Up Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util
  released: September 5, 2020 8:01 PM
  github: https://github.com/Tadukooverse/TadukooUtil/releases/tag/v.0.1-alpha
  details: |
    - This release represents the first release for Tadukoo Util of the following modules:
      - Tadukoo Annotation Processor - provides @AnnotationProcessor and AnnotationUtil for making Annotations
      - Tadukoo Lang - provides common basic utilities such as StringUtil and Tuples
      - Tadukoo Util - provides common utilities that are more advanced, such as MultiMap, ManyToManyMap, and Throwing Functional Interfaces
    - While the following modules are included, they should not be considered officially released with this release, and will be completed in future Alpha releases leading up to Beta. 
    Use them at your own risk, understanding they may change entirely.
      - Tadukoo Database - utilities for communicating with a SQL database
      - Tadukoo File Format - allows you to create your own file formats
      - Tadukoo Look & Feel - a customizable Look & Feel
      - Tadukoo View - common view utilities
    
    The first set of modules will be fully supported, while the second set will not. Tadukoo Util (the project) is in kind of a weird state at the moment, See 
    [the Tadukooverse Master Plan](/about/tadukooverse-master-plan.html) for more details on what''s going on.
    
    Due to some weird things going on with the plan, this version has the version string 0.1-Alpha-SNAPSHOT for the purposes of Maven, and will only be available in the snapshots 
    repository of Maven Central, and not in the official releases repository. Also, this is why the jars themselves have "-SNAPSHOT" in them.
---