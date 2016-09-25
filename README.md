# DYAML: Dynamic YAML for Scala

<img src="https://github.com/dmoliveira/dyaml/blob/master/.img/dyml.png" width="250px"/><br/>
[![GitHub version](https://badge.fury.io/gh/dmoliveira%2Fdyaml.svg)](https://badge.fury.io/gh/dmoliveira%2Fdyaml)
[![Build Status](https://travis-ci.org/dmoliveira/dyaml.svg?branch=master)](https://travis-ci.org/dmoliveira/dyaml)
[![Join the chat at https://gitter.im/dmoliveira/dyaml](https://badges.gitter.im/dmoliveira/dyaml.svg)](https://gitter.im/dmoliveira/dyaml?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badge/)

**Author:** [Oliveira, D.M](https://br.linkedin.com/in/dmztheone)

## Introduction
DYAML is a dynamic YAML reader for Scala. Load on-the-fly YAML files to Map objects without need to create case classes.

## Install
For now, you can add this follow line in your ```build.sbt``` project file:
```
.dependsOn(RootProject(uri("git://github.com/dmoliveira/dyaml.git")))
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
