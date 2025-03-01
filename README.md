# Repro leaking default error page

1. Run `yarn install`
2. Run `yarn dev`
3. Visit `localhost:3000/`, on which you can see our "beautiful" custom body styling
4. Visit a non existing page, e.g. `localhost:3000/oops`. NextJS applies their error styling to the body, messing with our custom styling. Basically the content in the layout is affected, while it should only be constrained to the children of the layout.
