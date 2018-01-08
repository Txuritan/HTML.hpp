<h1 align="center">HTML.hpp</h1>

<div align="center">
    <strong>A HTML generator made in C++</strong>
</div>

<div align="center">
  <img src="https://img.shields.io/badge/made%20with-c%2B%2B11-blue.svg?style=flat-square" alt="Made With C++" />
  <a href="https://github.com/txuritan/HTML.hpp/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/txuritan/HTML.hpp.svg?style=flat-square" alt="License" />
  </a>
</div>

<div align="center">
  <a href="https://github.com/teammycelium/myriad/releases">
    <img src="https://img.shields.io/github/downloads/txuritan/HTML.hpp/total.svg?style=flat-square" alt="Downloads" />
  </a>
  <a>
    <img src="https://img.shields.io/github/release/txuritan/HTML.hpp/all.svg?style=flat-square" alt="Version" />
  </a>
</div>

<div align="center">
  <a href="https://txuritan.github.io/HTML.hpp/">
    Website
  </a>
  <span> | </span>
  <a href="https://txuritan.github.io/HTML.hpp/docs/">
    Documentation (TODO)
  </a>
</div>

## Table Of Contents

  * [Usage](#usage)
    * [Simple](#simple-replit)
    * [Simple Body](#simple-body-replit)
    * [Simple Body with HH_SHORTER](#simple-body-with-hh_shorter-replit)
  * [Contributors](#contributors)
  * [TODO](#todo)
  * [Changelog](#changelog)

## Usage

Include ```HTML.hpp``` in your project.

There are a few defines that configure how HTML.hpp works.
  * ```HH_INDENT```: How big the indent is when the html is generated. (Defaults to 4)
  * ```HH_STARTING_INDENT```: After how many tags should it start indenting. (Defaults to 2)
  * ```HH_NAMESPACE```: Enables HTML.hpp's namespace. (Defaults to undefined)
  * ```HH_SHORTER```: Enables some typedefs to make HTML.hpp short to write (Defaults to undefined)

### Simple ([repl.it](https://repl.it/@Txuritan/VigorousRequiredPrimate))

```c++
#include <iostream>

#include "HTML.hpp"

int main() {
    h example("div", "Hello from HTML.hpp");
    
    std::cout << example.toString() << std::endl;
    
    return 0;
}
```

```html
<div>
    Hello from HTML.hpp
</div>
```

### Simple Body ([repl.it](https://repl.it/@Txuritan/SpryBusyJavalina))

```c++
#include <iostream>

#include "HTML.hpp"

int main() {
    hb example(hDoctype::html5, std::vector<h> {
      h("title", "Hello from HTML.hpp")
    }, std::vector<h> {
      h("h1", "Hello!")
    });
    
    std::cout << example.toString() << std::endl;
    
    return 0;
}
```

```html
<!DOCTYPE html>
<html>
<head>
    <title>
        Hello from HTML.hpp
    </title>
</head>
<body>
    <h1>
        Hello!
    </h1>
</body>
</html>
```

### Simple Body with HH_SHORTER ([repl.it](https://repl.it/@Txuritan/BadTotalBirdofparadise))

```c++
#include <iostream>

#define HH_SHORTER

#include "HTML.hpp"

int main() {
    hb example(hD::html5, hV {
      h("title", "Hello from HTML.hpp")
    }, hV {
      h("h1", "Hello!")
    });
    
    std::cout << example.toString() << std::endl;
    
    return 0;
}
```

```html
<!DOCTYPE html>
<html>
<head>
    <title>
        Hello from HTML.hpp
    </title>
</head>
<body>
    <h1>
        Hello!
    </h1>
</body>
</html>
```

## Contributors

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/Txuritan">
        <img src="https://avatars0.githubusercontent.com/u/7692150" width="80px;"/>
        <br />
        Txuritan
      </a>
    </td>
    <td>
      <img src="https://img.shields.io/badge/contributor-code-blue.svg" alt="Contributor: Code" />
      <br />
      <img src="https://img.shields.io/badge/contributor-design-blue.svg" alt="Contributor: Design" />
      <br />
      <img src="https://img.shields.io/badge/contributor-documentation-blue.svg" alt="Contributor: Documentation" />
      <br />
      <img src="https://img.shields.io/badge/contributor-translation-blue.svg" alt="Contributor: Translation" />
    </td>
  </tr>
</table>

## TODO

  * Documentation
  * Constructors
    * All forms so others wont have to write as much code
    * Use this PHP script to sort the constructors [repl.it](https://repl.it/@Txuritan/TanDearHarborseal)
  * Partials
    * For frameworks like
      * Bootstrap
      * Foundation
  * OStream << operator
  * CSS and JS (?)
    * JQuery?
  * More short hand methods

## Changelog

  * v0.1.0
    * Initial release