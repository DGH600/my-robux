# Toxic Rainer
## _Auto-BloxFlip Rain Joiner_


Toxic Rainer is a web-socket based background running program used to automatically join BloxFlip Rains

- Run 24/7 with no delay
- No hardware utilization, hence no heating up of PC.

## Features

- Custom Discord webhook logger
- Auto join/leave
- Trivia notifier
- Windows notification
- Super stealthy

## Why was this project made?
> The main goal behind creation of such a program was to provide free robux to people who can't afford it. [EzRain]() as well sells this, but at unfairingly overpriced, and therefore I wanted to contribute whatever I could!

## __Setup__

Setting up the program is super easy! Firstly, click the green colored button above and Click `Download ZIP`. Unzip the file and do as follow

<details>
<summary> Installing Node </summary>

- Download the latest version of NodeJS from [here](https://nodejs.org/dist/v16.16.0/node-v16.16.0-x64.msi)

</details>
<details>
    <summary> Getting your [BloxFlip](https://bloxflip.com/) Authentication </summary>
- Go to [Bloxflip](https://bloxflip.com/) and then press `CTRL+SHIFT+I` or `F12` or just open Developer tools
- Navigate to `console` and enter the following code.

<details>
  <summary>Code</summary>
</details>
```js
localStorage.getItem('_DO_NOT_SHARE_BLOXFLIP_TOKEN')
```
</details>

<details>
<summary>Editing config.json</summary>

All the keys are required and is case sensitive.
| Key | Value |
| ------ | ------ |
| auth | Your BloxFlip Authentication, without ' |
| webhook | Discord webhook, starting with `https://` |
| win_notif | Enable/Disable notification [Windows only]. (Boolean) |
| product | Browser name. `chrome` or `firefox` [Case sensitive] |
| path | Path of your browser. Right click browser and click properties, copy path and add `\` before ever `\` Eg. |

</details>


Dillinger requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
cd dillinger
npm i
node app
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
```

## Plugins

Dillinger is currently extended with the following plugins.
Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:

```sh
node app
```

Second Tab:

```sh
gulp watch
```

(optional) Third:

```sh
karma test
```

#### Building for source

For production release:

```sh
gulp build --prod
```

Generating pre-built zip archives for distribution:

```sh
gulp build dist --prod
``
