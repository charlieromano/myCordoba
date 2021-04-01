# myCordoba
This is my repo for studying Apache Cordova. My goal is to build a mobile app using HTML, Javascript and CSS for Android amd iOS phones.

Check Java:
```bash
java -version
```
If the Java version is not 8 (@Ubuntu 20), then we need to remove and install java 8 with:
```bash
sudo rm -r /usr/lib/jvm/java-11-......
sudo apt install openjdk8-jdk openjdk-8-jre
java -version
```
After installing Java, Android SDK, Node, and maybe sth else:

```bash
export PATH=/home/charlieromano/Documents/Personal/Arch/myCordoba/hello
## This is the local path for the app

export ANDROID_SDK_ROOT=/home/charlieromano/Android/Sdk
export ANDROID_HOME=/home/charlieromano/Android/Sdk
export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64

cd $PATH
yes | sdkmanager --licenses --sdk_root=$ANDROID_HOME
cordova emulate android
```
Si anduvo bien, después de un rato de debug que para arrancar con Cordova parece ser normal, debería correr el init:

```bash
charlieromano@TOSHIBA-L845:~/Documents/Personal/Arch/myCordoba/hello$ cordova emulate android
Checking Java JDK and Android SDK versions
ANDROID_SDK_ROOT=/home/charlieromano/Android/Sdk (recommended setting)
ANDROID_HOME=/home/charlieromano/Android/Sdk (DEPRECATED)
Using Android SDK: /home/charlieromano/Android/Sdk
Starting a Gradle Daemon (subsequent builds will be faster)

BUILD SUCCESSFUL in 4s
1 actionable task: 1 executed
Subproject Path: CordovaLib
Subproject Path: app
Downloading https://services.gradle.org/distributions/gradle-6.5-all.zip
...........................................................................................................................................
Unzipping /home/charlieromano/.gradle/wrapper/dists/gradle-6.5-all/2oz4ud9k3tuxjg84bbf55q0tn/gradle-6.5-all.zip to /home/charlieromano/.gradle/wrapper/dists/gradle-6.5-all/2oz4ud9k3tuxjg84bbf55q0tn
Set executable permissions for: /home/charlieromano/.gradle/wrapper/dists/gradle-6.5-all/2oz4ud9k3tuxjg84bbf55q0tn/gradle-6.5/bin/gradle

Welcome to Gradle 6.5!

Here are the highlights of this release:
 - Experimental file-system watching
 - Improved version ordering
 - New samples

For more details see https://docs.gradle.org/6.5/release-notes.html

Starting a Gradle Daemon, 1 incompatible Daemon could not be reused, use --status for details

```


