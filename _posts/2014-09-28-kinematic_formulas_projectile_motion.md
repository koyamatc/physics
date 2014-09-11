---
title: physics
layout: post
postTitle: Kinematic formulas and projectile motion 
categories: OneD-Motion
---

### Average velocity for constant acceleration

<div class="panel">
	+:to the right<br>
	-:to the left<br>
	$$initial \quad velocity:\vec{v_i}=5m/s$$
	$$final \quad velocity:\vec{v_f}=\vec{v_i}+(\Delta t)\vec{a_{c}}$$
	$$constant \quad acceleration:\vec{a_{c}}=2m/s^2$$
	$$time:\Delta t=4s$$
	How far does he travel?  
</div>

<div class="row">
	<div class="col-sm-6">
		<div id="svg01"></div>
	</div>
	<div class="col-sm-6">
		$$\vec{v_{f}}=5\frac{m}{s}+(4s)(2\frac{m}{s^2})
		=5\frac{m}{s}+8\frac{m}{s}=13\frac{m}{s}$$
		$$\vec{s_{1}}=\vec{v_{i}}*\Delta t 
		= 5\frac{m}{s}*(4s) = 20m$$
		$$\vec{s_{2}}=\frac{1}{2}*(\vec{v_{f}}-\vec{v_{i}})*\Delta t 
		= \frac{1}{2}*(13-5)\frac{m}{s}*(4s) = 16m$$
		$$\vec{s}=\vec{s_{1}}+\vec{s_{2}}=20m+16m=36m$$

		--*--*--*--*--*--*--*--*--*--*--

		$$\vec{s}=\vec{v_{i}}*\Delta t + \frac{1}{2}*(\vec{v_{f}}-\vec{v_{i}})*\Delta t$$
		$$\quad = \Delta t*(\vec{v_{i}}+\frac{1}{2}*(\vec{v_{f}}-\vec{v_{i}}))
		=\Delta t*(\vec{v_{i}}+\frac{1}{2}\vec{v_{f}}-\frac{1}{2}\vec{v_{i}})$$
		$$\quad = \Delta t*(\frac{1}{2}\vec{v_{i}}+\frac{1}{2}\vec{v_{f}})$$
		$$\quad = \Delta t*\frac{1}{2}(\vec{v_{i}}+\vec{v_{f}})$$

		<div class="panel panel-warning">
			<div class="panel-heading">Average Velocity</div>
			$$\frac{1}{2}(\vec{v_{i}}+\vec{v_{f}})$$	
		</div>
		$$\vec{s}=\Delta t*\frac{1}{2}(\vec{v_{i}}+\vec{v_{f}})$$
		$$\quad =4s*\frac{1}{2}(5m/s+13m/s)=4s*9m/s=36m$$
	</div>
</div>

------

### Acceleration of aircraft carrier take off

<div class="panel">
	$$runway = 80m$$
	$$initial \quad velocity:\vec{v_{i}} = 0m/s$$
	$$final \quad velocity:\vec{v_{f}} = 260\frac{km}{hour}
	=260*\frac{km}{hour}*\frac{1000}{1}*\frac{m}{km}*\frac{1}{3600}*\frac{hour}{s}
	=72m/s$$
</div>
<div class="panel">
	$$displacement:\vec{s}=\vec{v_{a}}*\Delta t$$
	$$constant \quad acceleration:\vec{a_{c}}= \frac{\Delta \vec{v}}{\Delta t}$$
	$$change \quad in \quad velocity:\Delta \vec{v}=\vec{v_{f}}-\vec{v_{i}}$$
	$$change \quad in \quad time:\Delta t$$
	$$average \quad velocity:\vec{v_{a}}=\frac{\vec{v_{f}}+\vec{v_{i}}}{2}$$
</div>

$$\vec{a_{c}}= \frac{\Delta \vec{v}}{\Delta t}
\quad \rightarrow \quad 
\Delta t=\frac{\Delta \vec{v}}{\vec{a_{c}}}
=\frac{\vec{v_{f}}-\vec{v_{i}}}{\vec{a_{c}}}$$
$$\vec{s}=\vec{v_{a}}*\Delta t
=\frac{\vec{v_{f}}+\vec{v_{i}}}{2}*
\frac{\vec{v_{f}}-\vec{v_{i}}}{\vec{a_{c}}}
=\frac{\vec{v_{f}}^2-\vec{v_{i}}^2}{2\vec{a_{c}}}$$
$$\qquad\qquad\qquad\qquad\downarrow$$
$$\vec{a_{c}}=\frac{\vec{v_{f}}^2-\vec{v_{i}}^2}{2\vec{s}}
=\frac{(72m/s)^2-(0m/s)^2}{2*80m}
=\frac{5184m^2/s^2}{160m}
=32.4m/s^2$$
$$\Delta t=\frac{\vec{v_{f}}-\vec{v_{i}}}{\vec{a_{c}}}
=\frac{72m/s}{32.4m/s^2}
=2.2s$$



------

### Deriving displacement as a function of time, acceleration and initial velocity

### Plotting projectile displacement, acceleration and velocity

### Projectile height given time

### Deriving max projectile displacement given time

### Impact velocity given height

### Viewing g as the value of Earth's gravitational field near the surface 


<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script>

  var height = 400;
  var width = 400;

/**
	average velocity
*/

var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",height)
                .attr("width",width);

/* 軸 */
var scale01X = d3.scale.linear()
                .domain([0,6])
                .range([50,380]);
var scale01Y = d3.scale.linear()
                .domain([0,15])
                .range([360,30]);

var xAxis01 = d3.svg.axis()
                  .scale(scale01X)
                  .tickValues([0, 1, 2, 3, 4, 5, 6])
                  .tickPadding(5)
                  .tickFormat(d3.format("d"));

var xAxis01Group = svg01.append("g")
                      .attr("transform","translate(0,"+ scale01Y(0)+")")
                      .attr("stroke","white")
                      .style("fill","none")
                      .call(xAxis01);   

var yAxis01 = d3.svg.axis()
                  .scale(scale01Y)
                  .orient(["left"])
                  .tickPadding(0)
                  .tickValues([0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15]);

var yAxis01Group = svg01.append("g")
.attr("transform","translate(" + scale01X(0) + ",0)")
                      .attr("stroke","white")
                      .style("fill","none")
                      .call(yAxis01);                                              
var curve011Data = [
	{"x":0,"y0":0,"y1":5},
	{"x":1,"y0":0,"y1":5},
	{"x":2,"y0":0,"y1":5},
	{"x":3,"y0":0,"y1":5},
	{"x":4,"y0":0,"y1":5},
];
var curve012Data = [
	{"x":0,"y0":5,"y1":5},
	{"x":1,"y0":5,"y1":7},
	{"x":2,"y0":5,"y1":9},
	{"x":3,"y0":5,"y1":11},
	{"x":4,"y0":5,"y1":13}
];
var area01 = d3.svg.area()
        .x(function(d,i) { return scale01X(d.x);})
        .y0(function(d,i) { return scale01Y(d.y0);})
        .y1(function(d,i) { return scale01Y(d.y1);});

svg01.append("path")
        .attr("d", area01(curve011Data))
        .attr("fill", "blue");
svg01.append("path")
        .attr("d", area01(curve012Data))
        .attr("fill", "green");

// grid
var gridX01 = [1,2,3,4,5,6];
var gridY01 = [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15];

svg01.selectAll(".gridX01")
	.data(gridX01)
	.enter()
	.append("line")
	.attr("x1", function(d){return scale01X(d);})
	.attr("y1", function(d){return scale01Y(0);})
	.attr("x2", function(d){return scale01X(d);})
	.attr("y2", function(d){return scale01Y(15);})
	.attr("class","gridX01")
	.attr("opacity",10)
	.attr("stroke","#666");

svg01.selectAll(".gridY01")
	.data(gridY01)
	.enter()
	.append("line")
	.attr("x1", function(d){return scale01X(0);})
	.attr("y1", function(d){return scale01Y(d);})
	.attr("x2", function(d){return scale01X(6);})
	.attr("y2", function(d){return scale01Y(d);})
	.attr("class","gridY01")
	.attr("opacity",10)
	.attr("stroke","#666");

svg01.append("line")
	.attr("x1", function(d){return scale01X(0);})
	.attr("y1", function(d){return scale01Y(5);})
	.attr("x2", function(d){return scale01X(5);})
	.attr("y2", function(d){return scale01Y(15);})
	.attr("class","gridY01")
	.attr("stroke","#fff");

  /* texts */    
  var text01Data = [
        {"x":-0.5,"y":16,"text":"V(m/s)"},
        {"x":5.2,"y":-1.5,"text":"t(sec)"},
        {"x":1,"y":3,"text":"displacement 1"},
        {"x":1,"y":6,"text":"displacement 2"} ];    
  
  svg01.selectAll(".text01")
      .data(text01Data)
      .enter()
      .append("text")
      .attr("class","text01")
      .attr("x",function(d){return scale01X(d.x)})
      .attr("y",function(d){return scale01Y(d.y)})
      .text(function(d){return d.text})
      .attr("stroke","#fff")
      .attr("font-size","16px")
      .style("fill","white");        


</script>
