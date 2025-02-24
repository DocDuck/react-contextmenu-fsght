[![NPM version][npm-image]][npm-url]
[![Build Status][travis-image]][travis-url]
[![Dependency Status][deps-image]][deps-url]
[![Dev Dependency Status][dev-deps-image]][dev-deps-url]
[![Code Climate][climate-image]][climate-url]

[![NPM](https://nodei.co/npm/react-contextmenu.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/react-contextmenu/)

# React Contextmenu with SubMenu className

## Table of contents

 - [Installation](#installation)
 - [Browser Support](#browser-support)
 - [Usage](#usage)
 - [API](#api)
 - [FAQs](#faqs)
 - [Contributors](#contributors)
 - [Changelog](#changelog)
 - [License](#license)

## Installation

Using npm

```
npm install --save react-contextmenu-fsght
```

Using yarn

```
yarn add react-contextmenu-fsght
```

## Browser Support
- IE 11 and Edge >= 12
- FireFox >= 38
- Chrome >= 47
- Opera >= 34
- Safari >= 8

## Usage

Simple example

```jsx
import React from "react";
import ReactDOM from "react-dom";
import { ContextMenu, MenuItem, ContextMenuTrigger } from "react-contextmenu-fsght";

function handleClick(e, data) {
  console.log(data.foo);
}

function MyApp() {
  return (
    <div>
      {/* NOTICE: id must be unique between EVERY <ContextMenuTrigger> and <ContextMenu> pair */}
      {/* NOTICE: inside the pair, <ContextMenuTrigger> and <ContextMenu> must have the same id */}

      <ContextMenuTrigger id="same_unique_identifier">
        <div className="well">Right click to see the menu</div>
      </ContextMenuTrigger>

      <ContextMenu id="same_unique_identifier">
        <MenuItem data={{foo: 'bar'}} onClick={this.handleClick}>
          ContextMenu Item 1
        </MenuItem>
        <MenuItem data={{foo: 'bar'}} onClick={this.handleClick}>
          ContextMenu Item 2
        </MenuItem>
        <MenuItem divider />
        <MenuItem data={{foo: 'bar'}} onClick={this.handleClick}>
          ContextMenu Item 3
        </MenuItem>
      </ContextMenu>

    </div>
  );
}

ReactDOM.render(<MyApp myProp={12}/>, document.getElementById("main"));
```

see [usage docs](./docs/usage.md) / [examples](./examples) for more details.

## API

[API docs](./docs/api.md)

## FAQs

[ALL FAQs](./docs/faq.md)

## Who's using react-contextmenu?
- [react-data-grid](https://github.com/adazzle/react-data-grid)
- [teamup.com](https://teamup.com)
- [Spotify Web Player](https://open.spotify.com)

## Contributors

[All Contributors](https://github.com/docduck/react-contextmenu-fsght/graphs/contributors)

## Changelog

For Changelog, see [releases](https://github.com/docduck/react-contextmenu-fsght/releases)

## License

[MIT](./LICENSE.md). Copyright(c) [Vivek Kumar Bansal](http://vkbansal.me/)

[npm-url]: https://npmjs.org/package/react-contextmenu
[npm-image]: http://img.shields.io/npm/v/react-contextmenu.svg?style=flat-square

[travis-url]: https://travis-ci.org/vkbansal/react-contextmenu
[travis-image]: http://img.shields.io/travis/vkbansal/react-contextmenu/master.svg?style=flat-square

[deps-url]: https://david-dm.org/vkbansal/react-contextmenu
[deps-image]: https://img.shields.io/david/vkbansal/react-contextmenu.svg?style=flat-square

[dev-deps-url]: https://david-dm.org/vkbansal/react-contextmenu
[dev-deps-image]: https://img.shields.io/david/dev/vkbansal/react-contextmenu.svg?style=flat-square

[climate-url]: https://codeclimate.com/github/vkbansal/react-contextmenu
[climate-image]: http://img.shields.io/codeclimate/github/vkbansal/react-contextmenu.svg?style=flat-square
