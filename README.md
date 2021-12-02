# PowSyBl Dev Tools

[![MPL-2.0 License](https://img.shields.io/badge/license-MPL_2.0-blue.svg)](https://www.mozilla.org/en-US/MPL/2.0/)
[![Slack](https://img.shields.io/badge/slack-powsybl-blueviolet.svg?logo=slack)](https://join.slack.com/t/powsybl/shared_invite/zt-rzvbuzjk-nxi0boim1RKPS5PjieI0rA)

PowSyBl (**Pow**er **Sy**stem **Bl**ocks) is an open source framework written in Java, that makes it easy to write complex
software for power systems’ simulations and analysis. Its modular approach allows developers to extend or customize its
features.

PowSyBl is part of the LF Energy Foundation, a project of The Linux Foundation that supports open source innovation projects
within the energy and electricity sectors.

<p align="center">
<img src="https://raw.githubusercontent.com/powsybl/powsybl-gse/main/gse-spi/src/main/resources/images/logo_lfe_powsybl.svg?sanitize=true" alt="PowSyBl Logo" width="50%"/>
</p>

Read more at https://www.powsybl.org !

This project and everyone participating in it is governed by the [PowSyBl Code of Conduct](https://github.com/powsybl/.github/blob/main/CODE_OF_CONDUCT.md).
By participating, you are expected to uphold this code. Please report unacceptable behavior to [powsybl-tsc@lists.lfenergy.org](mailto:powsybl-tsc@lists.lfenergy.org).

## PowSyBl vs PowSyBl Dev Tools

PowSyBl Dev Tools are components meant solely for debugging various PowSyBl components - in particular for [PowSyBl Single Line Diagram](https://github.com/powsybl/powsybl-single-line-diagram).

## PowSyBl single-line-diagram-viewer Dev Tool
Not to be confused with JavaScript viewer [powsybl-single-line-diagram-viewer](https://github.com/powsybl/powsybl-single-line-diagram-viewer)!

PowSyBl single-line-diagram-viewer Dev Tool is a JavaFX basic viewer used to display the single line diagrams generated by  [PowSyBl Single Line Diagram](https://github.com/powsybl/powsybl-single-line-diagram). It is based on [FranzXaver](https://github.com/afester/FranzXaver) library, which translates a SVG file into a JavaFX component.

### Launching the viewer
- First install
  * [JavaFX 17](https://openjfx.io/)
  * [powsybl-single-line-diagram](https://github.com/powsybl/powsybl-single-line-diagram) latest SNAPSHOT version (clone the repo then `mvn clean install` on `main` branch)
- Then launch the viewer by running `SingleLineDiagramViewer::main`, with the following vm options:
  ```
  --module-path /path/to/javafx-17/lib --add-modules=javafx.controls,javafx.web
  ```  
- Select the file you want to import in the viewer
- Once the file is imported, select the substation or the voltage level you want to display; you should obtain something similar to the following screenshot:

![Viewer screenshot](.github/screenshot.png)
