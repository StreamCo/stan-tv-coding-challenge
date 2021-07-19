# Stan TV Coding Challenge

> Welcome to the Stan TV Coding Challenge!

## Overview

The purpose of this challenge is to assess your knowledge around composing a **simple React/Typescript single-page application** following the guidelines and requirements.

This challenge is expected to take around 4 hours.

## Guidelines

- You should use the provided Stan logo [logo.svg](./logo.svg).
- The **deployable** solution should be built in a folder named **`dist`** with an entry point file of **`index.html`**.
- Your solution should be built using [TypeScript](https://www.typescriptlang.org) and [React](https://facebook.github.io/react/)
- You should avoid using any additional third party CSS frameworks or JS libraries.
- The app should be responsive and support both 720p and 1080p screen sizes.
- We are looking for solutions that are **simple, well-designed, performant, and tested**

## Requirements

You will need to build the following 2 pages with React:

- A "Home" page [home.jpg](./home.jpg)
- A "Program" page [program.jpg](./program.jpg)

### "Home" Page

- This page should consist of the layout along with a **simple** carousel.
- You will need to fetch the provided sample data in [data.json](./data.json)
- Each item in the carousel should link to a "Program" page.
- Navigation between items in the carousel should be handled using the `left`, `right` and `enter` keyboard keys.
- No more than ten carousel items should be in the DOM at any time.
- When there are no carousel items to display (or an error occurs) the carousel should not render anything.

### "Program" Page

- This page should consist of the layout along with a program overview.
- The program to display should be determined by the ID.
- You should only fetch the provided sample data if the "Home" page has not been visited first.
- Pressing the `backspace` keyboard key should take you back to the "Home" page.

## Other Notes

Please also include a `README` with setup instructions, and any tests or other documentation you created as part of your solution.

Also, add the following info to your `README`:

- How did you decide on the technical and architectural choices used as part of your solution?
- Are there any improvements you could make to your submission?
- What would you do differently if you were allocated more time?

Please also send through any other code or projects that you're proud of and would like to share with us.

Any feedback on the coding challenge once you're done is also appreciated!
