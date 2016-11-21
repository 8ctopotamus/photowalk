# Photowalk

Notes:
So the basis idea of the app is two connect local photographers on the one hand and on the other hand to create a map of interesting photo places.

So regarding the first part:
If somebody is going out to take pictures that person would be able to connect to others who are doing the same and partner up, because it is always more fun to do it in a group.

Regarding the second:
Imagine you are going to a new city and and to take photos but you don't really know where to go (except maybe the super touristic places). Or even in your own city there are many hidden places you have never heard of.
The idea it to categorize and cataloguize those places with additional information like ratings, comments and pictures.
(Ideally that would be done by the community.) So you would be able to comfortably search for them on your app.


That's the basic idea. I am currently still brainstorming for additional features. One would include (photo-)workshops using augmented reality. Which I think is really promising, as it would kinda create it's own demand.

I hope I was able to bring the point of the application across.
I also created a small mock-up of the possible features. It is very simple but maybe it helps understanding.

About the labels: my first idea was to categorize, as you probably want to meet people who do the same as you.

But thinking a little more about it. It might be good to leave this out, at least for the beginning. For simplicity reasons, and also maybe people enjoy trying out new things which aren't their field.

So showing those people who are currently walking around in your proximity and you are able to invite to take pictures together.
You should be able to invite them, and if they accept it will show you their location (using GPS), or you can schedule a meeting point.


## Polymer App Toolbox - Starter Kit

[![Build Status](https://travis-ci.org/PolymerElements/polymer-starter-kit.svg?branch=master)](https://travis-ci.org/PolymerElements/polymer-starter-kit)

This template is a starting point for building apps using a drawer-based
layout. The layout is provided by `app-layout` elements.

This template, along with the `polymer-cli` toolchain, also demonstrates use
of the "PRPL pattern" This pattern allows fast first delivery and interaction with
the content at the initial route requested by the user, along with fast subsequent
navigation by pre-caching the remaining components required by the app and
progressively loading them on-demand as the user navigates through the app.

The PRPL pattern, in a nutshell:

* **Push** components required for the initial route
* **Render** initial route ASAP
* **Pre-cache** components for remaining routes
* **Lazy-load** and progressively upgrade next routes on-demand

### Migrating from Polymer Starter Kit v1?

[Check out our blog post that covers what's changed in PSK2 and how to migrate!](https://www.polymer-project.org/1.0/blog/2016-08-18-polymer-starter-kit-or-polymer-cli.html)

### Setup

##### Prerequisites

Install [polymer-cli](https://github.com/Polymer/polymer-cli):

    npm install -g polymer-cli

##### Initialize project from template

    mkdir my-app
    cd my-app
    polymer init starter-kit

### Start the development server

This command serves the app at `http://localhost:8080` and provides basic URL
routing for the app:

    polymer serve --open


### Build

This command performs HTML, CSS, and JS minification on the application
dependencies, and generates a service-worker.js file with code to pre-cache the
dependencies based on the entrypoint and fragments specified in `polymer.json`.
The minified files are output to the `build/unbundled` folder, and are suitable
for serving from a HTTP/2+Push compatible server.

In addition the command also creates a fallback `build/bundled` folder,
generated using fragment bundling, suitable for serving from non
H2/push-compatible servers or to clients that do not support H2/Push.

    polymer build

### Preview the build

This command serves the minified version of the app at `http://localhost:8080`
in an unbundled state, as it would be served by a push-compatible server:

    polymer serve build/unbundled

This command serves the minified version of the app at `http://localhost:8080`
generated using fragment bundling:

    polymer serve build/bundled

### Run tests

This command will run
[Web Component Tester](https://github.com/Polymer/web-component-tester) against the
browsers currently installed on your machine.

    polymer test

### Adding a new view

You can extend the app by adding more views that will be demand-loaded
e.g. based on the route, or to progressively render non-critical sections
of the application.  Each new demand-loaded fragment should be added to the
list of `fragments` in the included `polymer.json` file.  This will ensure
those components and their dependencies are added to the list of pre-cached
components (and will have bundles created in the fallback `bundled` build).
