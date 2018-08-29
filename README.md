# flexbox

This stylesheet gives you a set of classes you can use to create a responsive flexbox grid in your web application. It is very similar to [angular material](https://material.angularjs.org) flexbox classes. It's written in scss, you can specify breakpoints for different media query ranges.

Note that this project is still a work in progress. The released version contains only features that should work perfectly. There is just a basic set of flexbox classes, but more will be added soon.

## Installation

Download css file or scss files and add them to your html project.

## Usage

### Including flexbox stylesheet in a project:

To use the css as it is add a link tag with its source path inside head of your html document.

To modify viewport width breakpoints, instead of using the css file, import scss files and change the variables:

``` scss
$fb-layout-sm: 768px;
$fb-layout-md: 1024px;

@import 'flexbox';
```

### Viewport width breakpoints:

These are the preset breakpoints:

``` scss
$fb-layout-sm: 600px;
$fb-layout-md: 960px;
$fb-layout-lg: 1280px;
$fb-layout-xl: 1920px;
```

Breakpoints define the lowest widths of each media query range. There are five of them:

```
Extra small [xs]:    0px -  599px
Small       [sm]:  600px -  959px
Medium      [md]:  960px - 1279px
Large       [lg]: 1280px - 1919px
Extra large [xl]: 1920px and more
```

Extra options:

```
Greater than extra small [gt-xs]:  600px and more
Greater than small       [gt-sm]:  960px and more
Greater than medium      [gt-md]: 1280px and more
Less than medium         [lt-md]:    0px -  959px
Less than large          [lt-lg]:    0px - 1279px
Less than extra large    [lt-xl]:    0px - 1919px
```

Usage of breakpoints is very simple to make your project responsive. Each class containing the media query range abbreviation will only add the styles to the element if the viewport width is within the media query range.

**Exception!** There is one class excluded from the responsive classes, `fb-layout-fill` can only be set regardless of the viewport's width.

### Class names:

Class names allways begin with a `fb-` prefix to avoid conflicts with other class names in your project.

Class names consist of:

```
                (optional)
[prefix]-[name]-[media-query-range]-[value]

// fb-flex-xs-20
[fb]-[flex]-[xs]-[20]

// fb-layout-lt-xl-row:
[fb]-[layout]-[lt-xl]-[row]

// fb-layout-align-md-center-center:
[fb]-[layout-align]-[md]-[center-center]
```

**Exception!** There is one class that doesn't have a value part, `fb-flex` (or `fb-flex-sm` etc)

### Set of style classes:

Description will be added soon

```
fb-layout-fill

fb-layout-row (fb-layout-md-row)
fb-layout-column (fb-layout-md-column)

fb-layout-wrap (fb-layout-md-wrap)
fb-layout-no-wrap

fb-layout-align-start-stretch (fb-layout-align-md-start-stretch)
fb-layout-align-start-start
fb-layout-align-start-center
fb-layout-align-start-end

fb-layout-align-center-stretch
fb-layout-align-center-start
fb-layout-align-center-center
fb-layout-align-center-end

fb-layout-align-end-stretch
fb-layout-align-end-start
fb-layout-align-end-center
fb-layout-align-end-end

fb-layout-align-space-around-stretch
fb-layout-align-space-around-start
fb-layout-align-space-around-center
fb-layout-align-space-around-end

fb-layout-align-space-between-stretch 
fb-layout-align-space-between-start
fb-layout-align-space-between-center
fb-layout-align-space-between-end

fb-flex (fb-flex-md)

fb-flex-5 (fb-flex-md-5)
fb-flex-10
...
fb-flex-95
fb-flex-100

fb-flex-33
fb-flex-66

fb-flex-order--20 (flex-order-md--20)
fb-flex-order--19
...
fb-flex-order-19
fb-flex-order-20

fb-hide (fb-hide-gt-sm)
```


## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/pavelccz/flexbox.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

