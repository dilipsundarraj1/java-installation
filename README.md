<!-- TOC -->
  * [Java Installation using Installer](#java-installation-using-installer)
  * [Java Installation using SDK man - windows](#java-installation-using-sdk-man---windows)
  * [Java Installation using SDK man - mac](#java-installation-using-sdk-man---mac)
    * [Install sdkMan](#install-sdkman)
    * [Install Java using sdk man](#install-java-using-sdk-man)
      * [How to install a specific Java Version ?](#how-to-install-a-specific-java-version-)
        * [Java 25](#java-25)
      * [How to switch between JAVA Versions ?](#how-to-switch-between-java-versions-)
        * [Java 21](#java-21)
      * [How to switch between JAVA Versions ?](#how-to-switch-between-java-versions--1)
<!-- TOC -->



## Java Installation using Installer

- Download the latest java from the below link
    - [Java 25](https://www.oracle.com/java/technologies/downloads/) 
    - [Java 21](https://www.oracle.com/java/technologies/downloads/#java21)

## Java Installation using SDK man - windows

> 🪟 **Windows Users:** If you're on Windows, please follow the [Windows Installation Guide](Windows_sdk_install.md) which covers installing Java using SDKMAN! via WSL (Windows Subsystem for Linux).

## Java Installation using SDK man - mac

> 📝 **Note:** The instructions below are for macOS/Linux users.

### Install sdkMan

- Follow the instructions in the below link to install sdkman in your mac.
    - [sdkMan](https://sdkman.io/install)

### Install Java using sdk man

- Run the below command to view the different version of supported Java
```agsl
sdk list java
```
#### How to install a specific Java Version ?

##### Java 25

```linux
sdk list java | grep '25'
```
- Running the below command will install Java 21.

```linux
sdk install java 25-tem
```

#### How to switch between JAVA Versions ?

- List the different installed versions of Java.

```linux
sdk list java | grep 'installed'
```

##### Java 21

```linux
sdk list java | grep '21'
```
- Running the below command will install Java 21.

```linux
sdk install java 21.0.2-tem
```

#### How to switch between JAVA Versions ?

- List the different installed versions of Java.

```linux
sdk list java | grep 'installed'
```

