# SMART on FHIR Demo
![FHIR Version 4.0.0](https://img.shields.io/badge/FHIR-R4-orange)
![Apache 2 License](https://img.shields.io/badge/license-Apache%202-blue)
![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/shaumik-ashraf/smart-on-fhir-demo/deploy.yml)
![GitHub deployments](https://img.shields.io/github/deployments/shaumik-ashraf/smart-on-fhir-demo/pages?label=pages)

 - [Overview](https://mitre.github.io/fhir-for-research/modules/smart-on-fhir-intro)
 - [Technical Guide](https://mitre.github.io/fhir-for-research/modules/smart-on-fhir-tech)
 - [Live Demo](https://shaumik-ashraf.github.com/smart-on-fhir-demo/index.html)

This repository supports the technical guide, and demonstrates a minimal SMART-on-FHIR application. You should follow along the technical guide, but a quickstart guide is posted here for your convnenience.

##### 1. Clone Repository

Make sure you have [git](https://git-scm.com/downloads) installed. In a console (windows powershell or terminal) run the following commands:

```
git clone https://github.com/Shaumik-Ashraf/smart-on-fhir-demo.git
cd smart-on-fhir-demo
```

##### 2. Next launch a static-file HTTP server. A few options are provided based on your computer environment setup:

 - python3: 
```
python3 -m http.server 8000
```

 - python2:
```
python -m SimpleHTTPServer 8000
```

 - nodeJS: 
```
npx http-server ./ -p 8000
```

 - ruby: 
```
gem install webrick && ruby -run -e httpd -- -p 8000
```

##### 3. Confirm your local server is running by visiting <http://localhost:8000/index.html>

##### 4. Go to <https://launch.smarthealthit.org>, enter `http://localhost:8000/launch.html` for in the “App’s Launch URL” field, and click “Launch”.

The website will then walk you through a provider-side stand-alone EHR SMART app launch, where you will select a fictional patient, and find the patients data loaded into your application. 
