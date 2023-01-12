# NEXT / Link

## Introduction

The Next.js Link component [next/link](https://nextjs.org/docs/api-reference/next/link) handles client-side transitions between routes. This component basically acts like HTML `<a>` tag, but there are a few differences.

~Next.js Docs

## **\*\*\*\***Advantages of Next/Link**\*\*\*\***

-   Include preloading page/s
-   Not involve full page reloads
-   Faster navigation
-   Very significant application performance and better user experience

## Using Next/Link

### Installation

Next/Link comes preinstalled when you create a next.js project. There’s no need to install it separately.

### Importing into project

The Next/Link component can be imported into a page as follows.

`import Link from 'next/link'`

### Required Props

The `Link` component has 9 props, but only one prop is a required prop.

1. href (required)
2. as
3. legacyBehavior
4. passHref
5. prefetch
6. replace
7. scroll
8. shallow
9. locale

### **href** (Required)

The path or URL that you need to navigate to. This is the only required prop. And you can pass the URL as an object.

-   **Pass URL/path as string**

```
    import Link from 'next/link'
    function Home() {
    return (
        <ul>
            <li>
                <Link href="/">Home</Link>
            </li>
            <li>
                <Link href="/about">About Us</Link>
            </li>
            <li>
                <Link href="/blog/hello-world">Blog Post</Link>
            </li>
        </ul>
        )
    }
    export default Home
```

-   **Pass URL/path as object**

```
    import Link from 'next/link'
    function Home() {
    return (
        <ul>
            <li>
                <Link href={
                        {
                        pathname: '/blog/[slug]',
                        query: { slug: 'my-post' },
                        }
                    }>Blog Post</Link>
            </li>
        </ul>
        )
    }
    export default Home
```

### **as** (Optional)

Optional decorator for the path that will be shown in the browser URL bar.

### **legacyBehavior** (Optional)

Changes behavior so that child must be `<a>`. If the child of Link is a custom component that wraps an `<a>` tag, you must add passHref to Link. Without using this `<a>` tag and legacy behavior, might affect on site's SEO and accessibility. [Read more about legacy behavior](https://nextjs.org/docs/api-reference/next/link#if-the-child-is-a-tag)

### **passHref** (Optional)

Forces Link to send the `href` property to its child. Defaults to `false`.

### **prefetch** (Optional)

Prefetch the page in the background. Defaults to true. Any `<Link />` that is in the viewport (initially or through scroll) will be preloaded. Prefetch can be disabled by passing `prefetch={false}`. When prefetch is set to false, prefetching will still occur on hover. Pages using <a href="/content/chapter_0/#what-are-the-main-areas-of-next-js-react-that-you-need-to-know-to-contribute-to-this-project">Static Generation</a> will preload JSON files with the data for faster page transitions. Prefetching is only enabled in production.

### **replace** (Optional)

This will prevent adding a new URL entered into the history stack. Defaults to `false`.

### **scroll** (Optional)

Scroll to the top of the page after a navigation. Defaults to `true`.

### **shallow** (Optional)

Update the path of the current page without re-running <a href="/content/chapter_0/#what-are-the-main-areas-of-next-js-react-that-you-need-to-know-to-contribute-to-this-project">getStaticProps</a>, <a href="/content/chapter_0/#what-are-the-main-areas-of-next-js-react-that-you-need-to-know-to-contribute-to-this-project">getServerSideProps</a> or <a href="/content/chapter_0/#what-are-the-main-areas-of-next-js-react-that-you-need-to-know-to-contribute-to-this-project">getInitialProps</a>. Defaults to `false`.

### **locale** (Optional)

The active locale is automatically prepended. locale allows for providing a different locale. When false href has to include the locale as the default behavior is disabled.

## Read more

Read more details on Next/Link component in [Next.js Docs](https://nextjs.org/docs/api-reference/next/link)
