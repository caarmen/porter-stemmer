Porter Stemmer
==============

This library provides an implementation of the Porter stemming algorithm, defined here:
http://tartarus.org/martin/PorterStemmer/def.txt
This implementation has not been tuned for high performance on large amounts of text. It is
a simple (naive perhaps) implementation of the rules.

Command-line program:
--------------------
To test out the library on the command-line:

```
    ./gradlew clean cliJar
    cat /path/to/file.txt | java -jar example/build/libs/example-all-1.0.0.jar 
```

Using the library:
-----------------
The library is available on jcenter. To include the library in your project:

maven:

```
<dependency>
  <groupId>ca.rmen</groupId>
  <artifactId>porter-stemmer</artifactId>
  <version>1.0.0</version>
</dependency>
```

gradle:

```
compile 'ca.rmen:porter-stemmer:1.0.0'
```

To use the stemmer:
```java
PorterStemmer porterStemmer = new PorterStemmer();
String stem = porterStemmer.stemWord("incorporated"); // returns "incorpor"
```
