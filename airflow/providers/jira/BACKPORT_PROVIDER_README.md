<!--
 Licensed to the Apache Software Foundation (ASF) under one
 or more contributor license agreements.  See the NOTICE file
 distributed with this work for additional information
 regarding copyright ownership.  The ASF licenses this file
 to you under the Apache License, Version 2.0 (the
 "License"); you may not use this file except in compliance
 with the License.  You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing,
 software distributed under the License is distributed on an
 "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
 KIND, either express or implied.  See the License for the
 specific language governing permissions and limitations
 under the License.
 -->


# Package apache-airflow-backport-providers-jira

Release: 2021.3.17

**Table of contents**

- [Backport package](#backport-package)
- [Installation](#installation)
- [PIP requirements](#pip-requirements)
- [Provider class summary](#provider-classes-summary)
    - [Operators](#operators)
        - [Moved operators](#moved-operators)
    - [Sensors](#sensors)
        - [Moved sensors](#moved-sensors)
    - [Hooks](#hooks)
        - [Moved hooks](#moved-hooks)
- [Releases](#releases)
    - [Release 2021.3.17](#release-2021317)
    - [Release 2020.10.29](#release-20201029)
    - [Release 2020.10.5](#release-2020105)
    - [Release 2020.6.24](#release-2020624)

## Backport package

This is a backport providers package for `jira` provider. All classes for this provider package
are in `airflow.providers.jira` python package.

**Only Python 3.6+ is supported for this backport package.**

While Airflow 1.10.* continues to support Python 2.7+ - you need to upgrade python to 3.6+ if you
want to use this backport package.


## Release 2021.3.17

### Bug fixes

* `The 2020.10.29 relese was broken  (#14673)`
* `Switch to f-strings using flynt. (#13732)`
* `Rename remaing modules to match AIP-21 (#12917)`
* `Add support for dynamic connection form fields per provider (#12558)`
* `Adds support for Connection/Hook discovery from providers (#12466)`


## Installation

You can install this package on top of an existing airflow 1.10.* installation via
`pip install apache-airflow-backport-providers-jira`

## PIP requirements

| PIP package   | Version required   |
|:--------------|:-------------------|
| `JIRA`        | `>1.0.7`           |

# Provider classes summary

In Airflow 2.0, all operators, transfers, hooks, sensors, secrets for the `jira` provider
are in the `airflow.providers.jira` package. You can read more about the naming conventions used
in [Naming conventions for provider packages](https://github.com/apache/airflow/blob/master/CONTRIBUTING.rst#naming-conventions-for-provider-packages)


## Operators



### Moved operators

| Airflow 2.0 operators: `airflow.providers.jira` package                                                               | Airflow 1.10.* previous location (usually `airflow.contrib`)                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [operators.jira.JiraOperator](https://github.com/apache/airflow/blob/master/airflow/providers/jira/operators/jira.py) | [contrib.operators.jira_operator.JiraOperator](https://github.com/apache/airflow/blob/v1-10-stable/airflow/contrib/operators/jira_operator.py) |


## Sensors



### Moved sensors

| Airflow 2.0 sensors: `airflow.providers.jira` package                                                                 | Airflow 1.10.* previous location (usually `airflow.contrib`)                                                                               |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [sensors.jira.JiraSensor](https://github.com/apache/airflow/blob/master/airflow/providers/jira/sensors/jira.py)       | [contrib.sensors.jira_sensor.JiraSensor](https://github.com/apache/airflow/blob/v1-10-stable/airflow/contrib/sensors/jira_sensor.py)       |
| [sensors.jira.JiraTicketSensor](https://github.com/apache/airflow/blob/master/airflow/providers/jira/sensors/jira.py) | [contrib.sensors.jira_sensor.JiraTicketSensor](https://github.com/apache/airflow/blob/v1-10-stable/airflow/contrib/sensors/jira_sensor.py) |


## Hooks



### Moved hooks

| Airflow 2.0 hooks: `airflow.providers.jira` package                                                       | Airflow 1.10.* previous location (usually `airflow.contrib`)                                                               |
|:----------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [hooks.jira.JiraHook](https://github.com/apache/airflow/blob/master/airflow/providers/jira/hooks/jira.py) | [contrib.hooks.jira_hook.JiraHook](https://github.com/apache/airflow/blob/v1-10-stable/airflow/contrib/hooks/jira_hook.py) |



## Releases

### Release 2021.3.17

| Commit                                                                                         | Committed   | Subject                                                                          |
|:-----------------------------------------------------------------------------------------------|:------------|:---------------------------------------------------------------------------------|
| [88bdcfa0d](https://github.com/apache/airflow/commit/88bdcfa0df5bcb4c489486e05826544b428c8f43) | 2021-02-04  | `Prepare to release a new wave of providers. (#14013)`                           |
| [ac2f72c98](https://github.com/apache/airflow/commit/ac2f72c98dc0821b33721054588adbf2bb53bb0b) | 2021-02-01  | `Implement provider versioning tools (#13767)`                                   |
| [a9ac2b040](https://github.com/apache/airflow/commit/a9ac2b040b64de1aa5d9c2b9def33334e36a8d22) | 2021-01-23  | `Switch to f-strings using flynt. (#13732)`                                      |
| [3fd5ef355](https://github.com/apache/airflow/commit/3fd5ef355556cf0ad7896bb570bbe4b2eabbf46e) | 2021-01-21  | `Add missing logos for integrations (#13717)`                                    |
| [295d66f91](https://github.com/apache/airflow/commit/295d66f91446a69610576d040ba687b38f1c5d0a) | 2020-12-30  | `Fix Grammar in PIP warning (#13380)`                                            |
| [6cf76d7ac](https://github.com/apache/airflow/commit/6cf76d7ac01270930de7f105fb26428763ee1d4e) | 2020-12-18  | `Fix typo in pip upgrade command :( (#13148)`                                    |
| [32971a1a2](https://github.com/apache/airflow/commit/32971a1a2de1db0b4f7442ed26facdf8d3b7a36f) | 2020-12-09  | `Updates providers versions to 1.0.0 (#12955)`                                   |
| [b40dffa08](https://github.com/apache/airflow/commit/b40dffa08547b610162f8cacfa75847f3c4ca364) | 2020-12-08  | `Rename remaing modules to match AIP-21 (#12917)`                                |
| [9b39f2478](https://github.com/apache/airflow/commit/9b39f24780e85f859236672e9060b2fbeee81b36) | 2020-12-08  | `Add support for dynamic connection form fields per provider (#12558)`           |
| [2037303ee](https://github.com/apache/airflow/commit/2037303eef93fd36ab13746b045d1c1fee6aa143) | 2020-11-29  | `Adds support for Connection/Hook discovery from providers (#12466)`             |
| [c34ef853c](https://github.com/apache/airflow/commit/c34ef853c890e08f5468183c03dc8f3f3ce84af2) | 2020-11-20  | `Separate out documentation building per provider  (#12444)`                     |
| [008035450](https://github.com/apache/airflow/commit/00803545023b096b8db4fbd6eb473843096d7ce4) | 2020-11-18  | `Update provider READMEs for 1.0.0b2 batch release (#12449)`                     |
| [ae7cb4a1e](https://github.com/apache/airflow/commit/ae7cb4a1e2a96351f1976cf5832615e24863e05d) | 2020-11-17  | `Update wrong commit hash in backport provider changes (#12390)`                 |
| [6889a333c](https://github.com/apache/airflow/commit/6889a333cff001727eb0a66e375544a28c9a5f03) | 2020-11-15  | `Improvements for operators and hooks ref docs (#12366)`                         |
| [7825e8f59](https://github.com/apache/airflow/commit/7825e8f59034645ab3247229be83a3aa90baece1) | 2020-11-13  | `Docs installation improvements (#12304)`                                        |
| [85a18e13d](https://github.com/apache/airflow/commit/85a18e13d9dec84275283ff69e34704b60d54a75) | 2020-11-09  | `Point at pypi project pages for cross-dependency of provider packages (#12212)` |
| [59eb5de78](https://github.com/apache/airflow/commit/59eb5de78c70ee9c7ae6e4cba5c7a2babb8103ca) | 2020-11-09  | `Update provider READMEs for up-coming 1.0.0beta1 releases (#12206)`             |
| [b2a28d159](https://github.com/apache/airflow/commit/b2a28d1590410630d66966aa1f2b2a049a8c3b32) | 2020-11-09  | `Moves provider packages scripts to dev (#12082)`                                |
| [41bf172c1](https://github.com/apache/airflow/commit/41bf172c1dc75099f4f9d8b3f3350b4b1f523ef9) | 2020-11-04  | `Simplify string expressions (#12093)`                                           |
| [4e8f9cc8d](https://github.com/apache/airflow/commit/4e8f9cc8d02b29c325b8a5a76b4837671bdf5f68) | 2020-11-03  | `Enable Black - Python Auto Formmatter (#9550)`                                  |
| [5a439e84e](https://github.com/apache/airflow/commit/5a439e84eb6c0544dc6c3d6a9f4ceeb2172cd5d0) | 2020-10-26  | `Prepare providers release 0.0.2a1 (#11855)`                                     |


### Release 2020.10.29

| Commit                                                                                         | Committed   | Subject                                                      |
|:-----------------------------------------------------------------------------------------------|:------------|:-------------------------------------------------------------|
| [b680bbc0b](https://github.com/apache/airflow/commit/872b1566a11cb73297e657ff325161721b296574) | 2020-10-24  | Generated backport providers readmes/setup for 2020.10.29    |
| [16e712971](https://github.com/apache/airflow/commit/16e7129719f1c0940aef2a93bed81368e997a746) | 2020-10-13  | Added support for provider packages for Airflow 2.0 (#11487) |
| [0a0e1af80](https://github.com/apache/airflow/commit/0a0e1af80038ef89974c3c8444461fe867945daa) | 2020-10-03  | Fix Broken Markdown links in Providers README TOC (#11249)   |


### Release 2020.10.5

| Commit                                                                                         | Committed   | Subject                                                              |
|:-----------------------------------------------------------------------------------------------|:------------|:---------------------------------------------------------------------|
| [ca4238eb4](https://github.com/apache/airflow/commit/ca4238eb4d9a2aef70eb641343f59ee706d27d13) | 2020-10-02  | Fixed month in backport packages to October (#11242)                 |
| [5220e4c38](https://github.com/apache/airflow/commit/5220e4c3848a2d2c81c266ef939709df9ce581c5) | 2020-10-02  | Prepare Backport release 2020.09.07 (#11238)                         |
| [fdd9b6f65](https://github.com/apache/airflow/commit/fdd9b6f65b608c516b8a062b058972d9a45ec9e3) | 2020-08-25  | Enable Black on Providers Packages (#10543)                          |
| [3696c34c2](https://github.com/apache/airflow/commit/3696c34c28c6bc7b442deab999d9ecba24ed0e34) | 2020-08-24  | Fix typo in the word &#34;release&#34; (#10528)                              |
| [ee7ca128a](https://github.com/apache/airflow/commit/ee7ca128a17937313566f2badb6cc569c614db94) | 2020-08-22  | Fix broken Markdown refernces in Providers README (#10483)           |
| [cdec30125](https://github.com/apache/airflow/commit/cdec3012542b45d23a05f62d69110944ba542e2a) | 2020-08-07  | Add correct signature to all operators and sensors (#10205)          |
| [24c8e4c2d](https://github.com/apache/airflow/commit/24c8e4c2d6e359ecc2c7d6275dccc68de4a82832) | 2020-08-06  | Changes to all the constructors to remove the args argument (#10163) |
| [aeea71274](https://github.com/apache/airflow/commit/aeea71274d4527ff2351102e94aa38bda6099e7f) | 2020-08-02  | Remove `args` parameter from provider operator constructors (#10097) |
| [ba2d6408e](https://github.com/apache/airflow/commit/ba2d6408e64f219e8f53a20a5a149e3d8109db31) | 2020-07-29  | Add typing for jira provider (#10005)                                |
| [d0e7db402](https://github.com/apache/airflow/commit/d0e7db4024806af35e3c9a2cae460fdeedd4d2ec) | 2020-06-19  | Fixed release number for fresh release (#9408)                       |


### Release 2020.6.24

| Commit                                                                                         | Committed   | Subject                                                                 |
|:-----------------------------------------------------------------------------------------------|:------------|:------------------------------------------------------------------------|
| [12af6a080](https://github.com/apache/airflow/commit/12af6a08009b8776e00d8a0aab92363eb8c4e8b1) | 2020-06-19  | Final cleanup for 2020.6.23rc1 release preparation (#9404)              |
| [c7e5bce57](https://github.com/apache/airflow/commit/c7e5bce57fe7f51cefce4f8a41ce408ac5675d13) | 2020-06-19  | Prepare backport release candidate for 2020.6.23rc1 (#9370)             |
| [f6bd817a3](https://github.com/apache/airflow/commit/f6bd817a3aac0a16430fc2e3d59c1f17a69a15ac) | 2020-06-16  | Introduce &#39;transfers&#39; packages (#9320)                                  |
| [0b0e4f7a4](https://github.com/apache/airflow/commit/0b0e4f7a4cceff3efe15161fb40b984782760a34) | 2020-05-26  | Preparing for RC3 release of backports (#9026)                           |
| [00642a46d](https://github.com/apache/airflow/commit/00642a46d019870c4decb3d0e47c01d6a25cb88c) | 2020-05-26  | Fixed name of 20 remaining wrongly named operators. (#8994)             |
| [375d1ca22](https://github.com/apache/airflow/commit/375d1ca229464617780623c61c6e8a1bf570c87f) | 2020-05-19  | Release candidate 2 for backport packages 2020.05.20 (#8898)            |
| [12c5e5d8a](https://github.com/apache/airflow/commit/12c5e5d8ae25fa633efe63ccf4db389e2b796d79) | 2020-05-17  | Prepare release candidate for backport packages (#8891)                 |
| [f3521fb0e](https://github.com/apache/airflow/commit/f3521fb0e36733d8bd356123e56a453fd37a6dca) | 2020-05-16  | Regenerate readme files for backport package release (#8886)            |
| [92585ca4c](https://github.com/apache/airflow/commit/92585ca4cb375ac879f4ab331b3a063106eb7b92) | 2020-05-15  | Added automated release notes generation for backport operators (#8807) |
| [05443c6dc](https://github.com/apache/airflow/commit/05443c6dc8100e791446bbcc0df04de6e34017bb) | 2020-03-23  | Add missing call to Super class in remaining providers (#7828)          |
| [f3ad5cf61](https://github.com/apache/airflow/commit/f3ad5cf6185b9d406d0fb0a4ecc0b5536f79217a) | 2020-02-03  | [AIRFLOW-4681] Make sensors module pylint compatible (#7309)            |
| [97a429f9d](https://github.com/apache/airflow/commit/97a429f9d0cf740c5698060ad55f11e93cb57b55) | 2020-02-02  | [AIRFLOW-6714] Remove magic comments about UTF-8 (#7338)                |
| [4a21b6216](https://github.com/apache/airflow/commit/4a21b62161a8e14f0dbc06f292f4662832c52669) | 2019-12-13  | [AIRFLOW-5959][AIP-21] Move contrib/*/jira to providers (#6661)         |
