# <a href='http://fdc3.finos.org'><img src='https://fdc3.finos.org/img/fdc3-logo-2019-color.png' height='150' alt='FDC3 Logo' aria-label='fdc3.finos.org' /></a>

# FDC3 Conformance
This project represents a means to confirm conformance of a [desktop agent](https://fdc3.finos.org/docs/api/ref/DesktopAgent) to the [fdc3 api specification](https://fdc3.finos.org/docs/api/spec).

To do so this application can be launched within the desktop agent which will run a series of tests to verify conformance against the specification.

## Getting Started

1. Clone the repository

`git clone https://github.com/finos/FDC3`

2. Install dependencies and build

~~~
cd FDC3/toolbox/fdc3-compliance
yarn install
yarn build
~~~

3. Start the development server

`yarn start`

4. Add the URL http://localhost:3000 to your FDC3-enabled container or desktop agent and ensure it has access to the `window.fdc3` object.

Alternatively, a full set of static files are available in the `build` folder. Load the index.html file into an environment that has the `window.fdc3` object available.

## Application Definition

A basic FDC3 application definition, as defined in the [application directory specification](https://fdc3.finos.org/schemas/1.2/app-directory#tag/Application), is supplied in the [file](./src/appDefinition.json) `appDefinition.json`. This may be useful when adding the conformance tests to an application directory. This file may need to be updated with additional manifest information, depending on the desktop agent. Consult the host environment documentation for information on configuring new applications.