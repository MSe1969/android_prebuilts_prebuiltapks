# Prebuilt APKs

THIS REPO HAS BEEN MIGRATED TO CODEBERG !!!

This is a collection of FOSS APKs, coupled with the respective Android.mk for an
easy integration in the Android build system.
These are just the official unmodified prebuilt binaries, signed by the
corresponding developers, except for:
 * additional_repos.xml, as it is just the microG FDroid repository XML file

To include them in your build just add their name in CUSTOM_PACKAGES (for
example in vendor/lineage/config/common.mk).

The included APKs are:
 * FDroid packages (binaries sourced from [here](https://f-droid.org/packages/org.fdroid.fdroid/) and [here](https://f-droid.org/packages/org.fdroid.fdroid.privileged/))
   * FDroid: a catalogue of FOSS (Free and Open Source Software) applications for the Android platform
   * FDroid Privileged Extension: a FDroid extension to ease the installation/removal of apps
   * additional_repos.xml: a simple package to include the [microG FDroid repository](https://microg.org/fdroid.html) in the ROM (requires FDroid >= 1.5)
 * microG packages (binaries sourced from [here](https://microg.org/download.html) and [here](https://github.com/microg/android_frameworks_mapsv1))
   * GmsCore: the main component of microG, a FOSS reimplementation of the Google Play Services (requires GsfProxy and FakeStore for full functionality)
   * GsfProxy: a GmsCore proxy for legacy GCM compatibility
   * FakeStore: an empty package that mocks the existence of the Google Play Store

## Adaptations and modifications of this repository (fork)
* GmsCore taken built from source (patched GCM to be enabled by default) and signed with platform key
* Added eSpeakTTS from e.OS
* FDroid and FDroidPrivilegedExtension built from source and signed with own key following v2-scheme
* Added Stubs for Android Auto and Google app, credit to Dylanger Daly <dylanger@diagnostix.io>

## Branches
Use branch 'master' up to Android 11, use branch '12L' from Android 12 onwards
