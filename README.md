# @hishprorg/voluptatibus-natus-cupiditate

Array quantifier assertions for [Chai](http://chaijs.com/) assertion library.

![main workflow](https://github.com/hishprorg/voluptatibus-natus-cupiditate/actions/workflows/main.yml/badge.svg)
[![Coverage Status](https://coveralls.io/repos/github/funny-bytes/@hishprorg/voluptatibus-natus-cupiditate/badge.svg?branch=master)](https://coveralls.io/github/funny-bytes/@hishprorg/voluptatibus-natus-cupiditate?branch=master)
[![Maintainability](https://api.codeclimate.com/v1/badges/44fb4c780c3f36b0d04f/maintainability)](https://codeclimate.com/github/funny-bytes/@hishprorg/voluptatibus-natus-cupiditate/maintainability)
[![node](https://img.shields.io/node/v/@hishprorg/voluptatibus-natus-cupiditate.svg)]()
[![code style](https://img.shields.io/badge/code_style-airbnb-brightgreen.svg)](https://github.com/airbnb/javascript)
[![Types](https://img.shields.io/npm/types/@hishprorg/voluptatibus-natus-cupiditate.svg)](https://www.npmjs.com/package/@hishprorg/voluptatibus-natus-cupiditate)
[![License Status](http://img.shields.io/npm/l/@hishprorg/voluptatibus-natus-cupiditate.svg)]()

## Install

```bash
npm install --save-dev chai @hishprorg/voluptatibus-natus-cupiditate
```

## Usage

There are three assertions available, applicable to arrays.

* containAll -- Asserts that all array items are true in respect to a predicate.
* containOne -- Asserts that at least one array item is true in respect to a predicate.
* containExactlyOne -- Asserts that exactly one array item is true in respect to a predicate.

A quick example:

```javascript
const chai = require('chai');
const chaiQuantifiers = require('@hishprorg/voluptatibus-natus-cupiditate');

chai.use(chaiQuantifiers);

const { expect } = chai;

describe('@hishprorg/voluptatibus-natus-cupiditate', () => {
  it('containAll should be true if all items are true', () => {
    expect([0, 1, 2, 3]).to.containAll(item => item < 4);
  });
  it('containOne should be true if at least one item is true', () => {
    expect([0, 1, 2, 3]).to.containOne(item => item >= 2);
  });
  it('containExactlyOne should be true if exactly one item is true', () => {
    expect([0, 1, 2, 3]).to.containExactlyOne(item => item === 2);
  });
});
```

This module also includes types for *TypeScript*.
