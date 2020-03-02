<h1 align="center">useDeviceOptions</h1>

Need to know when you're *on the server*, *in the browser* or in *react native* in your components/hooks?

Features
--------
- SSR (server side rendering) support
- TypeScript support
- Zero dependencies
- React Native support

Installation
------------

- using Yarn
```shell
yarn add use-device-options
```
- using npm
```shell
npm i -S use-device-options
```

Usage
-------

```js
import useDeviceOptions from 'use-device-options';
export const App = () => {

    const {
      isBrowser,
      isServer,
      isNative,
      device, // 'server', 'browser', or 'native'
      canUseWorkers,
      canUseEventListeners,
      canUseViewport,
    } = useDeviceOptions();

}
```
