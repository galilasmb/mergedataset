 ## 1. Clone the project 
    git clone https://github.com/spring-projects/spring-boot.git

## 2. Checkout to merge the commit hash
    git checkout -f 074771ec125dd407af0282b92960e9e9e3377e84

## 3. Open the parent directory (spring-boot/spring-boot-parent/pom.xml) and change all the urls:
```xml
    http://repo.spring.io change to https://repo.spring.io
```

## 4. Change the version from 1.3.0.BUILD-SNAPSHOT to 1.3.0.RELEASE in spring-boot/spring-boot-parent/pom.xml and in spring-boot/spring-boot/pom.xml.

## 5. Inside the folder spring-boot run the command:
```xml
    mvn clean compile package -Dmaven.compiler.failOnError=false -DskipTests jar:test-jar
```

## 6. Check the content folder: 
    spring-boot/spring-boot/target
