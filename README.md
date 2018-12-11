# Broad Media Player (BBMEDIA) #

BBMEDIA is an application level media player for Android. It provides an
alternative to Android’s MediaPlayer API for 
* Playing audio and video both locally and over the Internet.
* DLNA features

## Documentation ##

TBD.

## Using BBMEDIA ##

BBMEDIA modules can be obtained from JCenter. It's also possible to clone the
repository and depend on the modules locally.

### From JCenter ###

TBD.

### Locally ###

Cloning the repository and depending on the modules locally is required when
using some BBMEDIA modules. It's also a suitable approach if you
want to make local changes to BBMEDIA, or if you want to use a development
branch.

First, clone the repository into a local directory and checkout the desired
branch:

```sh
git clone https://github.com/bbtechlab/bbmedia.git
cd ~/bbmedia
git submodule init
git submodule update
```

Next, add the following to your project's `settings.gradle` file, replacing
`path/to/bbmedia` with the path to your local copy:

```gradle
gradle.ext.bbmediaRoot = 'path/to/bbmedia'
gradle.ext.exoplayerModulePrefix = 'bbmedia-'
apply from: new File(gradle.ext.bbmediaRoot, 'core_settings.gradle')
```

You should now see the BBMEDIA modules appear as part of your project. You can
depend on them as you would on any other local module, for example:

```gradle
implementation project(':bbmedia-core')
implementation project(':bbmedia-presenter')
implementation project(':bbmedia-model')
```

## Developing BBMEDIA ##

#### Project branches ####

TBD.

#### Using Android Studio ####

To develop BBMEDIA using Android Studio, simply open the BBMEDIA project in
the root directory of the repository.
