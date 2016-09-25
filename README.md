# DYAML: Dynamic YAML for Scala
![DYAML Logo](https://github.com/dmoliveira/dyaml/blob/master/.img/dyml.png)

**Author:** [Oliveira, D.M](https://br.linkedin.com/in/dmztheone);

## Introduction
DYAML is a dynamic YAML reader for Scala. Load on-the-fly YAML files to Map objects without need to create case classes.

## Install
For now, you can add DYAML to our project adding the following configuration to your ```project/Build.scala``` file:
```
import sbt._

object MyBuild extends Build {
  lazy val root = Project("root", file("."))
                    .dependsOn(dyaml)

  lazy val dyaml = RootProject(uri("git://github.com/dmoliveira/dyaml.git"))
}
```

## Example
#### Read filenames or ```java.io.InputStream```

Supose that we have this YAML file:

```
settings:
    name: base_settings
    enabled: true
    ...
```

We could read it using these steps:  
  1. Import the package
  ```
  import scala.dynamic.DYaml
  ```

  2. Read the data
  ```
  var example = DYaml.loadYAML("example.yml")
  ```

  3. Access object values  loaded from YAML
  ```
  println(example.name)
  println(example.enabled)
  ```

## Resources
This library is based on ```Fun with Scala Dynamic, macros and Yaml``` made by [xrrocha](https://github.com/xrrocha/sdynamic). It's only was adjusted for general purpose.  

## License
Apache License version 2.0, 2004 - [http://www.apache.org/licenses/](http://www.apache.org/licenses/)
