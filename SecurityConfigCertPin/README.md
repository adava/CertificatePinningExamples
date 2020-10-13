
Android SecurityConfigCertPin Sample
===================================

This sample demonstrates certificate pinning using network-security-config parameters.

Introduction
------------

This sample demonstrates certificate pinning using network-security-config parameters,
[`pin-set`][1]. Since API 24, Android 7.0, certificate pinning can be automatically done using
project network security configurations.
The developers can pin any certificate within the chain of trust for a target domain. They
should provide the PIN and mention the algorithm:

      <pin digest="SHA-256">9SLklscvzMYdgf+52lp5ze/hY0CFHyLSPQzSpYYIBm8=</pin>

This project security configuration file contains both the correct and the wrong pin for
the badssl.com domain:

      <!--The correct one-->
      <pin digest="SHA-256">9SLklscvzMYj8f+52lp5ze/hY0CFHyLSPQzSpYYIBm8=</pin>
      
For testing, you need comment/uncomment the one you need.

[1]: https://developer.android.com/training/articles/security-config

Pre-requisites
--------------

- Android SDK 28
- Andrpin 7.0
- Android Build Tools v28.0.3
- Android Support Repository

Screenshots
-------------

<img src="screenshots/SecurityConfig.png" height="400" alt="Screenshot"/> 

Getting Started
---------------

This sample uses the Gradle build system. To build this project, use the
"gradlew build" command or use "Import Project" in Android Studio.
