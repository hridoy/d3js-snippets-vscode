# D3.js Snippets

**Now Updated for 4.10.0 release**

This extension for Visual Studio Code adds snippets for D3.js Javascript. More Snippets will be coming soon just release.

[Use Extension](https://github.com/hridoy/d3js-snippets-vscode/raw/master/img/preview.gif)

## Contributors
[![Hridoy](https://avatars.githubusercontent.com/hridoy?s=100)<br /><sub>Hridoy</sub>](http://github.com/hridoy)<br />
See the [CHANGELOG](https://github.com/hridoy/r-development-vscode/master/CHANGELOG.md) for the latest changes



# Usage

### Selections

sel ⇥ `d3.select('')`

sela ⇥ `d3.selectAll('')`

attr ⇥ `.attr('', )`

translate ⇥ `.attr('transform', 'translate(' + 0 + ',' + 0 + ')')`

style ⇥ `.style('fill', '#000')`

join ⇥

    d3.selectAll('')
        .data()

margin ⇥

    var margin = { top: 10, right: 10, bottom: 10, left: 10 };
        width = 960 - margin.left - margin.right,
        height = 640 - margin.top - margin.bottom;
    
    var svg = d3.select('body').append('svg')
        .attr('width', width + margin.left + margin.right)
        .attr('height', height + margin.top + margin.bottom)
      .append('g')
        .attr('transform', 'translate(' + margin.left + ',' + margin.top + ')');


### Data

dsv ⇥ `var dsv = d3.dsv(';', 'text/plain');`

csv ⇥

    d3.csv('/', function(d) {
      return {
    
      };
    
    }, function(err, rows) {
    
    });

json ⇥

    d3.json('/', function(err, data) {
    
    });
    

### SVG shapes

**circle ⇥**

    .enter().append('circle')
        .attr('cx', )
        .attr('cy', )
        .attr('r', )
        .style('fill', '#000');

**ellipse ⇥**

    .enter().append('ellipse')
        .attr('cx', )
        .attr('cy', )
        .attr('rx', )
        .attr('ry', )
        .style('fill', '#000');
        

**line ⇥**

    .enter().append('line')
        .attr('x1', )
        .attr('y1', )
        .attr('x2', )
        .attr('y2', )
        .style('stroke', '#000');


**rect ⇥**

    .enter().append('rect')
        .attr('x', )
        .attr('y', )
        .attr('width', )
        .attr('height', )
        .attr('rx', 0)
        .attr('ry', 0)
        .style('fill', '#000');

### Geography

map ⇥

    var projection = d3.geo.equirectangular()
        .center([0, 0])
        .scale(0)
        .translate([width / 2, height / 2]);
    
    var path = d3.geo.path()
        .projection(projection);
    
### Functions

fd ⇥ `function(d) { return ; }`

fdi ⇥ `function(d, i) { return ; }`

fn ⇥ `function() { return ; }`


### Miscellaneous

scale ⇥ `d3.scale.linear().domain([]).range([]);`

nest ⇥

    var nest = d3.nest()
        .key(function(d) { return d; })
        .entries([]);

locale ⇥

    var d3.locale.en_US = d3.locale({
      'decimal': '.',
      'thousands': ',',
      'grouping': [3],
      'currency': ['\$', ''],
      'dateTime': '%a %b %e %X %Y',
      'date': '%m/%d/%Y',
      'time': '%H:%M:%S',
      'periods': ['AM', 'PM'],
      'days': ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'],
      'shortDays': ['Sun', 'Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat'],
      'months': ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
      'shortMonths': ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec']
    });

Alternatively, press `Ctrl`+`Space` (Windows, Linux) or `Cmd`+`Space` (OSX) to activate snippets from within the editor.

## Installation

1. Install Visual Studio Code 1.10.0 or higher
2. Launch Code
3. From the command palette `Ctrl`-`Shift`-`P` (Windows, Linux) or `Cmd`-`Shift`-`P` (OSX)
4. Select `Install Extension`
5. Choose the extension
6. Reload Visual Studio Code
