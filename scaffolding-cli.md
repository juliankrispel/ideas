Problem:

I, and many other react devs never use scaffolds or boilerplates because they either come with too much stuff that I don't need, or too little.

What if there was a tool that made it very straightforward to write scaffolds.

Here's a little brainfart:

A very simple cli that just copies templates for you.

Say you have a repo. That repo has a `templates` folder.

The cli picks up the templates folder and will use that to create stuff:

`scaffold component ./src/components/SomeComponent`

Then it asks you questions to customize the component:
- Do you want a tests folder?
- Do you want a styles?
- Do you want this or that?
