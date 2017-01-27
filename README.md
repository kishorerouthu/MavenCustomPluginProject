# MavenCustomPluginProject

This project demonstrate how to use the maven custom plugin.
Here the configuration of hello-maven-plugin in pom xml.

  <build>
    <plugins>
      <plugin>
        <groupId>com.tutorial.maven.plugin</groupId>
        <artifactId>hello-maven-plugin</artifactId>
        <version>1.0</version>
        <configuration>
          <greeting>Welcome hello-world-plugin...! ${pom.artifactId}</greeting>
        </configuration>
        <executions>
          <execution>
            <phase>install</phase>
            <goals>
              <goal>sayhi</goal>
            </goals>
          </execution>
        </executions>
      </plugin>
    </plugins>
  </build>
Points to consider :

- greeting is the message the we wanted to print by the plugin
- goal is the name that we given to the mojo
- phase @which this plugin execute method is going to be invoked
