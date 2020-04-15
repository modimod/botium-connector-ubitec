# Botium Connector for Ubitec

[![NPM](https://nodei.co/npm/botium-connector-ubitec.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/botium-connector-ubitec/)

[![npm version](https://badge.fury.io/js/botium-connector-ubitec.svg)](https://badge.fury.io/js/botium-connector-ubitec)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg)]()


This is a [Botium](https://github.com/codeforequity-at/botium-core) connector for testing your Ubitec chatbot.

__Did you read the [Botium in a Nutshell](https://medium.com/@floriantreml/botium-in-a-nutshell-part-1-overview-f8d0ceaf8fb4) articles? Be warned, without prior knowledge of Botium you won't be able to properly use this library!__

## How it works
Botium connects to the API of your Ubitec chatbot.

It can be used as any other Botium connector with all Botium Stack components:
* [Botium CLI](https://github.com/codeforequity-at/botium-cli/)
* [Botium Bindings](https://github.com/codeforequity-at/botium-bindings/)
* [Botium Box](https://www.botium.at)

## Requirements
* **Node.js and NPM**
* a **Ubitec bot**
* a **project directory** on your workstation to hold test cases and Botium configuration

## Install Botium and Ubitec Connector

When using __Botium CLI__:

```
> npm install -g botium-cli
> npm install -g botium-connector-ubitec
> botium-cli init
> botium-cli run
```

When using __Botium Bindings__:

```
> npm install -g botium-bindings
> npm install -g botium-connector-ubitec
> botium-bindings init mocha
> npm install && npm run mocha
```

When using __Botium Box__:

_Already integrated into Botium Box, no setup required_

## Connecting Ubitec chatbot to Botium

Process is very simple, you have to know just the endpoint URL for your chatbot.
  
Create a botium.json with this URL in your project directory: 

```
{
  "botium": {
    "Capabilities": {
      "PROJECTNAME": "<whatever>",
      "CONTAINERMODE": "ubitec",
      "UBITEC_URL": "..."
    }
  }
}
```

To check the configuration, run the emulator (Botium CLI required) to bring up a chat interface in your terminal window:

```
> botium-cli emulator
```

Botium setup is ready, you can begin to write your [BotiumScript](https://github.com/codeforequity-at/botium-core/wiki/Botium-Scripting) files.

## How to start samples

There is a sample available in [samples](./samples) with Botium Bindings.

* Adapt botium.json in the sample directory if required (change URL)
* Install packages, run the test

```
> cd ./samples
> npm install && npm test
```

## Supported Capabilities

Set the capability __CONTAINERMODE__ to __ubitec__ to activate this connector.

### UBITEC_URL
Ubitec chatbot endpoint url

### UBITEC_USER
Ubitec chatbot user

### UBITEC_PASSWORD
Ubitec chatbot password
