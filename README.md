# newGit
node imporatnt

We recommend developers use setImmediate() in all cases because it's easier to reason about (and it leads to code that's compatible with a wider variety of environments, like browser JS.)


In essence, the names should be swapped. process.nextTick() fires more immediately than setImmediate() but this is an artifact of the past which is unlikely to change. Making this switch would break a large percentage of the packages on npm.


抛却maxTickDepth的问题，nextTick 和 setImmediate 主要的区别在于任务插入的位置

nextTick 的插入位置是在当前帧的末尾、io回调之前，如果nextTick过多，会导致io回调不断延后
setImmediate 的插入位置是在下一帧，不会影响io回调
