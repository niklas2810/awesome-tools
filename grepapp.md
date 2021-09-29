# grep.app - Google for GitHub repositories

[grep.app](https://grep.app) is a search engine which stores half a million GitHub repositories.

Using it is especially useful when you are familiar with the language itself, but need to use a 
certain function, library, etc. and forgot how the syntax works, or how to do something specific.

Let's take my example, I wanted to use computed properties inside of Vue 3's components. And all
I knew was the following:

1. The file I'm looking for will most probably start with `<template>` (this is where you define your HTML markup).
2. Somewhere in the file, there will be sth. like `export default defineComponent() {`, which begins the start of the component's code.
3. Finally, inside of the function there will be a member called `computed` (this is what I'm looking for!

Using a regular expressions, which are supported by grep.app, I came up with the following: `<template>(.|\n)*defineComponent(.|\n)*computed:`
You can see the results [here](https://grep.app/search?q=%3Ctemplate%3E%28.%7C%5Cn%29%2AdefineComponent%28.%7C%5Cn%29%2Acomputed%3A&regexp=true).

And voila, the first result was exactly the type of [code](https://github.com/hoppscotch/hoppscotch/blob/main/packages/hoppscotch-app/components/smart/Icon.vue)
I was looking for!
