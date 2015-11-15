# Blocking Across the Wire - Kyle Simpson

any sufficiently unlearned technology is undistinguishable from magic

@getify

###PrivilegeAwareness

These are not your privileges.

Inclusivity, not diversity.

male white educated heterosexual american employed

no solutions to inclusivity

more empathy for those that we work for / with

YouDontKnowJS.com

head of curiculum for maker square


### concurrency

briefly review

no mastery of the topic, open ended research project

two higher level tasks : making request , searching results

blocking is evil

interleave these tasks

### parallel

callback hell

### promises

promises remove time

from an api perspective

vertical chain instead of callbacks

use function declarations and then utilize those

### synchronous async

synchronous-looking async

generators , yield

the new baseline

generators + promises you have to

```javascript
run(function *cool() {

});
```

coroutines

```javascript
async function foobar() {
    var data = await getData();
}
```

there's a strong reason for having the ability to modify the scheduling


### csp

communicating sequential processes

channel-based concurrency

go-routines in golang

```
csp.go(function *one() {

})
```

channel: stream with buffer=1, back pressure

blocking...

```javascript
csp.go(function *one() {
    yield csp.put(ch, 42);
});
csp.go(function *two() {
    var answer = yield csp.take(ch);
});
```

removing the construct of time from your syntax


https://github.com/getify/a-tale-of-three-lists

channels between client / server


https://github.com/getify/remote-csp-channel

### one last thing

blocking from server <> client and they're fundamentally

multi-threaded programs

web-worker , browser-browser, browser-server, server-child processes

csp is a powerful, simple pattern for distributed, coordinated concureency
