# Getting Started

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app) and was extended to utilize the [Unlock Paywall](https://docs.unlock-protocol.com/tools/paywall/).

If this is the first time you have been introduced to [Unlock Protocol](https://unlock-protocol.com/) and you are an experienced developer then we suggest you start by dropping into the [Unlock Protocol Docs](https://docs.unlock-protocol.com/). We have less technical [Guides](https://unlock-protocol.com/guides/) which are geared more towards creators or people with less experience doing web development.

## Find Support

[Unlock Protocol Discord server](https://discord.com/invite/Ah6ZEJyTDp) is the best place to ask for support and technical questions are best asked in the developer channel where you'll find both Unlock Protocol core team members and community members ready to help you through whatever issues you may be having. In general you'll want to join us there for protocol updates, governance information and to connect with the greater Unlock Protocol ecosystem.

## Before configuration
Before you get started configuring your app you'll need a few important items.

### Deploying a Lock
You will need to deploy your own lock to use in the configuration below. If you haven't done that yet you can use the [Unlock Dashboard](https://app.unlock-protocol.com/dashboard). Documentation on how to deploy a lock via the dashboard can be found [here](https://docs.unlock-protocol.com/basics/deploying-a-lock). The current configuration file is preloaded with the Unlock Member lock so it will work out of the box but won't be very useful to you until you complete your lock deployment and update the configuration file.

### Unlock Accounts & Credit Cards

We understand with web3 not everyone is there yet and making it easier for users to get started is really the goal so your users don't have to be crypto native. For users of your app who may not have their own crypto wallet yet we've made it easy to create special [Unlock Accounts](https://docs.unlock-protocol.com/basics/unlock-accounts) and [enable payments via credit card](https://unlock-protocol.com/guides/enabling-credit-cards/).

## Unlock Specific Configuration

### Unlock Paywall
Currently the app utilizes the latest version of the [Unlock Paywall](https://docs.unlock-protocol.com/tools/paywall/) but you only need to change the link in the index.html to specify a specific version if that is what you need. We are dedicated to pushing breaking changes to a new url for the [Unlock Paywall](https://docs.unlock-protocol.com/tools/paywall/) so you shouldn't fear leaving it on latest.

In the public/index.html you will find an Unlock configuration object.

```JavaScript
<!-- Unlock Configuration -->
<script>
  var unlockProtocolConfig = {
      "network": 100, // Network ID (1 is for mainnet, 4 for rinkeby, 100 for xDai, etc)
      "locks": {
        "0xac1fceC2e4064CCd83ac8C9B0c9B8d944AB0D246": {
          "name": "Unlock Members"
        }
      },
      "icon": "https://unlock-protocol.com/static/images/svg/unlock-word-mark.svg",
      "callToAction": {
        "default": "Please unlock this demo!"
      }
    }
</script>
```

There are many different configuration options for the [Unlock Paywall](https://docs.unlock-protocol.com/tools/paywall/) and the complete documentation for those options can be found [here](https://docs.unlock-protocol.com/tools/paywall/configuring-checkout/).

### Unlock Event Listeners

You'll find we've added special event listeners in the src/App.js file. This is a very basic example which changes the visible content on a page when a user finishes the checkout or already has a key in their wallet and the state changes from "locked" to "unlocked".

## Deploying the app

Now that we've gone over the Unlock specific changes and configurations you should be ready to get started. In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `npm run build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
