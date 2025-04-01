# Repo2Run_Rebuttal

Table 1: Analysis of 382 failed cases of SWE-agent. "Configure fail" indicates the number of failures during configuration within the Docker container. The latter three cases indicate that the configuration within the Docker container was successful, but the generated Dockerfile was incorrect. "Path error" represents the use of incorrect paths in the Dockerfile; "Dependency error" represents errors in dependency management within the Dockerfile; "Other Error" indicates other types of errors, such as missing environment variables.

| **Configure fail** | **Path error** | **Dependency Error** | **Other Error** |
|----------|----------|----------|----------|
| 79(20.7%) | 170(44.5%) | 117(30.6%) | 16(4.2%) |

Table 2: Language Support for Repo2Run Framework. It illustrates the various programming languages that can be supported by the Repo2Run framework by adjusting the base image and installation tools. This flexibility showcases the framework's capability to adapt to multiple languages, beyond just Python.
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

Table 3: Data Table for Different Fields. We classify repositories in the following categories as ML/AI repositories: "Artificial Intelligence", "Reinforcement Learning", "Machine Learning", "Deep Learning", and "Large Language Models". The count of ML/AI repositories is 204 (48.57%).
| Type                  | Count | Type                  | Count |
|---------------------------|------|---------------------------|------|
| Artificial Intelligence   | 1    | Reinforcement Learning    | 6    |
| Mobile Security           | 1    | Cybersecurity             | 7    |
| Video Generation          | 1    | Big Data Processing       | 7    |
| Operating System          | 1    | Network Programming       | 7    |
| Backend Development       | 1    | Testing Framework         | 7    |
| DevOps                    | 2    | Machine Learning          | 9    |
| Mobile Development        | 2    | Web Framework             | 10   |
| Continuous Integration    | 2    | Data Visualization        | 11   |
| Data Processing           | 3    | Robotics                  | 17   |
| Game Development          | 4    | Backend Development       | 29   |
| Database                  | 5    | Data Science              | 36   |
| Cloud Computing           | 5    | Natural Language Processing | 47  |
| Containerization          | 5    | Deep Learning             | 53   |
| Frontend Development      | 6    | Large Language Models     | 135  |


Table 4: Statistics on Lines of Code (LOC) for repositories in our benchmark. The table below illustrates the statistics regarding the lines of code (LOC) of all repositories in the benchmark. It separately counts the number of repositories with LOC greater than 10,000 and greater than 100,000. The last two rows provide reference LOC for well-known industry-level repositories.
| **Configuration state** | **#LOC > 10,000** | **#LOC > 100,000** | **Medium** | **Max** |
|----------|----------|----------|----------|----------|
| Success(361) | 220(60.9%) | 27(7.5%) |14,578|6,431,084|
| Fail(59) | 50(84.7%) | 12(30.6%) |43,001|3,584,542|
| All(420) | 270(64.3%) | 39(9.3%) |15,854|6,431,084|
| requests(reference) | ✅ | - |12,782|12,782|
| pandas(reference) | ✅ | ✅ |571,849|571,849|

Table 5: Evaluation of Repo2Run on 61 popular industry-grade repositories. The repositories were selected from [GitHub Ranking](https://github.com/EvanLi/Github-Ranking/blob/master/Top100/Python.md), filtering out those without tests and with #LOC < 10,000.

