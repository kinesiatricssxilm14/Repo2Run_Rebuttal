# Repo2Run_Rebuttal

Table 1: Analysis of 382 failed cases of SWE-agent. "Configure fail" indicates the number of failures during configuration within the Docker container. The latter three cases indicate that the configuration within the Docker container was successful, but the generated Dockerfile was incorrect. "Path error" represents the use of incorrect paths in the Dockerfile; "Dependency error" represents errors in dependency management within the Dockerfile; "Other Error" indicates other types of errors, such as missing environment variables.

| **Configure fail** | **Path error** | **Dependency Error** | **Other Error** |
|----------|----------|----------|----------|
| 79(20.7%) | 170(44.5%) | 117(30.6%) | 16(4.2%) |


Table 2: Language Support for Repo2Run Framework. The table below illustrates the various programming languages that can be supported by the Repo2Run framework by adjusting the base image and installation tools. This flexibility showcases the framework's capability to adapt to multiple languages, beyond just Python.
| **Programming language**      | **Docker base image**                 | **Installation tool**                    |
|---------------|--------------------------|-----------------------------|
| Python        | python:[version]         | pip                         |
| JavaScript/TypeScript    | node:[version]| npm                         |
| Ruby          | ruby:[version]           | bundler                     |
| Java          | OpenJDK:[version]        | maven                       |
| R             | r-base:[version]         | install.packages            |
| Go            | golang:[version]         | go get                      |
| PHP           | php:[version]            | composer                    |
| C/C++         | gcc:[version]            | custom build scripts        |
| Rust          | rust:[version]           | cargo                       |

Table 3: 
| **Configuration state** | **#LOC > 10,000** | **#LOC > 100,000** | **Medium** | **Max** |
|----------|----------|----------|----------|----------|
| Success(361) | 220(60.9%) | 27(7.5%) |----------|----------|
| Fail(59) | 50(84.7%) | 12(30.6%) |----------|----------|
| All(420) | 270(64.3%) | 39(20.3%) |----------|----------|
| requests(reference) | - | - |12782|12782|
| scrapy(reference) | - | - |77278|77278|
