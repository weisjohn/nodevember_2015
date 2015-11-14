# redux - tim griesser

http://redux.js.org/

programs are just managing state over time

facebook flux architecture

substack's tweet re:flux - NIH event emitter

redux is a different take on 

small pattern for composing event-emitters and reducers

talk by dan abramov - live reloading with time travel @ react europe
[https://github.com/gaearon/redux-devtools](redux-devtools)


### main ideas

 - single source of truth
 - unidirectional data flow
 - read only state
 - enforces immutability
 - composable
 - "it's all just functions"

state => view => update

inspired by Elm programming language

### actions

have a type, payload

### reducers

### stores

### subscribers

demo

actions get logged

how do you tap in and log the actions? - middleware

big idea: `invariant` - https://www.npmjs.com/package/invariant

### reselct

utilizing memo-izers

### component local state?

nothing

let's reconsider component boundaries

https://github.com/facebook/react/issues/4595

simplicity

Q&As 

smart vs dumb components
react would have just 1 top-down component w/ children
make some children smarter?

data-sync ?
relay? falcore?
something trying to bridge the gap
