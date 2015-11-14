### eliminate javascript code smells - elijah manor

Christian , Family , PluralSight / LeanKit

Linting

Descarte - I lint, therefore I am.

### agenda

easy to lint, fresh rules
easy to lint, no rules

how to write new rules for linters

hard to lint, subjective rules

convoluted code smells

#### pig latin example

 - too many statements
 - too much depth
 - too complexity (cyclomatic complexity)

jshint / eslint have cyclomatic 

#### linting rules 

 - max-depth
 - max-statements
 - complexity
 - max-len
 - max-params
 - max-nested-callbacks

#### smelly code, what to do?

 - refactor
 - but unit test first!


#### resources

 - jshint
 - eslint
 - jscomplexity
 - escomplex
 - jasmine


copy / paste examples

 - jsinspect - detect copy-pasted and structurally similar code
 - jscpd - javascript copy paste detector

switch statement smell

"god" object

violates the "open/closed" principles OCP

Uncle Bob's SOLID Principles

"...software entities (classes, modules, functions, etc.) should be open to extension but closed"

strategy design pattern - a good answer for switch statements

#### magic strings refactoring

AST parser

eslint-plugin-smells

https://github.com/elijahmanor/eslint-plugin-smells

resources 

 - addy osmani's JavaScript Design Patterns eBook

### `this` abyss smell

`that` or `self` or `selfie`

alternatives: 

 1. `bind()`
 2. `forEach()` takes a second-parameter
 3. fat-arrow function =>
 4. .forEach functional pattern

eslint

 - no-this-assign
 - consistent-this  (only `that` or `self`)
 - no-extra-bind

### crisp concatenation smell

alternatives:

1. tweet-size javascript template engine by @thomasfuchs
2. ES6 template strings
3. SanitizeHTML
4. other micro-libraries

### repeat reassign smell

 - 
 - lodash flow

eslint - no-reassign

### inappropriate info

shopping cart / product


