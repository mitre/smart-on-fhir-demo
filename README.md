# SMART on FHIR App (EHR Launch) Demo

![FHIR Version 4.0.0](https://img.shields.io/badge/FHIR-R4-orange)
![Apache 2 License](https://img.shields.io/badge/license-Apache%202-blue)
![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/mitre/smart-on-fhir-demo/deploy.yml)
![GitHub deployments](https://img.shields.io/github/deployments/mitre/smart-on-fhir-demo/github-pages?label=pages)

## Purpose

This repository contains a minimal demo SMART on FHIR application to support the [FHIR for Research resources](http://purl.org/fhir-for-research/web).

These resources contain some relevant background information:

- [Overview](https://mitre.github.io/fhir-for-research/modules/smart-on-fhir-intro)
- [Technical Guide](https://mitre.github.io/fhir-for-research/modules/smart-on-fhir-tech)

You can see a live demo version of the website in this repository at <https://mitre.github.io/smart-on-fhir-demo>.

## Running locally

### 1. Clone repository

Make sure you have [git](https://git-scm.com/downloads) installed. In a console (Windows Powershell or a terminal prompt on macOS/Linux) run the following commands:

```
git clone https://github.com/mitre/smart-on-fhir-demo.git
cd smart-on-fhir-demo
```

### 2. Launch a HTTP server

A few options are provided based on your computer environment setup:

- If you are using Visual Studio Code (VSCode), you can use [Microsoft's Live Preview extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode.live-server).

  Once the extension is installed, open `index.html` and use the Command Palette to run the "Live Preview: Show Preview (Internal Browser)" command. This will open up a live preview of `index.html` inside VSCode using a web server running on localhost (like the commands below).

- Otherwise, use a PowerShell/Terminal window to run one of the following:

  - python3:

    ```
    python3 -m http.server 3000
    ```

  - python2:

    ```
    python -m SimpleHTTPServer 3000
    ```

  - nodeJS:

    ```
    npx http-server ./ -p 3000
    ```

  - ruby:

    ```
    gem install webrick && ruby -run -e httpd -- -p 3000
    ```

### 3. Confirm your local server is running

Verify your server is running by visiting <http://localhost:3000/index.html>. (Note: this should happen automatically if you are using the VSCode extension.)

### 4. Simulate an EHR launch

Go to <https://launch.smarthealthit.org> and launch an app with URL `http://localhost:3000/launch.html` (If you can't get a localhost web server working, you can use this URL instead: `https://mitre.github.io/smart-on-fhir-demo/launch.html`.)

The SMART Launcher website will then walk you through a provider-side EHR SMART app launch, where you will select a fictional patient and load their data into your application.

---

## License

Copyright 2023 The MITRE Corporation

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

---

MITRE: Approved for Public Release / Case #23-0966
