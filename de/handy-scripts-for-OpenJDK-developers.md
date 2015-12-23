# Nützliche Scripts

**Nützliche Scripts zum Updaten, Builden und Testen von OpenJDK**

Die folgenden bash Scripts erleichtern dir das Leben.

```updateAndCleanBuildOpenJDK.sh``` - gedacht um ab und zu laufen zu lassen, oder falls du von Grund auf builden willst

```bash
./get_source.sh
bash configure
make clean images
```

```updateCleanBuildAndTestOpenJDK.sh``` - gedacht um ab und zu laufen zu lassen, oder falls du von Grund auf builden und testen willst

```bash
./get_source.sh
bash configure
make clean images
make test```


```updateAndBuildOpenJDK.sh``` - gedacht um regelmässig laufen zu lassen (inkrementeller Build)

```bash
./get_source.sh
bash configure
make images```


```updateBuildAndTestOpenJDK.sh``` - oft laufen lassen

```bash
./get_source.sh
bash configure
make images
make test```

<br/>
__Ein einfaches Beispiel für eine Anpassung an OpenJDK, und wie man einen Client schreibt der diese Anpassung testet__

```buildAndRunTheChangedRandom.sh``` - nach der Anpassung an ChangeRandom.java laufen lassen

```bash
##### OpenJDK8
IMAGES_FOLDER=$SOURCES/jdk8/build/linux-x86_64-normal-server-release/images
$IMAGES_FOLDER/j2sdk-image/bin/javac -version
$IMAGES_FOLDER/j2sdk-image/bin/javac ChangeRandom.java
$IMAGES_FOLDER/jdk/bin/javap -verbose ChangeRandom | grep "major"
$IMAGES_FOLDER/jdk/bin/javap -verbose ChangeRandom | grep "minor"

$IMAGES_FOLDER/jre/bin/java -version
$IMAGES_FOLDER/j2re-image/bin/java ChangeRandom
```

```bash
##### OpenJDK9
IMAGES_FOLDER=$SOURCES/jdk9/build/linux-x86_64-normal-server-release/images

$IMAGES_FOLDER/jdk/bin/javac -version
$IMAGES_FOLDER/jdk/bin/javac ChangeRandom.java
$IMAGES_FOLDER/jdk/bin/javap -verbose ChangeRandom | grep "major"
$IMAGES_FOLDER/jdk/bin/javap -verbose ChangeRandom | grep "minor"

$IMAGES_FOLDER/jre/bin/java -version
$IMAGES_FOLDER/jre/bin/java ChangeRandom
```

<br/>
**JTREG laufen lassen**

```runJtregViaExecutable.sh``` - starte JTREG mit dem $JTREG/bin/jtreg Befehl

```
$HOME/jtreg/linux/bin/jtreg -verbose:all  -jdk:$HOME/sources/jdk8_tl/build/linux-x86_64-normal-server-release/images/j2sdk-image/ $1
```

```runJtregViaTheJarFile.sh``` - starte JTREG mit dem  $JTREG/lib/jtreg.jar Befehl

```
java -jar $HOME/jtreg/lib/jtreg.jar -verbose:all  -jdk:$HOME/sources/jdk8_tl/build/linux-x86_64-normal-server-release/images/j2sdk-image/ $1```