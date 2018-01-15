# &lt;juicy-highlight&gt;

`<juicy-highlight>` is a Custom Element that highlights a DOM element on screen using a SVG overlay and/or border

## Demo

[Check it live!](http://juicy.github.io/juicy-highlight)

## Usage

1. Install the component using [Bower](http://bower.io/):

    ```sh
    $ bower install juicy-highlight --save
	```

2. Import Custom Element:

    ```html
    <link rel="import" href="bower_components/juicy-highlight/juicy-highlight.html">
    ```

3. Start using it!

    ```html
    <juicy-highlight id="border" strokeWidth="2" strokeColor="#222222" strokeOffset="4"></juicy-highlight>
    <script>
		document.addEventListener("DOMContentLoaded", function() {
			setTimeout(function() {
				document.querySelector("#border").show(document.querySelectorAll("li"));
			}, 100);
		});
	</script>
    ```

## Attributes

Attribute         | Type           | Default      | Description
---               | ---            | ---          | ---
`overlay`         | *Boolean*      | `false`      | Whether the overlay should be displayed
`strokeWidth`     | *Number*       | `1`          | Border width in px
`strokeColor`     | *String*       | `#000000`    | Border color
`strokeOffset`    | *Number*       | `1`          | Border offset (distance from the element) in px
`fill`            | *Color*        | `none`       | Color to fill selected area. Accepts HEX `#FFFF00`, RGB `rgb(255,255,0)`, RGBA `rgba(255,255,0,0.5)`, and color name `yellow`.

## Private properties

Property      | Type  | Description
---           | ---   | ---
`overlayRect` | *SVG* | The overlay SVG element.
`focusRect`   | *SVG* | The focus SVG element.

## Methods

Name               | Param name | Type                                     | Description
---                | ---        | ---                                      | ---
`show`             |            |                                          | Highlight element(s)
                   | elements   | *null*, *Element*, *Array* or *NodeList* | DOM element or array of those to highlight. If no elements are specified, only overlay will be shown (if applicable)
`hide`             |            |                                          | Hide current highlight

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

MIT
