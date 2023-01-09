# **NEXT Router**

Not like react, Next JS provides mechanisms for routing by default. By using the `useRouter();` hook, You can access the `router object` from any function component in your application.

### Next Router Object

-   _Router Object – Properties_

| Property Name | Data Type                               | Description                                                                                                                          |
| ------------- | --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| pathname      | String                                  | The path for the current route file that comes after '/'.                                                                            |
| query         | Object                                  | The query string parsed to an object, including [dynamic route](https://nextjs.org/docs/routing/dynamic-routes) parameters.          |
| asPath        | String                                  | The path shown in the browser, basePath not included.                                                                                |
| isFallback    | boolean                                 | Whether the current page is in [fallback mode](https://nextjs.org/docs/api-reference/data-fetching/get-static-paths#fallback-pages). |
| basePath      | String                                  | The active [basePath](https://nextjs.org/docs/api-reference/next.config.js/basepath) (if enabled).                                   |
| locale        | String                                  | The active locale (if enabled).                                                                                                      |
| locales       | String[]                                | All supported locales (if enabled).                                                                                                  |
| defaultLocale | String                                  | The current default locale (if enabled).                                                                                             |
| domainLocales | Array<{domain, defaultLocale, locales}> | Any configured domain locales.                                                                                                       |
| isReady       | boolean                                 | Indicate whether the router fields are updated client-side and ready for use.                                                        |
| isPreview     | boolean                                 | Indicate whether the application is currently in [preview mode](https://nextjs.org/docs/advanced-features/preview-mode).             |

-   _Router Object – Methods_

| Name        | Description                                                                                                                        |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| push();     | Handles client-side transitions, Useful for cases when [next/link](https://nextjs.org/docs/api-reference/next/link) is not enough. |
| replace();  | This will prevent adding a new URL entered into the history stack.                                                                 |
| prefetch(); | Prefetch pages for faster client-side transitions.                                                                                 |
| back();     | Go to the last page in history.                                                                                                    |
| reload();   | Reloads the page.                                                                                                                  |

-   _Router Object – Events_

| Name                                    | Description                                                                        |
| --------------------------------------- | ---------------------------------------------------------------------------------- |
| routeChangeStart(url, { shallow })      | Triggers when a route starts to change.                                            |
| routeChangeComplete(url, { shallow })   | Triggers when a route changed completely.                                          |
| routeChangeError(err, url, { shallow }) | Triggers when there's an error when changing routes, or a route load, is canceled. |
| beforeHistoryChange(url, { shallow })   | Triggers before changing the browser's history.                                    |
| hashChangeStart(url, { shallow })       | Triggers when the hash will change but not the page.                               |
| hashChangeComplete(url, { shallow })    | Triggers when the hash has changed but not the page.                               |

### Installation

`Next/Router` comes preinstalled when you create a next.js project. There’s no need to install it separately.

### Importing `Next/Router` into project

The `Next/Router` can be imported into a component as follows.

`import { useRouter } from 'next/router'`

### Accessing to router object

To access to the router object from component, You need to use `useRouter()` hook. You can get the router object as follows.

```
import { useRouter } from 'next/router'

function Component() {
  const router = useRouter()

  return (<h1>.....</h1>)
}

export default Component
```

## Read more

Read more details on Next/Router component in [Next.js Docs](https://nextjs.org/docs/api-reference/next/router)
