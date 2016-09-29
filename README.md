# newGit
node imporatnt

We recommend developers use setImmediate() in all cases because it's easier to reason about (and it leads to code that's compatible with a wider variety of environments, like browser JS.)


In essence, the names should be swapped. process.nextTick() fires more immediately than setImmediate() but this is an artifact of the past which is unlikely to change. Making this switch would break a large percentage of the packages on npm.
