# nodemon-glob-bug
Reproduce ignoreRoot + ignore directories glob problem

This repository is configured following [nodemon configuration](https://github.com/remy/nodemon/blob/master/doc/sample-nodemon.md) 

# reproduce

```shell
$ npm install
$ npm start
# In another shell, execute 'touch node_modules/test-dir/index.js'
```

At this point nodemon should have reloaded, because accordingly to [nodemon.json](nodemon.json) `ignore` includes all `node_modules` and then removes from the list `node_modules/test-dir`.
