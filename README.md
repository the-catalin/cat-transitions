<!--
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/the-catalin/cat-transitions)
-->
# cat-transitions

`cat-transitions` is a helper element that allows you to decorate Polymer elements.

includes:
`fade-in`
`slide-from-left`
`slide-from-right`
`slide-from-top`
`slide-from-bottom`
`scale-from-center`
`scale-from-left`
`scale-from-right`
`scale-from-top`
`scale-from-bottom`

## Demo

Currently, there is no dedicated demo, but the above transitions are used in the [Live Demo](http://webcomponents.online/cat-slider/) of [cat-slider](https://www.webcomponents.org/element/the-catalin/cat-slider)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install --save cat-transitions
```

Or [download as ZIP](https://github.com/the-catalin/cat-transitions/archive/master.zip)

## Usage

1. Import Web Components' polyfill (if needed):

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents-lite.min.js"></script>
    ```

2. Import behavior and transitions:

    ```html
    <!-- Import the behavior that allows you to add transitions to your elements -->
    <link rel="import" href="bower_components/cat-transitions/cat-transitions-runner-behavior.html">

    <!-- Import the transitions that you want to use: -->
    <link rel="import" href="bower_components/cat-transitions/transitions/fade-in.html">
    <link rel="import" href="bower_components/cat-transitions/transitions/scale-from-center.html">
    <link rel="import" href="bower_components/cat-transitions/transitions/slide-from-right.html">
    ```

3. Add `CatTransitionsRunnerBehavior` to your Polymer element:

	```js
	Polymer({      

	    is: 'my-custom-element',

	    behaviors: [Polymer.CatTransitionsRunnerBehavior],

	    properties: {
	    	...
	    }
	    ...
	```

4. Initialize an element with a desired transitions:

	```js
	this.addTransition({
	    name: 'fade-in',
        toNode: node1,
        fromNode: node2,
        function: 'ease',
        duration: 1,
        done: function() {
        	...
        }
	});
	```
	
	node1 and node2 are the elements that will be animated by the transition


## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## History

For detailed changelog, check [Releases](https://github.com/the-catalin/cat-transitions/releases).

## License

[The MIT License (MIT)](https://opensource.org/licenses/MIT)

Copyright (c) 2017 Catalin Ungureanu