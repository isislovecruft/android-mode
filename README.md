# Android development without Eclipse

## On debian wheezy/sid

### Dependencies

```
sudo apt-get install emacs24-nox ant multiarch-support
```

Also, install Oracle's Java JDK, either by doing:

```
sudo apt-get install sun-java6-jdk
```

or, if not available, get the current version of the Java 6 JDK from
http://www.oracle.com/technetwork/java/javase/downloads/index.html and then do:

```
sudo apt-get install java-package
make-jpkg <downloaded_jdk_file>
```

Then, create a symlink to the new JDK (assuming it is in /usr/lib/jvm/)if it
doesn't already exist:

```
test -s /usr/lib/jvm/java-6-sun || ln -s /usr/lib/jvm/java-6-sun-* /usr/lib/jvm/java-6-sun
```

### Add to ~/.emacs

```
;; Android mode
(add-to-list 'load-path "<path/to/android-mode>")
(require 'android-mode)
(defcustom android-mode-sdk-dir "<path/to/android-mode>"
  "Set to the directory containing the Android SDK"
  :type '(repeat string)
  :group 'android-mode)
```

### Also see:

The [Java Development Environment in Emacs](http://emacswiki.org/emacs/JavaDevelopmentEnvironment), [JDEE](http://sourceforge.net/projects/jdee/), which is apparently being turned into [CEDET](http://www.emacswiki.org/emacs/CollectionOfEmacsDevelopmentEnvironmentTools#CEDET), a set of various tools for Emacs.

[Javadoc-Help for Emacs](http://javadochelp.sourceforge.net/)

## On Ubuntu

Stop using Ubuntu. That will solve most of your problems.
