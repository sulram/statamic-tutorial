# statamic-tutorial

### new site

https://docs.statamic.com/installing#command-line-installation

    statamic new awesome-site


### clear site
    
    php please clear:site
    php please clear:site --force
    
### new theme

    php please make:theme awesome-site
    cd site/themes/awesome-site
    yarn
    
    
### compiling assets with elixir

- https://laravel.com/docs/5.3/elixir
- https://learnstatamic.com/courses/126671/lectures/1856197
    
```    
// gulpfile.js

elixir(function(mix) {
    mix(sass(theme + '.scss', 'css/' + theme + '.css')
        .scripts('./js/site.js', './js/' + theme + '.js')
        .browserSync({ proxy: 'awesome-site.test' });
});

// after you can run

gulp watch

```

### serving files with valet

https://laravel.com/docs/5.6/valet#the-link-command

    valet link awesome-site
    
