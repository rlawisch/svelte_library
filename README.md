# Svelte Library

This project is made based on the awesome [Svelte: Getting Started](https://app.pluralsight.com/library/courses/svelte-getting-started/table-of-contents) Pluralsight course (by [Jake Trent](https://app.pluralsight.com/profile/author/jake-trent)).

It is intended to be an interactive library, where the user can add books and set them as favorites.


## Get started

Clone the repository...

```bash
git clone https://github.com/rlawisch/svelte_library.git
```

Install the dependencies...

```bash
cd svelte_library
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:5000](http://localhost:5000). You should see the library with a few sample books to start. If you edit a component file in `src`, save it and reload the page, your changes will be there.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in package.json to include the option `--host 0.0.0.0`.


## Building and running in production mode

To create an optimised version of the app:

```bash
npm run build
```

You can run the newly built app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv), which is included in your package.json's `dependencies` so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).


## Deploying to the web

### With [now](https://zeit.co/now)

Install `now` if you haven't already:

```bash
npm install -g now
```

Then, from within the project folder:

```bash
cd public
now deploy --name svelte_library
```

As an alternative, use the [Now desktop client](https://zeit.co/download) and simply drag the unzipped project folder to the taskbar icon.

### With [surge](https://surge.sh/)

Install `surge` if you haven't already:

```bash
npm install -g surge
```

Then, from within the project folder:

```bash
npm run build
surge public svelte_library.surge.sh
```
