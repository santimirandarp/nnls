# nnls

[![NPM version][npm-image]][npm-url]
[![build status][ci-image]][ci-url]
[![Test coverage][codecov-image]][codecov-url]
[![npm download][download-image]][download-url]

Non-Negative Least-Squares (NNLS) algorithm, by Lawson and Hanson. It was mostly done for learning purposes, and will be improved over time.

Currently, it seems to match (scipy's results)[https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.nnls.html].

You are welcome to report issues and contribute to this project.

## Installation

`$ npm i nnls`

## Usage

```js
import { nnls } from 'nnls';

const { resultVector } = nnls(X, y);
```

The code returns also the `dualVector` and the `MSE`.

You can pass `{ interceptAtZero:false }` if you want $f(0)=C$.

Like other implementations (for example `scipy.optimize.nnls`) it is limited to a single vector $y$, or as it is called in the literature, a single right-hand-side (RHS).

For multiple RHS, you can take a look at [Fast-Combinatorial Non-Negative Least-Squares](https://github.com/mljs/fcnnls)

## License

[MIT](./LICENSE)

[npm-image]: https://img.shields.io/npm/v/nnls.svg
[npm-url]: https://www.npmjs.com/package/nnls
[ci-image]: https://github.com/santimirandarp/nnls/workflows/Node.js%20CI/badge.svg?branch=main
[ci-url]: https://github.com/santimirandarp/nnls/actions?query=workflow%3A%22Node.js+CI%22
[codecov-image]: https://img.shields.io/codecov/c/github/santimirandarp/nnls.svg
[codecov-url]: https://codecov.io/gh/santimirandarp/nnls
[download-image]: https://img.shields.io/npm/dm/nnls.svg
[download-url]: https://www.npmjs.com/package/nnls
