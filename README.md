# embedDiscordNextJs
how to embed a free discord chat floating widget on your nextjs application. Widgetbot can do this for us -for free! 
below are example screenshots. the colors, position, etc can be easily customized. check widgetbot links for that, given in this article.

###### before clicking crate
![image](https://user-images.githubusercontent.com/88471847/157035252-44e8d0a7-28cb-4067-bd30-e012501019c1.png)

###### after clicking crate
![image](https://user-images.githubusercontent.com/88471847/157035570-5facd093-7bcc-4a50-81d2-2b90c2cafc58.png)


# Steps:

### First,
create a public server in discord. [create now](https://www.alphr.com/how-to-make-a-discord-server/). Its totally free :)

### Secondly,
Go to widgetbot and register a free bot. See this [widgetbot tutorial](https://docs.widgetbot.io/tutorial/). This bot lets us embed public chat to our applications ;) 

### Finally,
open your __app.tsx__ file and take reference from the below example:
```
import "../styles/globals.css";
import type { AppProps } from "next/app";
import Head from "next/head";
import Script from "next/script";
function MyApp({ Component, pageProps }: AppProps) {
  return (
    <>
      <Script
        id="123"
        src="https://cdn.jsdelivr.net/npm/@widgetbot/crate@3"
        async
        defer
      >
        {
          // this creates live discord icon
          ``new Crate({
        server: "914576532293447700",
        channel: "914576605148483605",
        color: 'navy'
      })``
        }
      </Script>
      <Component {...pageProps} />
    </>
  );
}

export default MyApp;
```

This is it!

