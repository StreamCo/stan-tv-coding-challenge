# Stan TV NodeJS Coding Challenge

> Welcome to the Stan TV NodeJS Coding Challenge!

## Overview

The purpose of this challenge is to assess your knowledge around composing a **simple websocket based client/server application** closely following the guidelines and requirements.

## Guidelines

- The "Client" Application should be built using [Babel](https://www.babeljs.io) into a `dist/client` folder containing three files (`app.js`, `logo.svg` and `index.html`).
- The "Server" Application should be built using [Babel](https://www.babeljs.io) into a `dist/server` folder containing a single file (`server.js`).
- Your solution should be implemented using:
  - [TypeScript](https://www.typescriptlang.org)
  - [Babel](https://babeljs.io)
  - [Jest](https://jestjs.io)
- You should avoid using any other JS frameworks/libraries.
- We are looking for solutions that are **simple, modern, performant, and tested**.

## Requirements

You will need to build the following 2 applications:

### "Client" Application

[client-1.jpg](./client-1.jpg)
[client-2.jpg](./client-2.jpg)

- Render a black document with the stan logo `logo.svg` horizontally and vertically centered.
- Establish a connection to the "Server" Application.
- The "Client" App should be available from port 8080.
- Receive messages from the "Server" Application containing an id and url.
- Create a blob from this url and append this to the document.
- Skip any further actions when this blob has already been appended to the document.
- The `logo.svg` file should shrink to the top left corner when appending the first blob to the document.
- Create a sha256 hash from this blob and send a message back to the "Server" Application containing the id and the hash.
- Include a button to enable or disable hashing.
- When hashing is disabled `{ id, hash: null }` should be sent as a message to the "Server" Application.
- When a connection to the "Server" Application is lost `logo.svg` should be horizontally and vertically centered and any blobs should be removed
- This functionality should be unit tested.

### "Server" Application

[server-1.jpg](./server-1.jpg)
[server-2.jpg](./server-2.jpg)

- Create a basic cli to run the "Server" Application using `stan --interval=15 --file=data.json`.
- When this cli is ran the `data.json` file should be parsed and a websocket server instantiated.
- The "Server" Application should be available from port 8081.
- Every 15 seconds a message should be sent to the "Client" Application containing the next `{ id, image }`.
- When the end of the file has been reached the data should be reparsed.
- When the data has been reparsed a message should be sent to the "Client" Application containing the first `{ id, image }`.
- Messages should also be received from the "Client" Application containing `{ id, hash }`.
- As each message is received read the url into a buffer and create a blob before creating a new sha256 hash.
- Compare these two hashes and when these hashes match log `{ id, hash, image }` to the terminal as green text.
- When these hashes do not match log `{ id, hash, image }` to the terminal as red text.
- This functionality should be unit tested.

## Other Notes

Please also include a `README` with setup instructions, and any tests or other documentation you created as part of your solution.

Also, add the following info to your `README`:

- How did you decide on the technical and architectural choices used as part of your solution?
- Are there any improvements you could make to your submission?
- What would you do differently if you were allocated more time?

Please also send through any other code or projects that you're proud of and would like to share with us.

Any feedback on the coding challenge once you're done is also appreciated!

## Contact Us

If you have any questions feel free to email us:

[dev-team@stan.com.au](dev-team@stan.com.au)
