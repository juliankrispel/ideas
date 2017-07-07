A 0-config staging environment for react components

I took a stab at this a couple of times but it's hard and it might be better to just use storybook.

The idea is thus:

You have a component somewhere in your app and you want to run it in isolation right now!

```
sketchbook ./some-component.js
```

And there you go, we start a small dev server, launch your browser and mount your component.

Pain points:

- The build system needs to be the same.
- The tool would need to interpret accepted inputs to make the component work
