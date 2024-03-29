# MUML Code Generation Wiki

There is quite a bit of code generation already possible with the [MechatronicUML](http://www.mechatronicuml.org/de/index.html), and some more stuff was added during a Master's thesis concluding May 2022 - however, barely any documentation exists w.r.t. the code generation features of the MUML Tool Suite. Therefore, this wiki was created. There is still the  [original documentation](https://trac.cs.upb.de/mechatronicuml/wiki) of the MUML Tool Suite, but it neither covers the latest state of the metamodels nor the latest implementations, especially not regarding code generation for distributed deployments. The latest specification of the [MUML PIM](https://www.hni.uni-paderborn.de/publikationen/publikationen/?tx_hnippview_pi1%5Bpublikation%5D=9478) and [MUML PDM](https://www.hni.uni-paderborn.de/publikationen/publikationen/?tx_hnippview_pi1%5Bpublikation%5D=8015) are linked here.

As not all shortcomings of the past can be addressed, this wiki focues on
* Giving an overview about the code generion endeavors regarding the MUML (-> this page)
* Describing the newest additions: [The Master's Thesis](http://dx.doi.org/10.18419/opus-12528)
* [User documentation: how to use the code generation?](user-documentation/main.md)
* [Developer documentation: how can the code generation be improved, extended, customized?](dev-documentation/main.md)

## Overview about Code Generation with the MUML

There have been a couple of code generation approaches with the MUML. Firstly, there is the [C Code Generator](https://github.com/fraunhofer-iem/mechatronicuml-codegen-c) project. To the best of our knowledge, this refects the code generation documented in https://trac.cs.upb.de/mechatronicuml/wiki/user/CCodeGeneratorDescription which is a code generation approach that only uses a Platform-independent Model (PIM), thus, no communication code for a distributed deployment ist generated. However, platform specific code may be created based on three predefined platform setting. In the MUML Tool Suite, this is represented by the Export -> MechatronicUML -> Source Code options ```Arduino```, ```ANSI C99``` and ```nxtOSEK```. This code generator was not assessed in detail in the aforementioned Master's thesis as it does not support distributed deployments.

There are also adapters for [MATLAB/Simulink](https://github.com/fraunhofer-iem/mechatronicuml-simulinkadapter) and [Modelica (??)](https://github.com/fraunhofer-iem/mechatronicuml-modelicaadapter) which have briefly been looked at, but are not useful for code generation. T[he MATLAB/Simulink transformation is documented in a technical report](https://www.hni.uni-paderborn.de/publikationen/publikationen/?tx_hnippview_pi1%5Bpublikation%5D=8234) and in the [MUML Tool Suite documentation](https://trac.cs.upb.de/mechatronicuml/wiki/FujabaUserGuide/TutorialMUMLMatlab), and the Modelica Adapter is part of [Pohlmann Dis](https://digital.ub.uni-paderborn.de/hs/content/titleinfo/2824732).

Finally, the code generation approach for distributed deployments, which is called the *platform-modeling approach* in the aforementioned Master's thesis, originates from the [project group Cybertron](https://www.hni.uni-paderborn.de/sse/lehre/projektgruppenarchiv/projektgruppe-cybertron/). See their [user guide](https://trac.cs.upb.de/mechatronicuml/wiki/PGCybertron/userguide) for further information. While the implementation of Cybertron is documented by far the most detailed, to the best of our knowledge, it is not the most recent development. The most recent additions to the platform-modeling approach have been contributed in [Pohlmann Dis](https://digital.ub.uni-paderborn.de/hs/content/titleinfo/2824732). However, not all of the concepts are implemented in the current version of the MUML Tool Suite, version 1.0, like they are described/specified by Pohlmann. This latest approach has been adapted and extended in the aforementioned Master's thesis, and the documentation in this repository focuses on [using this extension](user-documentation/main.md) or [developing further extensions](dev-documentation/main.md). The following picture shows the process of the approach and in blue the tasks that have been adapted to support the Arduino-based robot cars.

![Code Generation Concept](./user-documentation/graphix/codegen_concept.png)

## [MUML Tool Suite](https://github.com/SQA-Robo-Lab/MUML_1_0-win32-x86_64)

Click the link above for more information.
