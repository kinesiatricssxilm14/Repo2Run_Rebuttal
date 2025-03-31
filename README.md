# Repo2Run_Rebuttal

Table 1: Analysis of 382 failed cases of SWE-agent. "Configure fail" indicates the number of failures during configuration within the Docker container. The latter three cases indicate that the configuration within the Docker container was successful, but the generated Dockerfile was incorrect. "Path error" represents the use of incorrect paths in the Dockerfile; "Dependency error" represents errors in dependency management within the Dockerfile; "Other Error" indicates other types of errors, such as missing environment variables.

| **Configure fail** | **Path error** | **Dependency Error** | **Other Error** |
|----------|----------|----------|----------|
| 79(20.7%) | 170(44.5%) | 117(30.6%) | 16(4.2%) |


Table 2: 
| Programming language      | Docker base image                 | installation tool                    |
|---------------|--------------------------|-----------------------------|
| Python        | python:[version]         | pip                         |
| JavaScript/TypeScript    | node:[version]           | npm / yarn                  |
| Ruby          | ruby:[version]           | bundler                     |
| Java          | OpenJDK:[version]        | maven / gradle              |
| R             | r-base:[version]         | install.packages            |
| Go            | golang:[version]         | go get                      |
| PHP           | php:[version]            | composer                    |
| C++           | gcc:[version]            | custom build scripts        |
| Rust          | rust:[version]           | cargo                       |
