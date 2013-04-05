java-coding-style
=================
Add the following to your pom.xml after downloading the git repo and running 'maven install'.

```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-checkstyle-plugin</artifactId>
    <version>2.6</version>
    <configuration>
        <configLocation>org/codequality/checkstyle.xml</configLocation>
        <consoleOutput>true</consoleOutput>
        <enableRulesSummary>false</enableRulesSummary>
        <failsOnError>true</failsOnError>
        <includeTestSourceDirectory>true</includeTestSourceDirectory>
    </configuration>
    <executions>
         <execution>
             <phase>validate</phase>
             <goals>
                 <goal>checkstyle</goal>
             </goals>
         </execution>
     </executions>
     <dependencies>
         <dependency>
             <groupId>org.codequality</groupId>
             <artifactId>java-code-quality</artifactId>
             <version>1.1-SNAPSHOT</version>
         </dependency>
     </dependencies>
</plugin>
```
