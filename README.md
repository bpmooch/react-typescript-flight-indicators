# react-typescript-flight-indicators

> A React + Typescript porting of react-flight-indicators (https://github.com/skyhop/react-flight-indicators)

[![NPM](https://img.shields.io/npm/v/react-typescript-flight-indicators.svg)](https://www.npmjs.com/package/react-typescript-flight-indicators) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)


The `react-typescript-flight-indicators` package allows you to display high quality flight indicators using html, css3, React, TypeScript and SVG images.
The methods make customization and real-time implementation really easy.
Further, since all the images are vector svg, you can resize the indicators to your application without any quality loss!

Currently supported indicators are :

* Attitude (artificial horizon)
* Heading 
* Vertical speed
* Air speed
* Altimeter
* variometer

`react-typescript-flight-indicators` is a porting from [skyhop/react-flight-indicators](https://github.com/skyhop/react-flight-indicators), and refactored for use with React and TypeScript.

## Install

Using YARN;

```bash
yarn add react-typescript-flight-indicators
```

Alternatively with NPM;

```bash
npm install --save react-typescript-flight-indicators
```

## Usage

```tsx
import React, { Component } from 'react'

import {
  Airspeed,
  Altimeter,
  AttitudeIndicator,
  HeadingIndicator,
  TurnCoordinator,
  Variometer
} from 'react-typescript-flight-indicators'

const Example = () => {
  	return (
	  	<>
			<HeadingIndicator heading={Math.random() * 360} showBox={false} />

			<hr />

			<Airspeed speed={Math.random() * 160} showBox={false} />

			<hr />

			<Altimeter altitude={Math.random() * 28000} showBox={false} />

			<hr />

			<AttitudeIndicator roll={(Math.random() - 0.5) * 120} pitch={(Math.random() - 0.5) * 40} showBox={false} />

			<hr />

			<TurnCoordinator turn={(Math.random() - 0.5) * 120} showBox={false} />

			<hr />

			<Variometer vario={(Math.random() - 0.5) * 4000} showBox={false} />
	  	</>
  	)
}
```

## License

GPL-3.0 © [Starnuto di topo](https://github.com/starnutoditopo)

Example & Demo
-------------------

The JQuery demo can be found here : [http://sebmatton.github.io/flightindicators/](http://sebmatton.github.io/flightindicators/)

Here are a few examples of currently implemented indicators :

![demo_example](https://raw.githubusercontent.com/sebmatton/jQuery-Flight-Indicators/master/_examples_data/example.png "Indicator examples")

The image below shows a part of an 800px indicator. Vector images allows you to keep high quality render with large indicators.

![demo_highres](https://raw.githubusercontent.com/sebmatton/jQuery-Flight-Indicators/master/_examples_data/example_highres.png "High resolution indicator")


Authors and License
-----------

Originally this project has been based on work by igneosaur, which could be found [on Bitbucket](https://bitbucket.org/igneosaur/attitude-indicator).

Further work is done by Sébastien Matton (seb_matton@hotmail.com), whom developed the jQuery plugin as part of his master's for showing realtime flight information from a quadcopter.

[Corstian Boerman](https://corstianboerman.com) has adapted the project by Sébastien for use with React.

The project is published under GPLv3 License. See LICENSE file for more informations

# Development log

## Create typescript react project 

Initial project created with the following command:

    docker run -it --rm -v ${PWD}:/app -p 3000:3000 --entrypoint /bin/sh node:16.0.0-alpine3.13 -c "cd /app && npx create-react-library"

### references

- https://www.npmjs.com/package/create-react-library