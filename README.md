# fullcalendar-yarn

testing publishing a fork of fullcalendar using yarn publish

try:

1) DIDN'T WORK: 'standard-scripts' is not recognized as an internal or external command

```sh
yarn publish
```

then

```sh
npm i -E fullcalendar-yarn
```

2) THIS DIDN'T WORK EITHER:

```sh
# (requires installing pnpm first)
pnpm install
pnpm run build
yarn publish
```

then

```sh
npm i -E fullcalendar-yarn
```

## FullCalendar

Full-sized drag & drop calendar in JavaScript

- [Project Website](https://fullcalendar.io/)
- [Documentation](https://fullcalendar.io/docs)
- [Changelog](CHANGELOG.md)
- [Support](https://fullcalendar.io/support)
- [License](LICENSE.md)
- [Roadmap](https://fullcalendar.io/roadmap)

Connectors:

- [React](https://github.com/fullcalendar/fullcalendar-react)
- [Angular](https://github.com/fullcalendar/fullcalendar-angular)
- [Vue 3](https://github.com/fullcalendar/fullcalendar-vue) |
  [2](https://github.com/fullcalendar/fullcalendar-vue2)

## Bundle

The [FullCalendar Standard Bundle](bundle) is easier to install than individual plugins, though filesize will be larger. It works well with a CDN.

## Installation

Install the FullCalendar core package and any plugins you plan to use:

```sh
npm install @fullcalendar/core @fullcalendar/interaction @fullcalendar/daygrid
```

## Usage

Instantiate a Calendar with plugins and options:

```js
import { Calendar } from '@fullcalendar/core'
import interactionPlugin from '@fullcalendar/interaction'
import dayGridPlugin from '@fullcalendar/daygrid'

const calendarEl = document.getElementById('calendar')
const calendar = new Calendar(calendarEl, {
  plugins: [
    interactionPlugin,
    dayGridPlugin
  ],
  initialView: 'timeGridWeek',
  editable: true,
  events: [
    { title: 'Meeting', start: new Date() }
  ]
})

calendar.render()
```

## Development

You must install this repo with [PNPM](https://pnpm.io/):

```
pnpm install
```

Available scripts (via `pnpm run <script>`):

- `build` - build production-ready dist files
- `dev` - build & watch development dist files
- `test` - test headlessly
- `test:dev` - test interactively
- `lint`
- `clean`

[Info about contributing code &raquo;](CONTRIBUTING.md)
