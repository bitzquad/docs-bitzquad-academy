# Routes in NEXT JS

## Introduction

Next JS has a relatively simple file-system like structure to handle routes. All routes start with a base directory(folder) `pages` in the project. When a file is added to this directory, it'll automatically become a route. There are three different ways to create a route in the next js project.

### Index Routes

The router will automatically detect files named index to the root of the directory and create a route.

-   → _folder path_ → `pages/index.js` → _route_ → `/`
-   → _folder path_ → `pages/blog/index.js` → _route_ → `/blog`

### Nested Routes

If you create a nested folder structure in the `pages` folder, files will automatically be routed in the same way as the nested folder structure.

-   → _folder path_ → `pages/blog/first-post.js` → _route_ → `/blog/first-post`
-   → _folder path_ → `pages/dashboard/settings/username.js` → _route_ → `/dashboard/settings/username`

### Dynamic Routes

This type of route is used to develop dynamic route structures. To match a dynamic segment, you can use the square bracket syntax. This allows you to match parameters in your dynamic route.

-   → _folder path_ → `pages/blog/[slug].js` → _route_ → `/blog/:slug` (/blog/hello-world)
-   → _folder path_ → `pages/[username]/settings.js` → _route_ → `/:username/settings` (/foo/settings)
-   → _folder path_ → `pages/post/[...all].js` → _route_ → `/post/\*` (/post/2020/id/title)

### How to retrieve parameters passed to dynamic routes

-   **Example 01**
    <br>
    Consider the following page `pages/blog/[slug].js`. In here `slug` is the parameter name.

```
import { useRouter } from 'next/router'

const BlogPost = () => {
    const router = useRouter()
    return <h1>Slug: {router.query.slug}</h1>
}

export default BlogPost
```

when you run the application and visit to `/blog/aricle1`, You'll see

```
 Slug: aricle1
```

in the rendered page.

-   **Example 02**
    <br>
    Consider the following page `pages/[username]/settings.js`. In here `username` is the parameter name.

```
import { useRouter } from 'next/router'

const SettingsPage = () => {
    const router = useRouter()
    return <h1>Username: {router.query.username}</h1>
}

export default SettingsPage
```

when you run the application and visit to `/bitzquad/settings`, You'll see

```
 Username: bitzquad
```

in the rendered page.
<br>

!!! info "In above examples you've seen how you can retrieve dynamic parameter from a next js dynamic route."

## Read more

Read more details about routing [Next.js Docs](https://nextjs.org/docs/routing/introduction)
