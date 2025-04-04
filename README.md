# Repo2Run_Rebuttal
The code for Repo2Run can be found at the following link: https://anonymous.4open.science/r/Repo2Run-Anonymous-4AB8

Rebuttal Table 1: Language Support for Repo2Run Framework. It illustrates the various programming languages that can be supported by the Repo2Run framework by adjusting the base image and installation tools. This flexibility showcases the framework's capability to adapt to multiple languages, beyond just Python.
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

Rebuttal Figure 1: Our design for applying Repo2Run to Node.js.
![nodejs_design](nodejs_design.png)

Rebuttal Table 2: Data table for 28 fields of 420 repositories in our benchmark. We classify repositories in the following categories as ML/AI repositories: "Artificial Intelligence", "Reinforcement Learning", "Machine Learning", "Deep Learning", and "Large Language Models". The count of ML/AI repositories is 204 (48.57%).
| Type                    | Count | Type                      | Count | Type                             | Count |
|-------------------------|-------|---------------------------|-------|----------------------------------|-------|
| Large Language Models   | 135   | Deep Learning             | 53    | Natural Language Processing      | 47    |
| Data Science            | 36    | Backend Development       | 29    | Robotics                         | 17    |
| Data Visualization      | 11    | Web Framework             | 10    | Machine Learning                 | 9     |
| Testing Framework       | 7     | Network Programming       | 7     | Big Data Processing              | 7     |
| Cybersecurity           | 7     | Reinforcement Learning    | 6     | Frontend Development             | 6     |
| Containerization        | 5     | Cloud Computing           | 5     | Database                         | 5     |
| Game Development        | 4     | Data Processing           | 3     | Continuous Integration           | 2     |
| Mobile Development      | 2     | DevOps                    | 2     | Artificial Intelligence          | 1     |
| Operating System        | 1     | Video Generation          | 1     | Mobile Security                  | 1     |
| Backend Development     | 1     |

Rebuttal Table 3: Statistics on Lines of Code (LOC) for repositories in our benchmark. The table below illustrates the statistics regarding the lines of code (LOC) of all repositories in the benchmark. It separately counts the number of repositories with LOC greater than 10,000 and greater than 100,000. The last two rows provide reference LOC for well-known industry-level repositories.
| **Configuration state** | **#LOC > 10,000** | **#LOC > 100,000** | **Medium** | **Max** |
|----------|----------|----------|----------|----------|
| Success(361) | 220(60.9%) | 27(7.5%) |14,578|6,431,084|
| Fail(59) | 50(84.7%) | 12(30.6%) |43,001|3,584,542|
| All(420) | 270(64.3%) | 39(9.3%) |15,854|6,431,084|
| requests(reference) | ✅ | - |12,782|12,782|
| pandas(reference) | ✅ | ✅ |571,849|571,849|

Rebuttal Table 4: Evaluation of Repo2Run on 59 popular industry-grade repositories. The repositories were selected from [GitHub Ranking](https://github.com/EvanLi/Github-Ranking/blob/master/Top100/Python.md), filtering out those without tests and with #LOC < 10,000.
| **Configuration state** | **#LOC > 10,000** | **#LOC > 100,000** | **Medium** | **Max** |
|----------|----------|----------|----------|----------|
| Success(30) | 30(100%) | 14(46.7%) |96,157|2,389,065|
| Fail(29) | 29(100%) | 24(82.6%) |333,464|2,669,973|
| All(59) | 59(100%)| 40(9.3%) |124,352|2,669,973|

Rebuttal Table 5: Successful additional configuration of 30 industry-grade repositories.
| Repository                                            | #LOC | Repository                                            | #LOC | Repository                                            | #LOC |
|-------------------------------------------------------|------------|-------------------------------------------------------|------------|-------------------------------------------------------|------------|
| comfyanonymous/ComfyUI                                | 737,543    | OpenBB-finance/OpenBB                                 | 2,389,065  | scrapy/scrapy                                         | 77,278     |
| yt-dlp/yt-dlp                                         | 155,662    | keras-team/keras                                      | 204,537    | AUTOMATIC1111/stable-diffusion-webui                  | 40,448     |
| pallets/flask                                         | 25,190     | geekan/MetaGPT                                        | 82,305     | psf/black                                             | 118,551    |
| deepfakes/faceswap                                    | 74,690     | streamlit/streamlit                                   | 201,894    | psf/requests                                          | 12,782     |
| lllyasviel/Fooocus                                    | 328,199    | labmlai/annotated_deep_learning_paper_implementations | 510,851    | RVC-Boss/GPT-SoVITS                                   | 34,658     |
| mingrammer/diagrams                                   | 11,994     | OpenInterpreter/open-interpreter                      | 15,818     | hiyouga/LLaMA-Factory                                 | 76,000     |
| nvbn/thefuck                                          | 10,267     | pandas-dev/pandas                                     | 571,849    | ytdl-org/youtube-dl                                   | 96,157     |
| TheAlgorithms/Python                                  | 419,917    | fastapi/fastapi                                       | 177,120    | Textualize/rich                                       | 45,744     |
| All-Hands-AI/OpenHands                                | 160,514    | Stability-AI/stablediffusion                          | 13,698     | ultralytics/ultralytics                               | 94,201     |
| gradio-app/gradio                                     | 184,722    | QuivrHQ/quivr                                         | 10,264     | freqtrade/freqtrade                                   | 188,889    |

Rebuttal Table 6: 30 examples of "pollution" during pip installation. Package_name represents the name of the package that failed to download, "pollution" represents other packages introduced by the failed download, and "pollution" count represents the number of these introduced packages.
| package_name | "pollution" | "pollution" count |
|----------|----------|----------|
| zbarlight | pillow | 1 |
| mxnet-cu91 | chardet, idna, urllib3 | 3 |
| texthero | blis, catalogue, certifi, charset-normalizer, click, ... | 41 |
| url | six | 1 |
| robotframework-ride | certifi, charset-normalizer, idna, numpy, packaging, ... | 10 |
| adb | libusb1, typing | 2 |
| onegov-core | fastcache, mailthon, passlib, polib, pytz, ... | 12 |
| postal | six | 1 |
| changes | requests | 1 |
| mxnet-cu75mkl | chardet, idna, urllib3 | 3 |
| winpdb | numpy, six | 2 |
| slybot | attrs, Automat, certifi, chardet, charset-normalizer, ... | 30 |
| fbprophet | aiohappyeyeballs, aiohttp, aiosignal, appdirs, async-timeout, ... | 44 |
| mxnet-cu75 | chardet, idna, urllib3 | 3 | 
| libarchive | nose | 1 |
| atari-py | numpy, six | 2 |
| reppy | cachetools, certifi, charset-normalizer, idna, python-dateutil, ... | 8 |
| sovrin | leveldb, libnacl, msgpack-python, orderedset, Pympler, ... | 15 |
| scrapely | numpy, six, w3lib | 3 |
| kevinsr | python-version | 1 |
| pysurvive | colored, numpy, pillow, psutil, pygtrie, ... | 6 |
| horovod | cffi, cloudpickle, packaging, psutil, PyYAML, ... | 6 |
| cupy | fastrlock, numpy | 2 |
| face-recognition | face-recognition-models | 1 |
| nsot | gunicorn, idna, ipaddress, ipython, itypes, ... | 15 |
| gooey | colored, numpy, pillow, psutil, pygtrie, ... | 6 |
| wxpython | numpy, six | 2 |
| neuralcoref | annotated-types, blis, boto3, botocore, catalogue, ... | 47 |
| apache-airflow-backport-providers-apache-hive | apispec, argcomplete, attrs, babel, cached-property, ... | 58 |
| bcolz | numpy | 1 |
