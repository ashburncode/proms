I used https://start.spring.io/ to create a new Spring Boot application named proms, and downloaded the corresponding proms.zip file.

Spring Initializr
https://start.spring.io/

Group:         com.ashburncode
Artifact:      proms
Name:          proms
Package name:  com.ashburncode.proms
Description:   spring boot 2.7.17, gradle project, jar packaging, java 8
Dependencies:
  Spring Web Web
    Build web, including RESTful, applications using Spring MVC. Uses Apache Tomcat as the default embedded container.
  Spring Data JPA SQL
    Persist data in SQL stores with Java Persistence API using Spring Data and Hibernate.
  Rest Repositories Web
    Exposing Spring Data repositories over REST via Spring Data REST.
  MySQL Driver SQL
    MySQL JDBC driver.
  Spring Security Security
    Highly customizable authentication and access-control framework for Spring applications.
  Lombok Developer Tools
    Java annotation library which helps to reduce boilerplate code.
  Spring Boot DevTools Developer Tools
    Provides fast application restarts, LiveReload, and configurations for enhanced development experience.
  Spring Configuration Processor Developer Tools
    Generate metadata for developers to offer contextual help and "code completion" when working with custom configuration keys (ex.application.properties/.yml files).
  H2 Database SQL
    Provides a fast in-memory database that supports JDBC API and R2DBC access, with a small (2mb) footprint. Supports embedded and server modes as well as a browser based console application.
  Spring Boot Actuator Ops
    Supports built in (or custom) endpoints that let you monitor and manage your application - such as application health, metrics, sessions, etc.

davidho@dphxps17:~/sbootprojs$ 
davidho@dphxps17:~/sbootprojs$ ls -latr ~/Downloads/prom*
-rw-rw-r-- 1 davidho davidho 71373 Oct 15 11:20 /home/davidho/Downloads/proms2716g17.zip
-rw-rw-r-- 1 davidho davidho 71395 Nov 17 08:39 /home/davidho/Downloads/proms.zip
davidho@dphxps17:~/sbootprojs$ mv proms proms2716g17
davidho@dphxps17:~/sbootprojs$ 
davidho@dphxps17:~/sbootprojs$ 7z l proms.zip

7-Zip [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21
p7zip Version 16.02 (locale=en_US.UTF-8,Utf16=on,HugeFiles=on,64 bits,16 CPUs 11th Gen Intel(R) Core(TM) i7-11800H @ 2.30GHz (806D1),ASM,AES-NI)

Scanning the drive for archives:
1 file, 71395 bytes (70 KiB)

Listing archive: proms.zip

--
Path = proms.zip
Type = zip
Physical Size = 71395

   Date      Time    Attr         Size   Compressed  Name
------------------- ----- ------------ ------------  ------------------------
2023-11-17 08:38:08 D....            0            2  proms
2023-11-17 08:38:08 .....         2590          782  proms/HELP.md
2023-11-17 08:38:08 .....         2868         1211  proms/gradlew.bat
2023-11-17 08:38:08 .....          444          242  proms/.gitignore
2023-11-17 08:38:08 D....            0            2  proms/src
2023-11-17 08:38:08 D....            0            2  proms/src/main
2023-11-17 08:38:08 D....            0            2  proms/src/main/java
2023-11-17 08:38:08 D....            0            2  proms/src/main/java/com
2023-11-17 08:38:08 D....            0            2  proms/src/main/java/com/ashburncode
2023-11-17 08:38:08 D....            0            2  proms/src/main/java/com/ashburncode/proms
2023-11-17 08:38:08 .....          312          170  proms/src/main/java/com/ashburncode/proms/PromsApplication.java
2023-11-17 08:38:08 D....            0            2  proms/src/main/resources
2023-11-17 08:38:08 D....            0            2  proms/src/main/resources/templates
2023-11-17 08:38:08 D....            0            2  proms/src/main/resources/static
2023-11-17 08:38:08 .....            1            3  proms/src/main/resources/application.properties
2023-11-17 08:38:08 D....            0            2  proms/src/test
2023-11-17 08:38:08 D....            0            2  proms/src/test/java
2023-11-17 08:38:08 D....            0            2  proms/src/test/java/com
2023-11-17 08:38:08 D....            0            2  proms/src/test/java/com/ashburncode
2023-11-17 08:38:08 D....            0            2  proms/src/test/java/com/ashburncode/proms
2023-11-17 08:38:08 .....          212          151  proms/src/test/java/com/ashburncode/proms/PromsApplicationTests.java
2023-11-17 08:38:08 D....            0            2  proms/gradle
2023-11-17 08:38:08 D....            0            2  proms/gradle/wrapper
2023-11-17 08:38:08 .....          250          152  proms/gradle/wrapper/gradle-wrapper.properties
2023-11-17 08:38:08 .....        63721        57558  proms/gradle/wrapper/gradle-wrapper.jar
2023-11-17 08:38:08 .....           27           29  proms/settings.gradle
2023-11-17 08:38:08 .....         1300          479  proms/build.gradle
2023-11-17 08:38:08 .....         8692         3688  proms/gradlew
------------------- ----- ------------ ------------  ------------------------
2023-11-17 08:38:08              80417        64499  11 files, 17 folders
davidho@dphxps17:~/sbootprojs$ 
davidho@dphxps17:~/sbootprojs$ 7z x proms.zip

7-Zip [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21
p7zip Version 16.02 (locale=en_US.UTF-8,Utf16=on,HugeFiles=on,64 bits,16 CPUs 11th Gen Intel(R) Core(TM) i7-11800H @ 2.30GHz (806D1),ASM,AES-NI)

Scanning the drive for archives:
1 file, 71395 bytes (70 KiB)

Extracting archive: proms.zip
--
Path = proms.zip
Type = zip
Physical Size = 71395

Everything is Ok

Folders: 17
Files: 11
Size:       80417
Compressed: 71395
davidho@dphxps17:~/sbootprojs$ 
davidho@dphxps17:~/sbootprojs$ cd proms
davidho@dphxps17:~/sbootprojs/proms$ 
davidho@dphxps17:~/sbootprojs/proms$ ls -latr
total 48
drwxr-xr-x  4 davidho davidho 4096 Nov 17 08:38 src
-rw-r--r--  1 davidho davidho   27 Nov 17 08:38 settings.gradle
-rw-r--r--  1 davidho davidho 2590 Nov 17 08:38 HELP.md
-rw-r--r--  1 davidho davidho 2868 Nov 17 08:38 gradlew.bat
-rwxr-xr-x  1 davidho davidho 8692 Nov 17 08:38 gradlew
drwxr-xr-x  3 davidho davidho 4096 Nov 17 08:38 gradle
-rw-r--r--  1 davidho davidho  444 Nov 17 08:38 .gitignore
-rw-r--r--  1 davidho davidho 1300 Nov 17 08:38 build.gradle
drwxr-xr-x  4 davidho davidho 4096 Nov 17 08:38 .
drwxrwxr-x 28 davidho davidho 4096 Nov 17 08:52 ..
davidho@dphxps17:~/sbootprojs/proms$ 
davidho@dphxps17:~/sbootprojs/proms$ tree
.
├── build.gradle
├── gradle
│   └── wrapper
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── gradlew
├── gradlew.bat
├── HELP.md
├── settings.gradle
└── src
    ├── main
    │   ├── java
    │   │   └── com
    │   │       └── ashburncode
    │   │           └── proms
    │   │               └── PromsApplication.java
    │   └── resources
    │       ├── application.properties
    │       ├── static
    │       └── templates
    └── test
        └── java
            └── com
                └── ashburncode
                    └── proms
                        └── PromsApplicationTests.java

16 directories, 10 files
davidho@dphxps17:~/sbootprojs/proms$ 
davidho@dphxps17:~/sbootprojs/proms$ ./gradlew --version
Downloading https://services.gradle.org/distributions/gradle-8.4-bin.zip
............10%............20%.............30%............40%.............50%............60%.............70%............80%.............90%............100%

Welcome to Gradle 8.4!

Here are the highlights of this release:
 - Compiling and testing with Java 21
 - Faster Java compilation on Windows
 - Role focused dependency configurations creation

For more details see https://docs.gradle.org/8.4/release-notes.html


------------------------------------------------------------
Gradle 8.4
------------------------------------------------------------

Build time:   2023-10-04 20:52:13 UTC
Revision:     e9251e572c9bd1d01e503a0dfdf43aedaeecdc3f

Kotlin:       1.9.10
Groovy:       3.0.17
Ant:          Apache Ant(TM) version 1.10.13 compiled on January 4 2023
JVM:          17.0.8.1 (Azul Systems, Inc. 17.0.8.1+1-LTS)
OS:           Linux 6.2.0-36-generic amd64

davidho@dphxps17:~/sbootprojs/proms$ 
davidho@dphxps17:~/sbootprojs/proms$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint: 	git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint: 	git branch -m <name>
Initialized empty Git repository in /home/davidho/sbootprojs/proms/.git/
davidho@dphxps17:~/sbootprojs/proms$ 
davidho@dphxps17:~/sbootprojs/proms$ git add .
davidho@dphxps17:~/sbootprojs/proms$ git commit -a -m "first commit"
[master (root-commit) 8f27fdd] first commit
 10 files changed, 459 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 build.gradle
 create mode 100644 gradle/wrapper/gradle-wrapper.jar
 create mode 100644 gradle/wrapper/gradle-wrapper.properties
 create mode 100755 gradlew
 create mode 100644 gradlew.bat
 create mode 100644 settings.gradle
 create mode 100644 src/main/java/com/ashburncode/proms/PromsApplication.java
 create mode 100644 src/main/resources/application.properties
 create mode 100644 src/test/java/com/ashburncode/proms/PromsApplicationTests.java
davidho@dphxps17:~/sbootprojs/proms$ 
davidho@dphxps17:~/sbootprojs/proms$ ./gradlew dependencies > proms-dependencies-20231117.txt
davidho@dphxps17:~/sbootprojs/proms$ grep "dependencies\|classpath" proms-dependencies-20231117.txt
> Task :dependencies
annotationProcessor - Annotation processors and their dependencies for source set 'main'.
No dependencies
compileClasspath - Compile classpath for source set 'main'.
compileOnly - Compile-only dependencies for the 'main' feature. (n)
No dependencies
developmentOnly - Configuration for development-only dependencies such as Spring Boot's DevTools.
implementation - Implementation dependencies for the 'main' feature. (n)
No dependencies
runtimeClasspath - Runtime classpath of source set 'main'.
No dependencies
runtimeOnly - Runtime-only dependencies for the 'main' feature. (n)
testAnnotationProcessor - Annotation processors and their dependencies for source set 'test'.
No dependencies
testCompileClasspath - Compile classpath for source set 'test'.
testCompileOnly - Compile only dependencies for source set 'test'. (n)
No dependencies
testImplementation - Implementation only dependencies for source set 'test'. (n)
testRuntimeClasspath - Runtime classpath of source set 'test'.
testRuntimeOnly - Runtime only dependencies for source set 'test'. (n)
No dependencies
davidho@dphxps17:~/sbootprojs/proms$ 

git remote add origin git@github.com:ashburncode/proms.git
git branch -M main
git push -u origin main


