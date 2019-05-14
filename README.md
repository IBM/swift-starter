<p align="center">
    <a href="http://kitura.io/">
        <img src="https://raw.githubusercontent.com/IBM-Swift/Kitura/master/Sources/Kitura/resources/kitura-bird.svg?sanitize=true" height="100" alt="Kitura">
    </a>
</p>


<p align="center">
    <a href="https://cloud.ibm.com">
    <img src="https://img.shields.io/badge/IBM%20Cloud-powered-blue.svg" alt="IBM Cloud">
    </a>
    <img src="https://img.shields.io/badge/platform-ios_swift-lightgrey.svg?style=flat" alt="platform">
    <img src="https://img.shields.io/badge/os-macOS-green.svg?style=flat" alt="macOS">
    <img src="https://img.shields.io/badge/os-linux-green.svg?style=flat" alt="Linux">
    <img src="https://img.shields.io/badge/license-Apache2-blue.svg?style=flat" alt="Apache 2">
    <a href="http://swift-at-ibm-slack.mybluemix.net/">
    <img src="http://swift-at-ibm-slack.mybluemix.net/badge.svg" alt="Slack Status">
    </a>
</p>


# Create and deploy a basic Swift Kitura application

> We have similar applications available for [Node.js](https://github.com/IBM/nodejs-starter), [Java Spring](https://github.com/IBM/spring-starter), [Go](https://github.com/IBM/go-starter), [Python Flask](https://github.com/IBM/flask-starter), and [Java Liberty](https://github.com/IBM/java-liberty-starter).

In this sample application, you will create a basic application using [Kitura](https://www.kitura.io/), complete with standard best practices, including a health check and application metric monitoring.


## Steps

You can [deploy this application to IBM Cloud](https://cloud.ibm.com/developer/appservice/create-app?navMode=starterkits) or [build it locally](#building-locally) by cloning this repo first.  Once your app is live, you can access the `/health` and `/swiftmetrics-dash` to build out your cloud native application.

### Deploying to IBM Cloud

<p align="center">
    <a href="https://cloud.ibm.com/developer/appservice/create-app?navMode=starterkits">
    <img src="https://cloud.ibm.com/devops/setup/deploy/button_x2.png" alt="Deploy to IBM Cloud">
    </a>
</p>

Use the button above to deploy this same application to IBM Cloud.  This option will create a deployment pipeline, complete with a hosted Git lab project and devops toolchain.  You will have the option of deploying to either CloudFoundry or a Kubernetes cluster. [IBM Cloud DevOps](https://www.ibm.com/cloud-computing/bluemix/devops) services provides toolchains as a set of tool integrations that support development, deployment, and operations tasks inside IBM Cloud. 


### Building Locally

To get started building this application locally, you can either run the application natively or use the IBM Cloud Developer Tools for containerization and easy deployment to IBM Cloud.


#### Native Application Development

- On Linux, install the [Swift toolchain](https://swift.org/) version _v5.0_.
- On macOS, install [Xcode](https://developer.apple.com/download) _v10.2+_

In the root of this project, first build the application using `swift build`. `swift run` will launch the application and render it at `http://localhost:8080`.

#### IBM Cloud Developer Tools

Install [IBM Cloud Developer Tools](https://cloud.ibm.com/docs/cli/index.html#overview) on your machine by using the following installation command: `curl -sL https://ibm.biz/idt-installer | bash`.

Your application will be compiled with Docker containers. To compile and run your app, run:

```bash
ibmcloud dev build
ibmcloud dev run
```

This will launch your application locally.  When you are ready to deploy to IBM Cloud on CloudFoundry or Kubernetes, run one of the commands below:

```bash
ibmcloud dev deploy -t buildpack
ibmcloud dev deploy -t container
```

You can build and debug your app locally with:

```bash
ibmcloud dev build --debug
ibmcloud dev debug
```

## Next Steps
* Learn more about augmenting your Swift applications on IBM Cloud with the [Swift Programming Guide](https://cloud.ibm.com/docs/swift).
* Explore [Kitura.io](https://www.kitura.io/) for more resources about the Kitura framework.
* Join the [Swift@IBM slack](http://swift-at-ibm-slack.mybluemix.net/) to get help with your projects.
* Explore other [sample applications](https://cloud.ibm.com/developer/appservice/starter-kits) on IBM Cloud.

## License

This sample application is licensed under the Apache License, Version 2. Separate third-party code objects invoked within this code pattern are licensed by their respective providers pursuant to their own separate licenses. Contributions are subject to the [Developer Certificate of Origin, Version 1.1](https://developercertificate.org/) and the [Apache License, Version 2](https://www.apache.org/licenses/LICENSE-2.0.txt).

[Apache License FAQ](https://www.apache.org/foundation/license-faq.html#WhatDoesItMEAN)
