# Getting started building a Proof of Concept (POC)

This guide walks you through a simple, step-by-step process to set up your proof of concept and create a working application.

## 1. Understand the basics

* [What is OpenFin?](https://youtu.be/40bNqihjyXw?si=NjFSDaiKH513YEOq)
* Understand the key differences between [Container](https://developers.openfin.co/of-docs/docs/container-overview) and [Workspace](https://developers.openfin.co/of-docs/docs/overview-of-workspace)
* Key concepts:
  * [Interoperability model](https://developers.openfin.co/of-docs/docs/interoperability-overview)
  * [Notifications](https://developers.openfin.co/of-docs/docs/overview-notifications)
  * [Deployment model](https://developers.openfin.co/of-docs/docs/deploying-applications)

## 2. Use live demos

Access live demos to understand what your POC should aim to achieve.

### Workspace

[Basic workspace starter](https://start.openfin.co/?manifest=https%3A%2F%2Fbuilt-on-openfin.github.io%2Fworkspace-starter%2Fworkspace%2Fv19.0.0%2Fworkspace-platform-starter-basic%2Fmanifest.fin.json) - Simple application demonstrating fundamental features  
[Workspace platform Starter](https://start.openfin.co/?manifest=https%3A%2F%2Fbuilt-on-openfin.github.io%2Fworkspace-starter%2Fworkspace%2Fv19.0.0%2Fworkspace-platform-starter%2Fsecond.manifest.fin.json) - Fully featured application showing all available options

On first visit, download and run the installer to install the OpenFun runtime. On subsequent visits, applications will launch without requiring additional installation.

[View all workspace demos…](https://github.com/built-on-openfin/workspace-starter)

### Web

Access a platform in your default web browser.

[OpenFin Web](https://built-on-openfin.github.io/web-starter/web/v19.0.0/web-interop-support-context-and-intents/platform/provider.html)  
(Access separate workspaces in the Layout dropdown at the top right)

[More Web demos…](https://github.com/built-on-openfin/web-starter)

## 3. Set up a starter project

Next, set up a starter project on your local computer.

OpenFin development is based on web technologies, such as JavaScript, Node.js, and NPM and will be straightforward to set up for developers familiar with this development environment.

### Prerequisites

First, ensure your network can access the necessary OpenFin endpoints: [Health Check](https://cdn.openfin.co/health/deployment/index.html)

Install development tooling:  
[NodeJS](https://nodejs.org/en/download/package-manager) (Current LTS version recommended)  
[OpenFin RVM](https://developer.openfin.co/versions/?product=RVM) - if you installed one of the live workspace demos above you will have installed the RVM

Windows and Mac are both supported for development.

[More information...](https://developers.openfin.co/of-docs/docs/set-up-your-dev-environment)

### Starter projects

We recommend using a starter project to bootstrap your POC. Choose the project that most closely suits your needs.

<details>
<summary>Workspace platform starter - basic (recommended)</summary>

Demonstrates a basic OpenFin workspace platform. 

Take note of the `client/src/provider.ts` file to observe how to initialize the platform and launch apps. And `public/manifest.fin.json` to configure a platform.

Set up the starter for local development:
```sh
git clone https://github.com/built-on-openfin/workspace-starter.git --depth=1
cd workspace-starter/how-to/workspace-platform-starter-basic
npm install
npm run build
npm start

//in a separate terminal
cd workspace-starter/how-to/workspace-platform-starter-basic
npm run client
```

Once loaded, the Home screen will appear with a prompt: *What would you like to do?*

Press the enter key to see all the available apps.

[More information…](https://github.com/built-on-openfin/workspace-starter/tree/main/how-to/workspace-platform-starter-basic)
</details>

<details>
<summary>Workspace platform starter</summary>

Demonstrates a fully-featured OpenFin workspace platform demonstrating advanced use cases.

The features are encapsulated into modules, see `client/src/modules`

Set up the starter for local development:
```sh
git clone https://github.com/built-on-openfin/workspace-starter.git --depth=1
cd workspace-starter/how-to/workspace-platform-starter
npm run setup
npm start

//in a separate terminal
cd workspace-starter/how-to/workspace-platform-starter
npm run client
```

Once initialized the Home screen and Dock will appear. From the Dock, explore the various options.

*Note, Mac or WSL users may experience some issues when building the applications. A Windows PC is recommended.*

[More information…](https://github.com/built-on-openfin/workspace-starter/tree/main/how-to/workspace-platform-starter)
</details>

<details>
<summary>Front-end framework starter</summary>

A basic application showing how to boostrap an OpenFin container or workspace using front-end frameworks (React or Angular).

Set up the starter for local development:
```sh
git clone https://github.com/built-on-openfin/frontend-framework-starter.git --depth=1
cd frontend-framework-starter/frameworks/react/workspace  // Or angular
npm install
npm start

//in a separate terminal
cd frontend-framework-starter/frameworks/react
npm run client
```

Once loaded, the Home screen will appear with a prompt: *What would you like to do?*

Press the enter key to see all the available apps.

[More information…](https://github.com/built-on-openfin/frontend-framework-starter)
</details>

<details>
<summary>OpenFin Web starter</summary>

An OpenFin workspace running in your default browser, demonstrating Interop and Layout features.

Set up the starter for local development:
```sh
git clone https://github.com/built-on-openfin/web-starter.git --depth=1
cd web-starter
npm install
npm run build
cd how-to/web-layout // or any subfolder of your choice
npm start

//in a separate terminal
npm run client
```

Your default browser will load the platform, otherwise visit [http://localhost:6060/platform/provider.html](http://localhost:6060/platform/provider.html)

*Note, Mac or WSL users may experience some issues when building the applications. A Windows PC is recommended.*

[More information…](https://github.com/built-on-openfin/web-starter)
</details>

[Additional starters...](https://github.com/built-on-openfin/workspace-starter/tree/main/how-to)

### Customize your POC

Once setup, you can begin to experiment with the features to create your proof of concept.

They key concepts to experiment with are:

- [Defining apps](https://github.com/built-on-openfin/workspace-starter/blob/main/how-to/workspace-platform-starter/docs/how-to-define-apps.md)
- [Notifications](https://github.com/built-on-openfin/workspace-starter/blob/main/how-to/workspace-platform-starter/docs/how-to-use-notifications.md)
- [Interop](https://github.com/built-on-openfin/workspace-starter/blob/main/how-to/workspace-platform-starter/docs/how-to-customize-your-interop-broker.md)
- [Authentication](https://github.com/built-on-openfin/workspace-starter/blob/main/how-to/workspace-platform-starter/docs/how-to-authenticate.md)
- [FCD3](https://github.com/built-on-openfin/workspace-starter/blob/main/how-to/workspace-platform-starter/docs/what-is-fdc3.md)
- [More…](https://github.com/built-on-openfin/workspace-starter/tree/main/how-to/workspace-platform-starter/docs)

## 4. Deploy your POC

### Prerequisites

The only infrastructure required is a server to host your web applications and the manifest.json files.

Any server capable of hosting static assets via HTTP will work, for example a CDN, AWS, Nginx, Apache, IIS, SharePoint, GitHub Pages etc.

### Deploy your web apps

Build the static assets:

```
npm run build
```

Deploy the contents of the `public` folder to your web host.

Ensure the urls in your manifest are valid and deploy your manifest files - they can be hosted with your web apps or separately.

### Create an installer

Create an installer file to distribute to your users which contains the RVM.

[https://install.openfin.co/](https://install.openfin.co/)

Alternatively send a [fins link](https://developers.openfin.co/of-docs/docs/deep-linking) to your users

[More information...](https://developers.openfin.co/of-docs/docs/deploying-applications)

## 5. Advanced topics and more information

[How to guides](https://github.com/built-on-openfin/workspace-starter/tree/main/how-to/workspace-platform-starter/docs)

[Hints and tips](https://github.com/built-on-openfin/workspace-starter/tree/main/how-to/hints-and-tips)
