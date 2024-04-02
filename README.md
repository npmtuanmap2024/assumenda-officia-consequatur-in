An [iterable] is a sequence of values.<br>
📦 [Node.js](https://www.npmjs.com/package/@npmtuanmap2024/assumenda-officia-consequatur-in),
🌐 [Web](https://www.npmjs.com/package/@npmtuanmap2024/assumenda-officia-consequatur-in.web),
📜 [Files](https://unpkg.com/@npmtuanmap2024/assumenda-officia-consequatur-in/),
📰 [Docs](https://nodef.github.io/@npmtuanmap2024/assumenda-officia-consequatur-in/),
📘 [Wiki](https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/).

This is a collection of functions for operating upon **iterables**. Assumption
here is that an **iterable** can *only* be iterated over *once*. Methods which
require multiple iterations preserve old values in a backup array using
[toMany]. Many methods accept both compare and map functions, and in some cases
using **only** a map function enables *faster comparision* (like [unique]). I
borrowed a lot of ideas from Haskell, Elm, Python, Basic, Lodash, and other NPM
packages. These are mentioned in references of each method.

This package is available in *Node.js* and *Web* formats. To use it on the web,
simply use the `extra_iterable` global variable after loading with a `<script>`
tag from the [jsDelivr CDN].

> Stability: [Experimental](https://www.youtube.com/watch?v=L1j93RnIxEo).

[iterable]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Iteration_protocols
[jsDelivr CDN]: https://cdn.jsdelivr.net/npm/@npmtuanmap2024/assumenda-officia-consequatur-in.web/index.js

<br>

```javascript
const xiterable = require('@npmtuanmap2024/assumenda-officia-consequatur-in');
// import * as xiterable from "@npmtuanmap2024/assumenda-officia-consequatur-in";
// import * as xiterable from "https://unpkg.com/@npmtuanmap2024/assumenda-officia-consequatur-in/index.mjs"; (deno)

var x = [2, 4, 6, 8];
xiterable.get(x, 1);
// → 4

var x = [1, 2, 3, 4];
[...xiterable.swap(x, 0, 1)];
// → [ 2, 1, 3, 4 ]

var x = [1, 2, 3];
[...xiterable.cycle(x, 0, 4)];
// → [1, 2, 3, 1]

var x = [1, 2, 3, 4];
xiterable.reduce(x, (acc, v) => acc+v);
// → 10
```

<br>
<br>


## Index

| Property | Description |
|  ----  |  ----  |
| [is] | Check if value is an iterable. |
| [isIterator] | Check if value is an iterator. |
| [isList] | Check if value is a list (iterable & !string). |
| [iterator] | Get iterator of an iterable. |
| [keys] | List all indices. |
| [values] | List all values. |
| [entries] | List all index-value pairs. |
|  |  |
| [from] | Convert an iterable-like to iterable. |
| [fromIterator] | Convert an iterator to iterable. |
| [fromRange] | Generate iterable from given number range. |
| [fromInvocation] | Generate iterable from repeated function invocation. |
| [fromApplication] | Generate iterable from repeated function application. |
|  |  |
| [isOnce] | Check if an iterable can iterated only once. |
| [isMany] | Check if an iterable can be iterated many times. |
| [toMany] | Convert a once-like iterable to many. |
| [toInvokable] | Generate a function that iterates over values upon invocation. |
|  |  |
| [isEmpty] | Check if an iterable is empty. |
| [length] | Find the length of an iterable. |
|  |  |
| [compare] | Compare two iterables. |
| [isEqual] | Check if two iterables are equal. |
|  |  |
| [index] | Get zero-based index for element in iterable. |
| [indexRange] | Get index range for part of iterable. |
| [get] | Get value at index. |
| [getAll] | Get values at indices. |
| [getPath] | Get value at path in a nested iterable. |
| [hasPath] | Check if nested iterable has a path. |
| [set] | Set value at index. |
| [swap] | Exchange two values. |
| [remove] | Remove value at index. |
|  |  |
| [count] | Count values which satisfy a test. |
| [countAs] | Count occurrences of values. |
| [min] | Find smallest value. |
| [max] | Find largest value. |
| [range] | Find smallest and largest values. |
| [minEntry] | Find smallest entry. |
| [maxEntry] | Find largest entry. |
| [rangeEntries] | Find smallest and largest entries. |
|  |  |
| [slice] | Get part of an iterable. |
| [head] | Get first value. |
| [last] | Get last value. |
| [tail] | Get values except first. |
| [init] | Get values except last. |
| [left] | Get values from left. |
| [right] | Get values from right. |
| [middle] | Get values from middle. |
| [take] | Keep first n values only. |
| [takeRight] | Keep last n values only. |
| [takeWhile] | Keep values from left, while a test passes. |
| [takeWhileRight] | Keep values from right, while a test passes. |
| [drop] | Discard first n values only. |
| [dropRight] | Discard last n values only. |
| [dropWhile] | Discard values from left, while a test passes. |
| [dropWhileRight] | Discard values from right, while a test passes. |
|  |  |
| [includes] | Check if iterable has a value. |
| [indexOf] | Find first index of a value. |
| [lastIndexOf] | Find last index of a value. |
| [find] | Find first value passing a test. |
| [findRight] | Find last value passing a test. |
| [scanWhile] | Scan from left, while a test passes. |
| [scanWhileRight] | Scan from right, while a test passes. |
| [scanUntil] | Scan from left, until a test passes. |
| [scanUntilRight] | Scan from right, until a test passes. |
| [search] | Find index of first value passing a test. |
| [searchRight] | Find index of last value passing a test. |
| [searchAll] | Find indices of values passing a test. |
| [searchValue] | Find first index of a value. |
| [searchValueRight] | Find last index of a value. |
| [searchValueAll] | Find indices of a value. |
| [searchInfix] | Find first index of an infix. |
| [searchInfixRight] | Find last index of an infix. |
| [searchInfixAll] | Find indices of an infix. |
| [searchSubsequence] | Find first index of a subsequence. |
| [hasValue] | Check if iterable has a value. |
| [hasPrefix] | Check if iterable starts with a prefix. |
| [hasSuffix] | Check if iterable ends with a suffix. |
| [hasInfix] | Check if iterable contains an infix. |
| [hasSubsequence] | Check if iterable has a subsequence. |
|  |  |
| [forEach] | Call a function for each value. |
| [some] | Check if any value satisfies a test. |
| [every] | Check if all values satisfy a test. |
| [map] | Transform values of an iterable. |
| [reduce] | Reduce values of iterable to a single value. |
| [filter] | Keep the values which pass a test. |
| [filterAt] | Keep the values at given indices. |
| [reject] | Discard the values which pass a test. |
| [rejectAt] | Discard the values at given indices. |
| [accumulate] | Produce accumulating values. |
| [flat] | Flatten nested iterable to given depth. |
| [flatMap] | Flatten nested iterable, based on map function. |
| [zip] | Combine values from iterables. |
|  |  |
| [fill] | Fill with given value. |
| [push] | Add values to the end. |
| [unshift] | Add values to the start. |
| [copy] | Copy part of iterable to another. |
| [copyWithin] | Copy part of iterable within. |
| [moveWithin] | Move part of iterable within. |
| [splice] | Remove or replaces existing values. |
| [split] | Break iterable considering test as separator. |
| [splitAt] | Break iterable considering indices as separator. |
| [cut] | Break iterable when test passes. |
| [cutRight] | Break iterable after test passes. |
| [cutAt] | Break iterable at given indices. |
| [cutAtRight] | Break iterable after given indices. |
| [group] | Keep similar values together and in order. |
| [partition] | Segregate values by test result. |
| [partitionAs] | Segregate values by similarity. |
| [chunk] | Break iterable into chunks of given size. |
| [cycle] | Obtain values that cycle through an iterable. |
| [repeat] | Repeat an iterable given times. |
| [reverse] | Reverse the values. |
| [rotate] | Rotate values in iterable. |
| [intersperse] | Place a separator between every value. |
| [interpolate] | Estimate new values between existing ones. |
| [intermix] | Place values of an iterable between another. |
| [interleave] | Place values from iterables alternately. |
|  |  |
| [concat] | Append values from iterables. |
| [merge] | Merge values from sorted iterables. |
| [join] | Join values together into a string. |
|  |  |
| [isUnique] | Check if there are no duplicate values. |
| [isDisjoint] | Checks if arrays have no value in common. |
| [unique] | Remove duplicate values. |
| [union] | Obtain values present in any iterable. |
| [intersection] | Obtain values present in both iterables. |
| [difference] | Obtain values not present in another iterable. |
| [symmetricDifference] | Obtain values not present in both iterables. |
| [cartesianProduct] | List cartesian product of iterables. |

<br>
<br>


[![](https://img.youtube.com/vi/qgxPbqDskyw/maxresdefault.jpg)](https://www.youtube.com/watch?v=qgxPbqDskyw)<br>
[![ORG](https://img.shields.io/badge/org-nodef-green?logo=Org)](https://nodef.github.io)
[![DOI](https://zenodo.org/badge/133694055.svg)](https://zenodo.org/badge/latestdoi/133694055)
[![Coverage Status](https://coveralls.io/repos/github/nodef/@npmtuanmap2024/assumenda-officia-consequatur-in/badge.svg?branch=master)](https://coveralls.io/github/nodef/@npmtuanmap2024/assumenda-officia-consequatur-in?branch=master)
[![Test Coverage](https://api.codeclimate.com/v1/badges/1ba4b1b22418456df9f9/test_coverage)](https://codeclimate.com/github/nodef/@npmtuanmap2024/assumenda-officia-consequatur-in/test_coverage)
[![Maintainability](https://api.codeclimate.com/v1/badges/1ba4b1b22418456df9f9/maintainability)](https://codeclimate.com/github/nodef/@npmtuanmap2024/assumenda-officia-consequatur-in/maintainability)


[is]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/is
[isIterator]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/isIterator
[isList]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/isList
[iterator]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/iterator
[keys]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/keys
[values]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/values
[entries]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/entries
[from]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/from
[fromIterator]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/fromIterator
[fromRange]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/fromRange
[fromInvocation]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/fromInvocation
[fromApplication]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/fromApplication
[isOnce]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/isOnce
[isMany]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/isMany
[toMany]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/toMany
[toInvokable]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/toInvokable
[isEmpty]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/isEmpty
[length]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/length
[compare]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/compare
[isEqual]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/isEqual
[index]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/index
[indexRange]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/indexRange
[get]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/get
[getAll]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/getAll
[getPath]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/getPath
[hasPath]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/hasPath
[set]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/set
[swap]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/swap
[remove]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/remove
[count]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/count
[countAs]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/countAs
[min]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/min
[max]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/max
[range]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/range
[minEntry]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/minEntry
[maxEntry]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/maxEntry
[rangeEntries]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/rangeEntries
[slice]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/slice
[head]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/head
[last]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/last
[tail]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/tail
[init]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/init
[left]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/left
[right]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/right
[middle]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/middle
[take]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/take
[takeRight]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/takeRight
[takeWhile]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/takeWhile
[takeWhileRight]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/takeWhileRight
[drop]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/drop
[dropRight]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/dropRight
[dropWhile]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/dropWhile
[dropWhileRight]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/dropWhileRight
[includes]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/includes
[indexOf]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/indexOf
[lastIndexOf]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/lastIndexOf
[find]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/find
[findRight]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/findRight
[scanWhile]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/scanWhile
[scanWhileRight]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/scanWhileRight
[scanUntil]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/scanUntil
[scanUntilRight]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/scanUntilRight
[search]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/search
[searchRight]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/searchRight
[searchAll]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/searchAll
[searchValue]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/searchValue
[searchValueRight]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/searchValueRight
[searchValueAll]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/searchValueAll
[searchInfix]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/searchInfix
[searchInfixRight]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/searchInfixRight
[searchInfixAll]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/searchInfixAll
[searchSubsequence]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/searchSubsequence
[hasValue]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/hasValue
[hasPrefix]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/hasPrefix
[hasSuffix]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/hasSuffix
[hasInfix]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/hasInfix
[hasSubsequence]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/hasSubsequence
[forEach]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/forEach
[some]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/some
[every]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/every
[map]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/map
[reduce]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/reduce
[filter]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/filter
[filterAt]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/filterAt
[reject]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/reject
[rejectAt]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/rejectAt
[accumulate]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/accumulate
[flat]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/flat
[flatMap]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/flatMap
[zip]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/zip
[fill]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/fill
[push]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/push
[unshift]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/unshift
[copy]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/copy
[copyWithin]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/copyWithin
[moveWithin]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/moveWithin
[splice]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/splice
[split]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/split
[splitAt]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/splitAt
[cut]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/cut
[cutRight]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/cutRight
[cutAt]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/cutAt
[cutAtRight]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/cutAtRight
[group]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/group
[partition]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/partition
[partitionAs]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/partitionAs
[chunk]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/chunk
[cycle]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/cycle
[repeat]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/repeat
[reverse]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/reverse
[rotate]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/rotate
[intersperse]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/intersperse
[interpolate]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/interpolate
[intermix]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/intermix
[interleave]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/interleave
[concat]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/concat
[merge]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/merge
[join]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/join
[isUnique]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/isUnique
[isDisjoint]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/isDisjoint
[unique]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/unique
[union]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/union
[intersection]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/intersection
[difference]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/difference
[symmetricDifference]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/symmetricDifference
[cartesianProduct]: https://github.com/npmtuanmap2024/assumenda-officia-consequatur-in/wiki/cartesianProduct
