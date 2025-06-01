<!---

  Copyright 2019 Google Inc. All Rights Reserved.
 
   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at
 
       http://www.apache.org/licenses/LICENSE-2.0
 
   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
-->
Bubblewrap
==========
[![Node CI Status](https://github.com/GoogleChromeLabs/bubblewrap/workflows/Node%20CI/badge.svg)](https://github.com/GoogleChromeLabs/bubblewrap/actions?query=workflow%3A%22Node+CI%22)

Bubblewrap is a set of tools and libraries designed to help developers to create, build and update
projects for Android Applications that launch Progressive Web App (PWA) using
[Trusted Web Activity (TWA)](https://developer.chrome.com/docs/android/trusted-web-activity/).

<hr />


## My notes

Bubblewrap's keystore generation DOES NOT WORK. Use this instead:```
keytool -genkey -v -keystore android.keystore -alias android -keyalg RSA -keysize 2048 -validity 10000
```

JDK and Android SDK are stored at these respective paths:
```
? Do you want Bubblewrap to install the JDK (recommended)?
  (Enter "No" to use your own JDK 17 installation) Yes
Downloading JDK 17 to ~/.bubblewrap/jdk
Downloading the JDK 17 Sources...
 >> [████████████████████████████████████████] 100% | 174793k of 174783k
Decompressing the JDK 17 Sources...
Downloading the JDK 17 Binaries...
 >> [████████████████████████████████████████] 100% | 187887k of 187887k
Decompressing the JDK 17 Binaries...
Extracting ~/.bubblewrap/jdk/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz to ~/.bubblewrap/jdk
? Do you want Bubblewrap to install the Android SDK (recommended)?
  (Enter "No" to use your own Android SDK installation) Yes
? Do you agree to the Android SDK terms and conditions at https://developer.android.com/studio/terms.html? Yes
Downloading Android SDK to ~/.bubblewrap/android_sdk
Downloading the Android SDK...
 >> [████████████████████████████████████████] 100% | 84504k of 84504k
Decompressing the Android SDK...

```

<hr />


## Requirements
- [Node.js](https://nodejs.org/en/) 14.15.0 or above

## Getting Started
- To get started with building an application using Bubblewrap, check the [Trusted Web Activity
Quick Start Guide][1] or the [bubblewrap/cli](./packages/cli) documentation.

## Bubblewrap Components

- **[bubblewrap/core](./packages/core):** a javascript library for generating, building and
updating TWA projects.
- **[bubblewrap/cli](./packages/cli):** a command-line version of Bubblewrap.
- **[bubblewrap/validator](./packages/validator):** library to validate the correctness and
compare Trusted Web Activity projects against the quality criteria.

## Community

We welcome anyone who wants to contribute with issues, feedback, feature requests or just
generally discuss Bubblewrap. Alternatively developers can contribute to the conversation
by joining the public monthly office hours, which hosted on every first Thursday at 5PM,
London time. Check when the next office hours is going to happen via [this calendar][5]
and join the meeting via [this link][3].
 
## Getting started with GUI tools 
- If you are just getting started with APK generation from PWA, You might want to check [PWABuilder](https://www.pwabuilder.com/).
This tool is powered by Bubblewrap and uses the same underlying core. 

## Contributing

See [CONTRIBUTING](./CONTRIBUTING.md) for more.

## License

See [LICENSE](./LICENSE) for more.

## Disclaimer

This is not an officially supported Google product.

[1]: https://developer.chrome.com/docs/android/trusted-web-activity/quick-start/
[2]: https://join.slack.com/t/chromiumdev/shared_invite/zt-4b4af0yu-1mZ7uF6pCjYMC4poRr8Bkg
[3]: https://meet.google.com/hps-wjke-qac
[4]: https://chromiumdev.slack.com/archives/C01829L0URJ
[5]: https://calendar.google.com/calendar/embed?src=c_jovg5osnfku7kigbo7joh1reug%40group.calendar.google.com&ctz=Europe%2FLondon&mode=AGENDA
[6]: https://chromiumdev.slack.com/
