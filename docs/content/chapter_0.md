## **React & Next Js**

<figure markdown>
![Next vs React](../img/chap_0/nextjs-vs-react.png){width="700"}
</figure>

-   ### **About Next**

    Next.js is an open-source web development framework created by Vercel enabling React-based web applications with server-side rendering and generating static websites.
    <!-- <br /><br />Read more - <a href="https://en.wikipedia.org/wiki/Next.js" target="_blank">https://en.wikipedia.org/wiki/Next.js</a> -->

    <br />Documentation - <a href="https://nextjs.org/" target="_blank">https://nextjs.org/</a>

-   ### **Why Next JS?**

    Next JS is used to create web applications and performs server-side rendering, whereas React JS focuses on rendering toward the DOM. Next JS offers server-side rendering (SSR), whereas Create React App offers client-side rendering, improving the application performance. It is open source, and SEO friendly.

    | Advantages                                                         | Disadvantages                                                                   |
    | ------------------------------------------------------------------ | ------------------------------------------------------------------------------- |
    | Excellent performance in terms of load times                       | Some developers find it too opinionated                                         |
    | Supports SSG, SSR and Client-Side rendering                        | Multiple developers complain about how Next.js does routing, others champion it |
    | Fantastic user-experience                                          |                                                                                 |
    | Great SEO                                                          |                                                                                 |
    | Easy customization                                                 |                                                                                 |
    | Rapid feature development                                          |                                                                                 |
    | Great community support                                            |                                                                                 |
    | Load times helped with “lazy loading” and automatic code splitting |                                                                                 |

    <br />Read more about advantages and disadvantages - <a href=" https://dev.to/richkurtzman/advantages-and-disadvantages-of-nextjs-5hg6" target="_blank"> https://dev.to/richkurtzman/advantages-and-disadvantages-of-nextjs-5hg6</a>

-   ### **React vs. Next js, what are the differences?**

    React is one of the most used front-end libraries, allowing developers to create reusable UI components, maintained by Facebook. React is an easy-to-use front-end library that offers various useful tools to enclose routing and <u><a href="#state-management-with-next-js"> state management</a></u> patterns alongside Redux and other libraries. React is a JavaScript library that allows developers to build user interfaces. A user interface (UI) is a combination of HTML and JavaScript that contains all of the logic needed to display a tiny piece of a bigger UI. ( Other javascript libriaries - Vue JS, Angular, Svelte )<br /><br />Next JS is a JavaScript framework that allows developers to create user-friendly and blazing-fast static websites and static web applications with React. Next, JS is an open-source, lightweight web development framework for React applications. It allows developers to build server-side rendering.

    <br />Read more - <a href="https://radixweb.com/blog/nextjs-vs-react" target="_blank">https://radixweb.com/blog/nextjs-vs-react</a>

-   ### **What are the main areas of next js & react that you need to know to contribute to this project?**

    -   **Hooks**

        | Name           | Description                                                                                                                                                                                 | References                                                                                                                              |
        | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
        | `useState();`  | This React hook store a value(state) in a component.                                                                                                                                        | <a href="https://reactjs.org/docs/hooks-state.html" target="_blank">https://reactjs.org/docs/hooks-state.html</a>                       |
        | `useEffect();` | This hook will trigger when the DOM in a component changes. You can specify what variables trigger this hook by passing variables as an array to the hook.                                  | <a href="https://reactjs.org/docs/hooks-effect.htm" target="_blank">https://reactjs.org/docs/hooks-effect.html</a>                      |
        | `useRef();`    | This hook allows you to access the DOM element directly. And you can read and mutate its properties.                                                                                        | <a href="https://reactjs.org/docs/hooks-reference.html#useref" target="_blank">https://reactjs.org/docs/hooks-reference.html#useref</a> |
        | `useRouter();` | This next hook enables you to access the 'router object' from any component in your app. Used to handle client-side transitions such as navigation between pages, redirection, reload, etc. | <a href="https://nextjs.org/docs/api-reference/next/router" target="_blank">https://nextjs.org/docs/api-reference/next/router</a>       |

    -   **SSR & SSG**

        | Name                         | Description                                                                                                                  | References                                                                                                                                                          |
        | ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | SSR (Server Side Rendering)  | Build (render) page on the server at the time of request (pre-rendering) and serves the page as the response to the request. | <a href="https://nextjs.org/docs/basic-features/pages#server-side-rendering" target="_blank">https://nextjs.org/docs/basic-features/pages#server-side-rendering</a> |
        | SSG (Static Site Generation) | Build (render) page on application build time (static-site generation) and serve requested page from the app build cache.    | <a href="https://nextjs.org/docs/basic-features/pages#static-generation" target="_blank">https://nextjs.org/docs/basic-featurespages#static-generation</a>          |

    -   **Data fetching with next**

        | Method                                  | Description                                                                                                                            | References                                                                                                                                                                                                |
        | --------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | `getServerSideProps();`                 | The page will be pre-rendered at runtime.                                                                                              | <a href="https://nextjs.org/docs/basic-features/data-fetching/get-server-side-props" target="_blank">https://nextjs.org/docs/basic-features/data-fetching/get-server-side-props</a>                       |
        | `getStaticProps();`                     | The page will be pre-rendered at build time                                                                                            | <a href="https://nextjs.org/docs/basic-features/data-fetching/get-static-props" target="_blank">https://nextjs.org/docs/basic-features/data-fetching/get-static-props</a>                                 |
        | `getStaticPaths();`                     | This function generates a list of pages that will be pre-rendered at build time                                                        | <a href="https://nextjs.org/docs/basic-features/data-fetching/get-static-path" target="_blank">https://nextjs.org/docs/basic-features/data-fetching/get-static-path</a>                                   |
        | `Incremental Static Regeneration (ISR)` | If the page isn't statically generated at the build-time this enables you to build that page runtime (once) and severs from the cache. | <a href=" https://nextjs.org/docs/basic-features/data-fetching/incremental-static-regeneration" target="_blank"> https://nextjs.org/docs/basic-features/data-fetching/incremental-static-regeneration</a> |
        | `Client-side data fetching`             | Fetch data from the client side.                                                                                                       | <a href="https://nextjs.org/docs/basic-features/data-fetching/client-side" target="_blank">https://nextjs.org/docs/basic-features/data-fetching/client-side</a>                                           |

        -   ### **State management with Next JS**

            State management is the process of keeping and handling data in an application or a component. In the next js, managing states in a component are exactly similar to react.

            In a react component, data is typically stored in the component's state object. When the state changes the component or the page will re-render.

        -   ### **Functional Components**

            You can create react component as a function. This is the simplest way to define a component. This function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element.

            !!! warning "Remember, We don't use _Class Components_ for this project."

## **Tailwind CSS**

<figure markdown>
![Tailwind CSS](../img/chap_0/tailwind.png)
</figure>

-   ### **About Tailwind**

    Tailwind CSS is an open-source CSS framework. The main feature of this library is that, unlike other CSS frameworks like Bootstrap, it does not provide a series of predefined classes for elements such as buttons or tables.

-   ### **Why Tailwind**
    
    Tailwind CSS makes it quicker to write and maintain the code of the application. By using this utility-first framework, We don’t have to write custom CSS to style our application. Instead, we can use utility classes to control the padding, margin, color, font, shadow, and more of the application.

    - **Advantages of using Tailwind CSS**
        
        - Ease to build responsive websites.
        - We can add custom css utilities.
        - Remove unused css when it comes to production build.

    <br />Documentation - <a href="https://tailwindcss.com/" target="_blank">https://tailwindcss.com/</a>
    <br />UI library - <a href="https://tailwindui.com/" target="_blank">https://tailwindui.com/</a>

    !!! info "Important!"
        - You must read the core concepts in the Tailwind documentation to get a better idea of how hover, focus, and other important states work.


<small>image credits goes to respective owners</small>
