<!--

@license Apache-2.0

Copyright (c) 2023 The Stdlib Authors.

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

# unarynd

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Apply a unary callback to elements in an n-dimensional nested input array and assign results to elements in an n-dimensional nested output array.

<section class="intro">

</section>

<!-- /.intro -->



<section class="usage">

## Usage

```javascript
import unarynd from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-base-unarynd@esm/index.mjs';
```

#### unarynd( arrays, shape, fcn )

Applies a unary callback to elements in an n-dimensional nested input array and assigns results to elements in an n-dimensional nested output array.

```javascript
import abs from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-abs@esm/index.mjs';

var x = [ [ -1.0, -2.0 ], [ -3.0, -4.0 ] ];
var shape = [ 2, 2 ];

// Compute the absolute values in-place:
unarynd( [ x, x ], shape, abs );
// x => [ [ 1.0, 2.0 ], [ 3.0, 4.0 ] ]
```

The function accepts the following arguments:

-   **arrays**: array-like object containing one input nested array and one output nested array.
-   **shape**: array shape.
-   **fcn**: unary function to apply.

</section>

<!-- /.usage -->

<section class="notes">

## Notes

-   The function assumes that the input and output arrays have the same shape.

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

var discreteUniform = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/random-base-discrete-uniform' ).factory;
import filledndBy from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-base-fillednd-by@esm/index.mjs';
import zerosnd from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-base-zerosnd@esm/index.mjs';
import abs from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-abs@esm/index.mjs';
import unarynd from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-base-unarynd@esm/index.mjs';

var shape = [ 3, 3 ];

var x = filledndBy( shape, discreteUniform( -100, 100 ) );
console.log( x );

var y = zerosnd( shape );
console.log( y );

unarynd( [ x, y ], shape, abs );
console.log( y );

shape = [ 3, 3, 3 ];

x = filledndBy( shape, discreteUniform( -100, 100 ) );
console.log( x );

y = zerosnd( shape );
console.log( y );

unarynd( [ x, y ], shape, abs );
console.log( y );

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

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

[npm-image]: http://img.shields.io/npm/v/@stdlib/array-base-unarynd.svg
[npm-url]: https://npmjs.org/package/@stdlib/array-base-unarynd

[test-image]: https://github.com/stdlib-js/array-base-unarynd/actions/workflows/test.yml/badge.svg?branch=v0.2.1
[test-url]: https://github.com/stdlib-js/array-base-unarynd/actions/workflows/test.yml?query=branch:v0.2.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/array-base-unarynd/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/array-base-unarynd?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/array-base-unarynd.svg
[dependencies-url]: https://david-dm.org/stdlib-js/array-base-unarynd/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/array-base-unarynd/tree/deno
[deno-readme]: https://github.com/stdlib-js/array-base-unarynd/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/array-base-unarynd/tree/umd
[umd-readme]: https://github.com/stdlib-js/array-base-unarynd/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/array-base-unarynd/tree/esm
[esm-readme]: https://github.com/stdlib-js/array-base-unarynd/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/array-base-unarynd/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/array-base-unarynd/main/LICENSE

</section>

<!-- /.links -->
