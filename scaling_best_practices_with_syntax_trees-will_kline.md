# Scaling Best Practices with Syntax Trees - Will Kline

3 companies in 3 different industries

small companies with small teams

insurance company , looking at the codebase , quickly overwhelmed , first JS job

senior dev - "it's gonna take you 6 months to get up to speed"

couple weeks later, submitted first commit

### two years ago

moved to Colorado, 125 developers working on this project, more to learn, "don't worry, 6 months"

### today

CA Technologies - Raleigh Software, rearchitecting the FE

start-over - new tech, newer libraries, veteran devs, 

how do I get that knowledge? 

### testing

unit tests / integration tests

### user experience

protecting 

### developer experience

what is it like for us as developers to acquire that knowledge from our company

### documentation

document what this code does at an API level

### code reviews

### convention tests

we have conventions in code (style/API use/patterns)

 - linters
 - code analyzers
 - static analysis

### language conventions

### project conventions

what about our project conventions?

no matter what tool we're using, there are different ways that we've applied it from project to project?

how do we share knowledge?

what if we could write our own convention tests?

### convention test "frameworks"

 - common tests included
 - pluggable testing API
 - eslint for example

write your own tests against code not how or what code runs

// the meaning of life


### abstract syntax trees

lexical analysis

lexers / tokenizers

semantic meaning of the AST

### an example

unused variable

no semicolon

eslint

`no-unused-vars`

`semi` rule

`nested-if` case doesn't exist

AST node object:

 - type
 - test { type : identifier, name: someCondition}
 - consequent / alternate


### ESLINT 

 - builds our syntax tree for us
 - iterates over nodes in the tree
 - for each node, do we have a test?

eslint rule boilerplate 

common js module

```javascript
module.exports = function(context) {
    return {
        "IfStatement": function(context) {
            var ancestors = context.getAncestors(),
                parent = ancestors.pop(),
                gparent = ancestors.pop();

            if (parent.consequent === node ||
                (parent.type === "BlockStatement" && 
                parent.body.length === 1 &&
                grandparent.type === "IfStatement")) {
                    context.report(node, "Directly nested if.");
            }
        }
    }
}
```

### test 

valid and invalid (with errors)

### develop your own

esprima.org tool

parser which spits out syntax , tree, tokens

github.com/willkline/

### what else?

if it's a pattern 

convention tests
syntax trees
how to write a convention test using syntax trees

### go forth and test

implement existing tools
consider your project's convention
write your own convention tests

### 

"programs must be written for people to read, and only incidentally for computers to execute" - donald knuth

### currying favor

focus on things that are biting you

one clear way to write things

if you fail the test, you fail the build

use GitHub and do code reviews there

