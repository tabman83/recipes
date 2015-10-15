# BrowserSync modRewrite

This describes how to configure the modRewrite module of BrowserSync in your Gulp task to support
HTML5 applications and live reloading of your CSS.

```
gulp.task('ws', function(cb) {
  browserSync({
    server: {
      baseDir: paths.dirs.build,
      middleware: [
        modRewrite([
          '^[^\\.]*$ /index.html [L]'
        ])
      ]
    },
    port: 8000,
    notify: false,
    open: false
  }, cb);
});
```

Credits:
https://github.com/BrowserSync/browser-sync/issues/554#issuecomment-89410081
