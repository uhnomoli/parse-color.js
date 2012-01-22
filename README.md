# parse-color.js

parse-color.js is a simple JavaScript function for parsing colors in a variety of formats.

~~~ { javascript }
var color = parse_color('#000000');
~~~

It is also possible to generate a random color.

~~~ { javascript }
var random_color = parse_color();
~~~

As well as with a specific hue _(0-360)_.

~~~ { javascript }
var random_red = parse_color(0);
~~~


## Arguments

`parse_color()` accepts arguments in the following formats:

### Strings

_Note, for the following, case is ignored, for hex the hash sign is optional, and for rgb(a) spaces are optional._

+ `'#000'`
+ `'#000000'`
+ `'rgb(0, 0, 0)'`
+ `'rgba(0, 0, 0, 0.5)'`

### Objects

+ `{'h': 0, 's': 0, 'l': 0}`
+ `{'h': 0, 's': 0, 'v': 0}`
+ `{'r': 0, 'g': 0, 'b': 0}`


## Return

`parse_color()` returns an object with the following properties:

<table>
    <thead>
        <tr>
            <th>Property</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    
    <tbody>
        <tr>
            <td><code>hex</code></td>
            <td><em>string</em></td>
            <td>The hex value of the color without the hash sign.</td>
        </tr>
        
        <tr>
            <td><code>hsl</code></td>
            <td><em>object</em></td>
            <td>The HSL values of the color.</td>
        </tr>
        
        <tr>
            <td><code>hsv</code></td>
            <td><em>object</em></td>
            <td>The HSV values of the color.</td>
        </tr>
        
        <tr>
            <td><code>luma</code></td>
            <td><em>number</em></td>
            <td>The <a href="http://en.wikipedia.org/wiki/Luma_(video)">luma</a> <em>(Y'<sub>709</sub>)</em> of the color.</td>
        </tr>
        
        <tr>
            <td><code>rgb</code></td>
            <td><em>object</em></td>
            <td>The RGB values of the color.</td>
        </tr>
    </tbody>
</table>
