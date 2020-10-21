# Getting started (Developer)

## Pre-requisites

* `Maven 3.6.3`
* `OpenJDK 1.8`, or `OracleJDK 1.8` (higher versions will not work yet)
* `Git` installed and in your `PATH` variable

## System Requirements

In order to build Strongbox in reasonably short times you need:

* At least 16 GB RAM
* Minimum 2 cores / 4 threads (recommended: 4 cores / 8 threads or more)
* An SSD

## Before you continue

Please, place this [settings.xml]({{resources}}/maven/settings.xml) file under your `~/.m2` directory.
We have dependencies which are only available through our repository and if you skip this it will cause build failure.

=== "Linux"
    ``` linenums="1"
    mkdir ~/.m2
    curl -o ~/.m2/settings.xml \
            {{resources}}/maven/settings.xml
    ```
=== "Windows"
    ``` linenums="1"
    mkdir %HOMEPATH%\.m2
    curl -o %HOMEPATH%\.m2\settings.xml ^
            {{resources}}/maven/settings.xml
    ```

!!! tip
    You can use a different location to save our `settings.xml`. For example, you could save it as   
    `~/.m2/settings-strongbox.xml` and then specify this path when executing maven commands:
    ```
    mvn -s ~/.m2/settings-strongbox.xml clean install
    ```
