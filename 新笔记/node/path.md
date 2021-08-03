### path.resolve
##### 从后往前执行,遇到"/"则终止,遇到"./"或无符号则拼接前面的路径,遇到"../"也拼接前面的路径但跳过前面路径的最后一级
```js
    var path = require("path")     //引入node的path模块
    path.resolve('/foo/bar', './baz')   // returns '/foo/bar/baz'
    path.resolve('/foo/bar', 'baz')   // returns '/foo/bar/baz'
    path.resolve('/foo/bar', '/baz')   // returns '/baz'
    path.resolve('/foo/bar', '../baz')   // returns '/foo/baz'
    path.resolve('home','/foo/bar', '../baz')   // returns '/foo/baz'
    path.resolve('home','./foo/bar', '../baz')   // returns '/home/foo/baz'
    path.resolve('home','foo/bar', '../baz')   // returns '/home/foo/baz'
```