<h1 align="center">useDeviceOptions</h1>

Need to know when you're *on the server*, *in the browser* or in *react native* in your components/hooks? This simple hook makes it easy. 🔥

Features
--------
- SSR (server side rendering) support
- TypeScript support
- Zero dependencies
- React Native support

Installation
------------

```shell
yarn add use-ssr      or     npm i -S use-ssr
```

Usage
-----

```jsx
import useDeviceOptions from 'use-device-options'

const App = () => {
  var { isBrowser, isServer, isNative } = useDeviceOptions()
  
  
  /*
   * In your browser's chrome devtools console you should see
   * > IS BROWSER: 👍
   * > IS SERVER: 👎
   *
   * AND, in your terminal where your server is running you should see
   * > IS BROWSER: 👎
   * > IS SERVER: 👍
   */
  console.log('IS BROWSER: ', isBrowser ? '👍' : '👎')
  console.log('IS SERVER: ', isServer ? '👍' : '👎')
  console.log('IS NATIVE: ', isNative ? '👍' : '👎')
  return (
    <>
      Is in browser? {isBrowser ? '👍' : '👎'}
      <br />
      Is on server? {isServer ? '👍' : '👎'}
      <br />
      Is react native? {isNative ? '👍' : '👎'}
    </>
  )
}
```

Options
-------

```js
const {
  isBrowser,
  isServer,
  isNative,
  device, // 'server', 'browser', or 'native'
  canUseWorkers,
  canUseEventListeners,
  canUseViewport,
} = useDeviceOptions()
```
