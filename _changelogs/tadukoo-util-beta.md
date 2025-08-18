---
title: Tadukoo Util Beta Changelog
project: TadukooUtil
version_range: Beta
blurb: Tadukoo Util's Beta changelog
changelog:
- version: Beta v.0.6.1
  blurb: Small Dependency Changes
  released: August 30, 2024 7:52 PM
  github: 
  details: | 
    * Updated Tadukoo Maven to Beta v.0.5
    * Small change in StringUtil for strings when using convertToString
    * Tadukoo Util now also uses Tadukoo Functions as a dependency
- version: Beta v.0.6
  blurb: Tadukoo JUnit and Other Changes
  released: August 31, 2023 8:00 PM
  github: https://github.com/Tadukooverse/TadukooUtil/releases/tag/0.6-Beta
  details: | 
    ### Tadukoo Lang
    * FileUtil Changes
      * FileUtil method to writeFile using byte array
      * listAllFilesAsPaths Methods in FileUtil
      * deleteFile and deleteDirectory in FileUtil
    * StringUtil Changes
      * More StringUtil methods
      * parseListFromStringWithRegex Method in StringUtil
      * Null-Safe Trim Method in StringUtil
      * StringUtil allBlank, noneBlank, anyBlank, and anyNotBlank
      * StringUtil.indentAllLines
    * MergeSets and MergeLists Methods
    * CollectionUtil
    * SetUtil
    * SetUtil createOrderedSet and mergedOrderedSets
    * Equals Methods for Tuples
    
    ### Tadukoo Functions
    * ThrowingSelfFunction
    
    ### Tadukoo Util
    * StackUtil
    * EasyLogger to use StackUtil
    * Basic Util Classes for Parallel Functionality
    * DownloadUtil
    
    ### Tadukoo JUnit
    * More Useful Logger Entry Comparisons
    * EnumTest
    * Better Errors in Failed Tests
    * Move Tadukoo JUnit here as a new module
- version: Beta v.0.5.1
  blurb: Java 17
  released: November 19, 2021 9:52 PM
  github: https://github.com/Tadukooverse/TadukooUtil/releases/tag/0.5.1-Beta
  details: | 
    * Updated to Tadukoo Maven Alpha v.0.3.1 (for Java 17 and dependency updates)
- version: Beta v.0.5
  blurb: ByteUtil and Other Changes
  released: July 5, 2021 7:33 PM
  github: https://github.com/Tadukooverse/TadukooUtil/releases/tag/0.5-Beta
  details: |
    ### Tadukoo Lang
    #### File Util
    New methods:
    * BufferedReader setupFileReader(String filepath)
    * BufferedReader setupFileReader(File file)
    * boolean exists(String filepath)
    * boolean exists(File file)
    * boolean notExists(String filepath)
    * boolean notExists(File file)
    * String readAsString(String filepath)
    * String readAsString(File file)
    * List<String> readLinesAsList(String filepath)
    * List<String> readLinesAsList(File file)
    * List<String> getLinesAsList renamed to readLinesAsList(Reader reader)
    * byte[] readAsBytes(String filepath)
    * byte[] readAsBytes(File file)
    
    #### Byte Util
    Completely new
    
    ### Tadukoo Util
    #### Added ProgressReadableByteChannel and ProgressRBCWrapper
    Used to track progress on a download/file read
    
    #### Removed Table
    It was just a List anyway
    
    #### Mapped Pojo
    New methods:
    * boolean isEmpty()
    * void clear()
    * <T extends MappedPojo> T getPojoItemNoThrow(String key, Class<T> clazz)
    * <T extends MappedPojo> T getPojoItemNoThrow(EasyLogger logger, String key, Class<T> clazz)
    * <T extends MappedPojo> List<T> getListItemNoThrow(String key, Class<T> clazz)
    * <T extends MappedPojo> List<T> getListItemNoThrow(EasyLogger logger, String key, Class<T> clazz)
    
    ### Other/Technical
    * Now using Tadukoo Maven Library POM as a parent pom - Alpha v.0.3 of it
---
