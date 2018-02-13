# sort-by-chapter

Creates an array of elements, sorted in ascending order by the results of running each element in a collection thru each iteratee.

[![NPM](https://nodei.co/npm/sort-by-chapter.png?downloads=true&downloadRank=true&stars=true)][npm-url][![NPM](https://nodei.co/npm-dl/sort-by-chapter.png?height=3&months=6)][npm-url]

[![npm](https://img.shields.io/npm/v/sort-by-chapter.svg)][npm-url] [![npm](https://img.shields.io/npm/dm/sort-by-chapter.svg)][npm-url] [![npm](https://david-dm.org/Envisio/sort-by-chapter.svg)][npm-url] [![npm](https://img.shields.io/npm/l/sort-by-chapter.svg)][npm-url]

[![bitHound Overall Score](https://www.bithound.io/github/Envisio/sort-by-chapter/badges/score.svg)](https://www.bithound.io/github/Envisio/sort-by-chapter) [![Inline docs](http://inch-ci.org/github/Envisio/sort-by-chapter.svg?branch=master&style=shields)](http://inch-ci.org/github/Envisio/sort-by-chapter) [![Build Status](https://travis-ci.org/Envisio/sort-by-chapter.svg?branch=master)](https://travis-ci.org/Envisio/sort-by-chapter) [![Coverage Status](https://coveralls.io/repos/github/Envisio/sort-by-chapter/badge.svg?branch=master)](https://coveralls.io/github/Envisio/sort-by-chapter?branch=master)

[![GitHub stars](https://img.shields.io/github/stars/Envisio/sort-by-chapter.svg?style=social&label=Star)](https://github.com/Envisio/sort-by-chapter/stargazers) [![GitHub watchers](https://img.shields.io/github/watchers/Envisio/sort-by-chapter.svg?style=social&label=Watch)](https://github.com/Envisio/sort-by-chapter/subscription)

[npm-url]: https://npmjs.org/package/sort-by-chapter

## Installation

```bash
$ npm install sort-by-chapter
```

## Examples

### Basic

```js
import sortByChapter from 'sort-by-chapter';

const arr = [
  'Goal 1',
  'Goal 2',
  'Goal 3',
  'Strategy 1.1',
  'Strategy 1.2',
  'Strategy 1.3',
  'Activity 1.1.1',
  'Activity 1.1.2',
  'Activity 1.1.3'
];
const newArr = sortByChapter(arr);
console.log(newArr);
```
```json
[ 'Goal 1',
  'Strategy 1.1',
  'Activity 1.1.1',
  'Activity 1.1.2',
  'Activity 1.1.3',
  'Strategy 1.2',
  'Strategy 1.3',
  'Goal 2',
  'Goal 3' ]
```

### Specify Attribute

```js
import sortByChapter from 'sort-by-chapter';

const arr = [
  { title: 'Goal 1',
  { title: 'Goal 2' },
  { title: 'Goal 3' },
  { title: 'Strategy 1.1' },
  { title: 'Strategy 1.2' },
  { title: 'Strategy 1.3' },
  { title: 'Activity 1.1.1' },
  { title: 'Activity 1.1.2' },
  { title: 'Activity 1.1.3' }
];
const newArr = sortByChapter(arr, { attribute: 'title' });
console.log(newArr);
```
```json
[ { title: 'Goal 1' },
  { title: 'Strategy 1.1' },
  { title: 'Activity 1.1.1' },
  { title: 'Activity 1.1.2' },
  { title: 'Activity 1.1.3' },
  { title: 'Strategy 1.2' },
  { title: 'Strategy 1.3' },
  { title: 'Goal 2' },
  { title: 'Goal 3' } ]
```