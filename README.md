# next-fbq

Next.js High Order Component to integrate Facebook Pixel on every page change.

## Usage

Install it

```bash
yarn add next-fbq
```

Import it inside your `pages/_app.js`;

```js
import withFBQ from "next-fbq";
```

Wrap your [custom App container](https://nextjs.org/docs#custom-%3Capp%3E) with it

```js
// pass your Facebook Pixel code as first argument
export default withFBQ("139xxxxxxxxx3")(MyApp);
```

That's it, now when the user access a page it will log a pageview to Facebook Pixel, each page change after that will also trigger a pageview on GA.

> **Note**: This module detects if it's running in localhost and do nothing there to avoid polluting your analytics with local data.


# Credits

This is a complete copy of [@sergiodxa](https://github.com/sergiodxa) Google Analytics implementation [next-ga](https://github.com/sergiodxa/next-ga/blob/master/src/analytics.js) adapted to the Facebok Pixel
