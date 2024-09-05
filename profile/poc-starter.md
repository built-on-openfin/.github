# Getting started building a Proof of Concept (POC)

This guide walks you though setting up a proof of concept.

It follows a step by step process using the simplest possible path to creating a working application.

## Understand the basics

[Videos, product demos, and webinars](https://www.openfin.co/on-demand/)

[Unifying you Notifications Experience](https://www.openfin.co/on-demand/?wchannelid=qfzzhxnygo&wmediaid=3m5b0o78va)

## **Access Live Demos**

Hosted examples are available to quickly install and use without setting up a development environment. 

### Workspace

Download and run the installer if you do not yet have the Runtime Version Manager (RVM) installed. On subsequent visits applications will launch without requiring additional installation.

[Basic workspace starter](https://start.openfin.co/?manifest=https%3A%2F%2Fbuilt-on-openfin.github.io%2Fworkspace-starter%2Fworkspace%2Fv19.0.0%2Fworkspace-platform-starter-basic%2Fmanifest.fin.json) - Simple application demonstrating fundamental features  
[Workspace Platform Starter](https://start.openfin.co/?manifest=https%3A%2F%2Fbuilt-on-openfin.github.io%2Fworkspace-starter%2Fworkspace%2Fv19.0.0%2Fworkspace-platform-starter-basic%2Fmanifest.fin.json) - Fully featured application showing all available options 
  
[More workspace demos…](https://github.com/built-on-openfin/workspace-starter)  

### Web

Simply click on the link and access the platform in a web browser.

You can see various workspaces in the Layout dropdown at the top right

[OpenFin Web](https://built-on-openfin.github.io/web-starter/web/v19.0.0/web-interop-support-context-and-intents/platform/provider.html) - The best features of OpenFin in your web browser
  
[More Web demos…](https://github.com/built-on-openfin/web-starter)

## Set up starter project

Setup a starter project on your local computer

### Prerequisites

[NodeJS](https://nodejs.org/en/download/package-manager) (Current LTS version recommended)

[OpenFin RVM](https://developer.openfin.co/versions/?product=RVM) - if you installed one of the live workspace demos above you will have installed the RVM

### Starter projects

<details>
<summary>Set up Workspace platform starter - basic (recommended)</summary>

```jsx
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
<summary>Set up Workspace platform starter</summary> 

```jsx
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
<summary>Set up front-end framework starter</summary> 

```jsx
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
<summary>Set up OpenFin Web starter</summary> 

```jsx
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

### Customize

Once setup, you can begin to experiment with the features to create your proof of concept.

- [Notifications](https://github.com/built-on-openfin/workspace-starter/blob/main/how-to/workspace-platform-starter/docs/how-to-use-notifications.md)
- [Interop](https://github.com/built-on-openfin/workspace-starter/blob/main/how-to/workspace-platform-starter/docs/how-to-customize-your-interop-broker.md)
- [More…](https://github.com/built-on-openfin/workspace-starter/tree/main/how-to/workspace-platform-starter/docs)

## Deploy your POC

### Prerequisites

The only infrastructure required is a server to host your web applications and the manifest.json files.

Any server capable of hosting static assets via HTTP will work, for example a CDN, AWS, Nginx, Apache, IIS, SharePoint, GitHub Pages etc.

### Deploy your web apps

Build the static assets:

```jsx
npm run build
```

Deploy the contents of the `public` folder to your web host.

### Create an installer

Create an installer file to distribute to your users which contains the RVM.

[https://install.openfin.co/](https://install.openfin.co/)

Alternatively send a `fins` link to your users - [more information here](https://developers.openfin.co/of-docs/docs/deep-linking).

## Advanced topics and more information

[How to guides](https://github.com/built-on-openfin/workspace-starter/tree/main/how-to/workspace-platform-starter/docs)

[Hints and tips](https://github.com/built-on-openfin/workspace-starter/tree/main/how-to/hints-and-tips)
