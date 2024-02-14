<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# reDirnameWindows

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Regular expression][regexp] to capture a Windows path [dirname][dirname].



<section class="usage">

## Usage

```javascript
import reDirnameWindows from 'https://cdn.jsdelivr.net/gh/stdlib-js/regexp-dirname-windows@deno/mod.js';
```
The previous example will load the latest bundled code from the deno branch. Alternatively, you may load a specific version by loading the file from one of the [tagged bundles](https://github.com/stdlib-js/regexp-dirname-windows/tags). For example,

```javascript
import reDirnameWindows from 'https://cdn.jsdelivr.net/gh/stdlib-js/regexp-dirname-windows@v0.2.0-deno/mod.js';
```

You can also import the following named exports from the package:

```javascript
import { REGEXP } from 'https://cdn.jsdelivr.net/gh/stdlib-js/regexp-dirname-windows@deno/mod.js';
```

#### reDirnameWindows()

Returns a [regular expression][regexp] to capture a Windows path [dirname][dirname]. 

```javascript
var RE_DIRNAME_WINDOWS = reDirnameWindows();
var dir = RE_DIRNAME_WINDOWS.exec( 'foo\\bar\\index.js' )[ 1 ];
// returns 'foo\bar'
```

#### reDirnameWindows.REGEXP

[Regular expression][regexp] to capture a Windows path [dirname][dirname]. 

```javascript
var dir = reDirnameWindows.REGEXP.exec( 'foo\\bar\\index.js' )[ 1 ];
// returns 'foo\bar'
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
import reDirnameWindows from 'https://cdn.jsdelivr.net/gh/stdlib-js/regexp-dirname-windows@deno/mod.js';

var RE_DIRNAME_WINDOWS = reDirnameWindows();

var dir = RE_DIRNAME_WINDOWS.exec( 'index.js' )[ 1 ];
// returns ''

dir = RE_DIRNAME_WINDOWS.exec( 'C:\\foo\\bar\\home.html' )[ 1 ];
// returns 'C:\foo\bar'

dir = RE_DIRNAME_WINDOWS.exec( 'foo\\file.pdf' )[ 1 ];
// returns 'foo'

dir = RE_DIRNAME_WINDOWS.exec( 'beep\\boop.' )[ 1 ];
// returns 'beep'

dir = RE_DIRNAME_WINDOWS.exec( '' )[ 1 ];
// returns ''

dir = RE_DIRNAME_WINDOWS.exec( '\\foo\\bar\\file' )[ 1 ];
// returns '\foo\bar'

dir = RE_DIRNAME_WINDOWS.exec( 'C:\\foo\\bar\\.gitignore' )[ 1 ];
// returns 'C:\foo\bar'
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/regexp-dirname`][@stdlib/regexp/dirname]</span><span class="delimiter">: </span><span class="description">return a regular expression to capture a path dirname.</span>
-   <span class="package-name">[`@stdlib/regexp-dirname-posix`][@stdlib/regexp/dirname-posix]</span><span class="delimiter">: </span><span class="description">return a regular expression to capture a POSIX path dirname.</span>
-   <span class="package-name">[`@stdlib/utils-dirname`][@stdlib/utils/dirname]</span><span class="delimiter">: </span><span class="description">return a directory name.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/regexp-dirname-windows.svg
[npm-url]: https://npmjs.org/package/@stdlib/regexp-dirname-windows

[test-image]: https://github.com/stdlib-js/regexp-dirname-windows/actions/workflows/test.yml/badge.svg?branch=v0.2.0
[test-url]: https://github.com/stdlib-js/regexp-dirname-windows/actions/workflows/test.yml?query=branch:v0.2.0

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/regexp-dirname-windows/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/regexp-dirname-windows?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/regexp-dirname-windows.svg
[dependencies-url]: https://david-dm.org/stdlib-js/regexp-dirname-windows/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/regexp-dirname-windows/tree/deno
[deno-readme]: https://github.com/stdlib-js/regexp-dirname-windows/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/regexp-dirname-windows/tree/umd
[umd-readme]: https://github.com/stdlib-js/regexp-dirname-windows/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/regexp-dirname-windows/tree/esm
[esm-readme]: https://github.com/stdlib-js/regexp-dirname-windows/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/regexp-dirname-windows/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/regexp-dirname-windows/main/LICENSE

[regexp]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

[dirname]: https://en.wikipedia.org/wiki/Dirname

<!-- <related-links> -->

[@stdlib/regexp/dirname]: https://github.com/stdlib-js/regexp-dirname/tree/deno

[@stdlib/regexp/dirname-posix]: https://github.com/stdlib-js/regexp-dirname-posix/tree/deno

[@stdlib/utils/dirname]: https://github.com/stdlib-js/utils-dirname/tree/deno

<!-- </related-links> -->

</section>

<!-- /.links -->
