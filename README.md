# live-cam-bot

[Electron](https://electron.atom.io/)-based Bot utilizing the [setScreenshareStream](https://circuitsandbox.net/sdk/classes/Client.html#method_setScreenshareStream) API to send a video stream captured from a local camera.

This example would be suited to run on a Raspberry PI with a local camera and wifi. The PI could then be used for surveillance, local surf conditions or anything else you'd like to share.

> Electron is based on node.js and Chromium and is therefore able to utilize the Circuit JS WebRTC APIs unlike a regular node.js app.

## Details
* Group conversation to stream video on is predefined and its ID set in config.json 
* Bot will start (or join) conference on given conversation and share the video stream of the local camera. If non default camera is to be used, [setMediaDevices](https://circuitsandbox.net/sdk/classes/Client.html#method_setMediaDevices) can be used to choose a video input device.
* Bot will ensure the conference is always running

## Getting Started

* [Register an account](https://www.circuit.com/web/developers/registration) on circuitsandbox.net (if you didn't yet)
* [Register a bot](http://circuit.github.io/oauth) on the sandbox (OAuth 2.0 Client Credentials)

### Run the app

> This example uses async/await, so node.js version 7.6+ is required

```bash
    git clone https://github.com/circuit/live-cam-bot.git
    cd live-cam-bot
    cp config.json.template config.json
    // Edit config.json with your credentials and the conversation ID to stream on
    npm install
    npm start // or npm run dev
```

> When running using "npm start" no window is opened. Run using "npm run dev" if you want to debug the app.
