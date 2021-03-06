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
		final velocity
		$$\vec{v_{f}}=5\frac{m}{s}+(4s)(2\frac{m}{s^2})
		=5\frac{m}{s}+8\frac{m}{s}=13\frac{m}{s}$$
		displacement1 (area of blue rectangle)
		$$\vec{s_{1}}=\vec{v_{i}}*\Delta t 
		= 5\frac{m}{s}*(4s) = 20m$$
		displacement2 (area of green triangle)
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

<div class="panel">
	Throw a ball straight up into the air.
	$$go \quad upward:positive$$
	$$go \quad downward:negative$$
	$$initial \quad velocity:\vec{v_{i}}=19.6m/s$$
	$$gravity \quad of \quad the \quad earth:g=9.8m/s^2$$
	Earth's gravity accelerate an object downward to the center of Earth. So..
	$$g=-9.8m/s^2$$
</div>
<div class="panel">
	$$\vec{F}=m\vec{a} 
	\qquad 
	(\vec{F}:force \quad 
	m:mass \quad 
	\vec{a}:acceleration=g\quad assume \quad constant)$$

	$$\vec{F}=G\frac{m_{1}m_{2}}{r^2}$$
	$$ \quad (\vec{F}:force$$
	$$ \quad 
	m_{1}:mass \quad of \quad one \quad object
	\quad
	m_{2}:mass \quad of \quad another \quad object$$
	$$ \quad
	r:distance \quad between \quad 2 \quad objects
	:radius \quad of \quad Earth)$$
</div>

displacement is
$$\vec{s}=\vec{v_{avg}} \centerdot \Delta t$$
$$assuming \quad constant \quad \vec{a}$$
average velocity is
$$\vec{v_{avg}}=\frac{\vec{v_{i}}+\vec{v_{f}}}{2}$$
final velocity is
$$\vec{v_{f}}=\vec{v_{i}}+\vec{a} \centerdot \Delta t$$ 

$$\vec{s}=
\frac{\vec{v_{i}}+\vec{v_{i}}+\vec{a} \centerdot \Delta t}{2}
\centerdot \Delta t
=(\frac{2\vec{v_{i}}}{2}
+\frac{\vec{a}\Delta t}{2})\centerdot\Delta t
=\vec{v_{i}} \centerdot \Delta t 
+ \frac{1}{2}\vec{a}(\Delta t)^2$$

<div class="panel">
	<div class="panel^heading">
		Use this equation in following section.
	</div>
$$\vec{s}
=\vec{v_{i}} \centerdot \Delta t 
+ \frac{1}{2}\vec{a}(\Delta t)^2$$
</div>

------

### Plotting projectile displacement, acceleration and velocity

<div class="row">
	<div class="col-sm-6">
		<div class="panel">
			displacement is
			$$\vec{s}
			=\vec{v_{i}} \centerdot \Delta t 
			+ \frac{1}{2}\vec{a}(\Delta t)^2$$
			acceleration is
			$$\vec{a_{g}=-9.8m/s^2}$$
			final velocity is
			$$\vec{v_{f}}=\vec{v_{i}}+\vec{a} \centerdot \Delta t$$ 
		</div>
	</div>
	<div class="col-sm-3">
		<table class="table">
			<tr>
				<th>$$\Delta t$$</th>
				<th>$$\vec{v_{f}}$$</th>
				<th>$$\vec{s}$$</th>
			</tr>	
			<tr>
				<td>0</td>
				<td>19.6</td>
				<td>0</td>
			</tr>
			<tr>
				<td>1</td>
				<td>9.8</td>
				<td>14.7</td>
			</tr>
			<tr>
				<td>2</td>
				<td>0</td>
				<td>19.6</td>
			</tr>
			<tr>
				<td>3</td>
				<td>-9.8</td>
				<td>14.7</td>
			</tr>
			<tr>
				<td>4</td>
				<td>-19.6</td>
				<td>0</td>
			</tr>
		</table>
	</div>

</div>
<div class="row">
	<div class="col-sm-4">
		<div id="svg02"></div>
	</div>
	<div class="col-sm-4">
		<div id="svg03"></div>
	</div>
	<div class="col-sm-4">
		<div id="svg04"></div>
	</div>
</div>


------

### Projectile height given time

<div class="panel-body">
	Throw a ball in the air.	How high in the air?
</div>

<div class="panel">
	Air resistance is negligible.

	$$\Delta t = 5seconds \quad in \quad the \quad air.$$
	time upward = time downward

	<h4>case upward</h4>
	$$\Delta t_{up}=2.5seconds$$
	$$initial \quad velocity:\vec{v_{i}}$$
	$$final \quad velocity:\vec{v_{f}}=0$$
	$$gravity \quad acceleration:\vec{a_{g}}=-9.8m/s^2$$ 
	$$change \quad in \quad velocity:
	\Delta \vec{v}=\vec{v_{f}}-\vec{v_{i}}
	=(0-\vec{v_{i}})
	=-\vec{v_{i}}$$
	$$\Delta \vec{v} = \vec{a} \centerdot \Delta t$$
</div>

$$\Delta \vec{v} =-9.8m/s^2 \centerdot 2.5s=-24.5m/s$$
$$\Delta \vec{v} =-\vec{v_{i}}=-24.5m/s$$
$$\vec{v_{i}}=24.5m/s$$

<div class="panel">
	$$displacement:\vec{s} = \vec{v_{avg}} \centerdot \Delta t$$
</div>
$$\vec{s}=\frac{24.5 + 0}{2}m/s \centerdot 2.5s=30.625m$$

-------------------

### Deriving max projectile displacement given time

<div class="panel">
	$$\Delta t:total \quad time \quad in \quad the \quad air $$
	$$\Delta t_{up}= \frac{\Delta t}{2}
	\quad 時間全体の半分が上昇する時間$$
	$$initial \quad velocity:\vec{v_{i}}$$
	$$final \quad velocity:\vec{v_{f}}=0$$
	$$change \quad in \quad velocity:
	\Delta \vec{v}=\vec{v_{f}}-\vec{v_{i}}
	=0-\vec{v_{i}}
	=-\vec{v_{i}}$$
	$$\Delta \vec{v} = \vec{a} \centerdot \Delta t$$
	$$average \quad velocity:\frac{\vec{v_{i}}+\vec{v_{f}}}{2}$$ 
	$$displacement:\vec{s} = \vec{v_{avg}} \centerdot \Delta t$$
</div>
change in velocity equals to minus initial velocity
$$\Delta \vec{v} 
=-\vec{v_{i}}
= -9.8m/s^2 \centerdot \frac{\Delta t}{2}$$
initial velocity is
$$\vec{v_{i}}=4.9m/s^2 \centerdot \Delta t$$

displacement is
$$\vec{s} 
= \frac{\vec{v_{i}}+\vec{v_{f}}}{2} \centerdot \frac{\Delta t}{2}
\quad
=\frac{4.9m/s^2 \centerdot \Delta t+0}{2}\centerdot \frac{\Delta t}{2}
\quad
=\frac{4.9m/s^2 \centerdot (\Delta t)^2}{4}
\quad
=1.225m/s^2 \centerdot (\Delta t)^2$$

<div class="panel panel-info">
	<div class="panel-heading">
		max displacement
	</div>
	$$\vec{s_{max}}=1.225m/s^2 \centerdot (\Delta t)^2$$
</div>


### Impact velocity given height

<div class="row">
	<div class="col-sm-2">
		<div id="svg05"></div>
	</div>
	<div class="col-sm-3">
		$$$$
		$$\vec{v_{i}}= 0$$
		$$$$
		$$$$
		$$$$
		$$$$
		$$\vec{v_{f}}= ?\quad negative \quad value$$
	</div>
	<div class="col-sm-7">
		<div class="panel">
			<div class="panel-heading">
				Throw a rock off to the ground.
				How fast is it going to be  right before it hits to the ground?  
			</div>
			$$air \quad is \quad negligible$$
			$$height:h \quad meters$$
			acceleration of gravity is assumed constant and 
			$$\vec{a_{c}}=-9.8m/s^2$$
			$$upward:positive \quad value$$
			$$downward:negative \quad value$$
			$$initial \quad velocity:\vec{v_{i}}=0m/s$$
			$$displacement:\vec{s}=\vec{v_{avg}} \centerdot \Delta t$$
		</div>
	</div>
</div>
$$average \quad velocity \quad is \quad 
\frac{\vec{v_{i}}+\vec{v}_{f}}{2}
=\frac{0+\vec{v}_{f}}{2}
=\frac{\vec{v}_{f}}{2}$$

$$displacement \quad is \quad
\vec{s}=\frac{\vec{v}_{f}}{2} \centerdot \Delta t$$

$$\Delta t \quad is \quad
\Delta \vec{v}=\vec{a} \centerdot \Delta t 
\rightarrow \Delta t=\frac{\Delta \vec{v}}{\vec{a}}$$

$$displacement \quad is \quad
\vec{s}=\frac{\vec{v}_{f}}{2} \centerdot 
\frac{\Delta \vec{v}}{\vec{a}}$$

$$change \quad in \quad velocity \quad is \quad
\Delta \vec{v}=\vec{v_{f}}-\vec{v_{i}}
=\vec{v_{f}}-0
=\vec{v_{f}}$$

$$displacement \quad is \quad
\vec{s}=\frac{\vec{v}_{f}}{2} \centerdot 
\frac{\vec{v_{f}}}{\vec{a}}$$

$$\qquad \qquad \swarrow$$

$$2\vec{a}\vec{s}=(\vec{v_{f}})^2$$
$$\vec{s} = -h 
\quad A \quad rock \quad falls \quad down, \quad so \quad
\vec{s} \quad is \quad negative$$
$$-19.6\frac{m}{s^2} \centerdot -hm = (\vec{v_{f}})^2$$
$$19.6\frac{m^2}{s^2} \centerdot h = (\vec{v_{f}})^2$$
$$final \quad velocity \quad is \quad negative \quad and \quad
\vec{v_{f}}=-\sqrt{19.6h}\frac{m}{s}$$

$$h=5m \rightarrow \vec{v_{f}}=-9.9m/s$$

<div class="panel panel-danger">
	<div class="panel-heading">impact velocity</div>
	<div class="panel-body">
		$$\vec{v_{f}}=-\sqrt{19.6h}\frac{m}{s}$$
	</div>
</div>

----------------

### Viewing g as the value of Earth's gravitational field near the surface 

$$g=-9.81m/s^2$$
g is the acceleration due to gravity near Earth's surface
for an object in free fall to the center of the Earth.



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

/**
	displacement
*/

var svg02 = d3.select("#svg02")
                .append("svg")
                .attr("height",height)
                .attr("width",width);

/* 軸 */
var scale02X = d3.scale.linear()
                .domain([-0.5,4.2])
                .range([50,380]);
var scale02Y = d3.scale.linear()
                .domain([0,22])
                .range([360,30]);

var xAxis02 = d3.svg.axis()
                  .scale(scale02X)
                  .tickValues([0, 1, 2, 3, 4])
                  .tickPadding(5)
                  .tickFormat(d3.format("d"));

var xAxis02Group = svg02.append("g")
                      .attr("transform","translate(0,"+ scale02Y(0)+")")
                      .attr("stroke","white")
                      .style("fill","none")
                      .call(xAxis02);   

var yAxis02 = d3.svg.axis()
                  .scale(scale02Y)
                  .orient(["left"])
                  .tickPadding(0)
                  .tickValues([5,10,15,20]);

var yAxis02Group = svg02.append("g")
.attr("transform","translate(" + scale02X(0) + ",0)")
                      .attr("stroke","white")
                      .style("fill","none")
                      .call(yAxis02);                            



// grid
var gridX02 = [1,2,3,4];
var gridY02 = [5,10,15,20];

svg02.selectAll(".gridX02")
	.data(gridX02)
	.enter()
	.append("line")
	.attr("x1", function(d){return scale02X(d);})
	.attr("y1", function(d){return scale02Y(0);})
	.attr("x2", function(d){return scale02X(d);})
	.attr("y2", function(d){return scale02Y(20);})
	.attr("class","gridX02")
	.attr("opacity",10)
	.attr("stroke","#666");

svg02.selectAll(".gridY02")
	.data(gridY02)
	.enter()
	.append("line")
	.attr("x1", function(d){return scale02X(0);})
	.attr("y1", function(d){return scale02Y(d);})
	.attr("x2", function(d){return scale02X(4);})
	.attr("y2", function(d){return scale02Y(d);})
	.attr("class","gridY02")
	.attr("opacity",10)
	.attr("stroke","#666");

  /* texts */    
  var text02Data = [
        {"x":-0.5,"y":21,"text":"m"},
        {"x":4.1,"y":-1.5,"text":"t"},
        {"x":1.5,"y":21,"text":"displacement"} ];    
  
  svg02.selectAll(".text02")
      .data(text02Data)
      .enter()
      .append("text")
      .attr("class","text02")
      .attr("x",function(d){return scale02X(d.x)})
      .attr("y",function(d){return scale02Y(d.y)})
      .text(function(d){return d.text})
      .attr("stroke","#fff")
      .attr("font-size","16px")
      .style("fill","white");        

var point02Data = [0,14.7,19.6,14.7,0];

svg02.selectAll(".point02")
				.data(point02Data)
				.enter()
				.append("circle")
				.attr("cx",function(d,i){return scale02X(i) })
				.attr("cy",function(d,i){return scale02Y(d) })
				.attr("r",4)
				.attr("stroke","gold")
				.style("fill","gold")
				.attr("class","point02");

	var line02Data = [];
	for (var i = 0; i < 4.1; i=i+0.1) {
	 				line02Data.push(i);
	 			}; 			
	var line02 = d3.svg.line()
        .x(function(d) { return scale02X(d); })
        .y(function(d) { 
        	return scale02Y(19.6*d + (-9.8*d*d)/2); })
        .interpolate("linear");

 	svg02.append("path")
          .attr("d", line02(line02Data))
          .attr("stroke", "gold")
          .attr("stroke-width", 2)
          .attr("fill", "none");   

/**
	velocity
*/

var svg03 = d3.select("#svg03")
                .append("svg")
                .attr("height",height)
                .attr("width",width);

/* 軸 */
var scale03X = d3.scale.linear()
                .domain([-0.5,4.2])
                .range([50,380]);
var scale03Y = d3.scale.linear()
                .domain([-22,22])
                .range([360,30]);

var xAxis03 = d3.svg.axis()
                  .scale(scale03X)
                  .tickValues([1, 2, 3, 4])
                  .tickPadding(5)
                  .tickFormat(d3.format("d"));

var xAxis03Group = svg03.append("g")
                      .attr("transform","translate(0,"+ scale03Y(0)+")")
                      .attr("stroke","white")
                      .style("fill","none")
                      .call(xAxis03);   

var yAxis03 = d3.svg.axis()
                  .scale(scale03Y)
                  .orient(["left"])
                  .tickPadding(0)
                  .tickValues([-20,-10,0,10,20]);

var yAxis03Group = svg03.append("g")
.attr("transform","translate(" + scale03X(0) + ",0)")
                      .attr("stroke","white")
                      .style("fill","none")
                      .call(yAxis03);                                              
// grid
var gridX03 = [1,2,3,4];
var gridY03 = [-20,-10,10,20];

svg03.selectAll(".gridX03")
	.data(gridX03)
	.enter()
	.append("line")
	.attr("x1", function(d){return scale03X(d);})
	.attr("y1", function(d){return scale03Y(-20);})
	.attr("x2", function(d){return scale03X(d);})
	.attr("y2", function(d){return scale03Y(20);})
	.attr("class","gridX03")
	.attr("opacity",10)
	.attr("stroke","#666");

svg03.selectAll(".gridY03")
	.data(gridY03)
	.enter()
	.append("line")
	.attr("x1", function(d){return scale03X(0);})
	.attr("y1", function(d){return scale03Y(d);})
	.attr("x2", function(d){return scale03X(4);})
	.attr("y2", function(d){return scale03Y(d);})
	.attr("class","gridY03")
	.attr("opacity",10)
	.attr("stroke","#666");

var point03Data = [19.6,9.8,0,-9.8,-19.6];

svg03.selectAll(".point03")
				.data(point03Data)
				.enter()
				.append("circle")
				.attr("cx",function(d,i){return scale03X(i) })
				.attr("cy",function(d,i){return scale03Y(d) })
				.attr("r",4)
				.attr("stroke","gold")
				.style("fill","gold")
				.attr("class","point03");

	var line03Data = [];
	for (var i = 0; i <= 4; i++) {
	 				line03Data.push(i);
	 			}; 			
	var line03 = d3.svg.line()
        .x(function(d) { return scale03X(d); })
        .y(function(d) { return scale03Y(19.6 - (9.8*d)); })
        .interpolate("linear");

 	svg03.append("path")
          .attr("d", line03(line03Data))
          .attr("stroke", "gold")
          .attr("stroke-width", 2)
          .attr("fill", "none");   
  
  /* texts */    
  var text03Data = [
        {"x":-0.5,"y":21.5,"text":"m/s"},
        {"x":4.1,"y":-2,"text":"t"},
        {"x":1.5,"y":21,"text":"Velocity"} ];    
  
  svg03.selectAll(".text03")
      .data(text03Data)
      .enter()
      .append("text")
      .attr("class","text03")
      .attr("x",function(d){return scale03X(d.x)})
      .attr("y",function(d){return scale03Y(d.y)})
      .text(function(d){return d.text})
      .attr("stroke","#fff")
      .attr("font-size","16px")
      .style("fill","white");        

/**
	acceleration
*/

var svg04 = d3.select("#svg04")
                .append("svg")
                .attr("height",height)
                .attr("width",width);

/* 軸 */
var scale04X = d3.scale.linear()
                .domain([-0.5,4.2])
                .range([50,380]);
var scale04Y = d3.scale.linear()
                .domain([-22,22])
                .range([360,30]);

var xAxis04 = d3.svg.axis()
                  .scale(scale04X)
                  .tickValues([1, 2, 3, 4])
                  .tickPadding(5)
                  .tickFormat(d3.format("d"));

var xAxis04Group = svg04.append("g")
                      .attr("transform","translate(0,"+ scale04Y(0)+")")
                      .attr("stroke","white")
                      .style("fill","none")
                      .call(xAxis04);   

var yAxis04 = d3.svg.axis()
                  .scale(scale04Y)
                  .orient(["left"])
                  .tickPadding(0)
                  .tickValues([-20,-10,0,10,20]);

var yAxis04Group = svg04.append("g")
.attr("transform","translate(" + scale04X(0) + ",0)")
                      .attr("stroke","white")
                      .style("fill","none")
                      .call(yAxis04);                                              
// grid
var gridX04 = [1,2,3,4];
var gridY04 = [-20,-10,10,20];

svg04.selectAll(".gridX04")
	.data(gridX04)
	.enter()
	.append("line")
	.attr("x1", function(d){return scale04X(d);})
	.attr("y1", function(d){return scale04Y(-20);})
	.attr("x2", function(d){return scale04X(d);})
	.attr("y2", function(d){return scale04Y(20);})
	.attr("class","gridX04")
	.attr("opacity",10)
	.attr("stroke","#666");

svg04.selectAll(".gridY04")
	.data(gridY04)
	.enter()
	.append("line")
	.attr("x1", function(d){return scale04X(0);})
	.attr("y1", function(d){return scale04Y(d);})
	.attr("x2", function(d){return scale04X(4);})
	.attr("y2", function(d){return scale04Y(d);})
	.attr("class","gridY04")
	.attr("opacity",10)
	.attr("stroke","#666");

var point04Data = [-9.8,-9.8,-9.8,-9.8,-9.8];

svg04.selectAll(".point04")
				.data(point04Data)
				.enter()
				.append("circle")
				.attr("cx",function(d,i){return scale04X(i) })
				.attr("cy",function(d,i){return scale04Y(d) })
				.attr("r",4)
				.attr("stroke","gold")
				.style("fill","gold")
				.attr("class","point04");

	var line04Data = [];
	for (var i = 0; i <= 4; i++) {
	 				line04Data.push(i);
	 			}; 			
	var line04 = d3.svg.line()
        .x(function(d) { return scale04X(d); })
        .y(function(d) { return scale04Y(-9.8); })
        .interpolate("linear");

 	svg04.append("path")
          .attr("d", line04(line04Data))
          .attr("stroke", "gold")
          .attr("stroke-width", 2)
          .attr("fill", "none");   
  
  /* texts */    
  var text04Data = [
        {"x":-0.5,"y":21.5,"text":"m/s^2"},
        {"x":4.1,"y":-2,"text":"t"},
        {"x":1.5,"y":21,"text":"Acceleration"} ];    
  
  svg04.selectAll(".text04")
      .data(text04Data)
      .enter()
      .append("text")
      .attr("class","text04")
      .attr("x",function(d){return scale04X(d.x)})
      .attr("y",function(d){return scale04Y(d.y)})
      .text(function(d){return d.text})
      .attr("stroke","#fff")
      .attr("font-size","16px")
      .style("fill","white");        

/*
	Impact velocity
*/
var svg05 = d3.select("#svg05")
                .append("svg")
                .attr("height",height)
                .attr("width",width);

/* cliff */
var line05Data = [{"x":0,"y":100},{"x":100,"y":100},
									{"x":100,"y":350},{"x":200,"y":350}];
var line05 = d3.svg.line()
        .x(function(d) { return d.x; })
        .y(function(d) { return d.y; })
        .interpolate("linear");

svg05.append("path")
          .attr("d", line05(line05Data))
          .attr("stroke", "#fff")
          .attr("stroke-width", 3)
          .attr("fill", "none");   

/* curve arrow */
var curve05Data = [{"x":100,"y":70},{"x":120,"y":75},
									{"x":130,"y":85},{"x":135,"y":100},
									{"x":135,"y":200}];
var curve05 = d3.svg.line()
        .x(function(d) { return d.x; })
        .y(function(d) { return d.y; })
        .interpolate("basis");

svg05.append("path")
          .attr("d", curve05(curve05Data))
          .attr("stroke", "#fff")
          .attr("stroke-width", 1)
          .attr("fill", "none");   

/* lines height arrow & person */
var lines05Data =[
	{"x1":50,"y1":100,"x2":50,"y2":350},
	{"x1":50,"y1":100,"x2":45,"y2":105},
	{"x1":50,"y1":100,"x2":55,"y2":105},
	{"x1":50,"y1":350,"x2":45,"y2":345},
	{"x1":50,"y1":350,"x2":55,"y2":345},
	{"x1":80,"y1":55,"x2":80,"y2":70},
	{"x1":80,"y1":70,"x2":70,"y2":100},
	{"x1":80,"y1":70,"x2":90,"y2":100},
	{"x1":80,"y1":60,"x2":60,"y2":70},
	{"x1":80,"y1":60,"x2":100,"y2":70},
	{"x1":135,"y1":200,"x2":130,"y2":195},
	{"x1":135,"y1":200,"x2":140,"y2":195}

];

svg05.selectAll(".hArrow05")
			.data(lines05Data)
			.enter()
			.append("line")
			.attr("class","hArrow05")
  		.attr("x1",function(d){return d.x1})
  		.attr("y1",function(d){return d.y1})
  		.attr("x2",function(d){return d.x2})
  		.attr("y2",function(d){return d.y2})
      .attr("stroke", "#fff")
      .attr("stroke-width", 2);

  /* texts */    
  var text05Data = [
        {"x":10,"y":225,"text":"h(m)"} ];    
  
  svg05.selectAll(".text05")
      .data(text05Data)
      .enter()
      .append("text")
      .attr("class","text05")
      .attr("x",function(d){return d.x})
      .attr("y",function(d){return d.y})
      .text(function(d){return d.text})
      .attr("stroke","#fff")
      .attr("font-size","16px")
      .style("fill","white");        

/* a person & a rock */
  var circle05Data = [
  	{"cx":80,"cy":50,"r":5},
  	{"cx":100,"cy":70,"r":2}
  	];
  svg05.selectAll("circle05")
  		.data(circle05Data)
  		.enter()
  		.append("circle")
     	.attr("cx",function(d){return d.cx;})
     	.attr("cy",function(d){return d.cy;})
     	.attr("r",function(d){return d.r;})
     	.attr("stroke","#fff")
     	.attr("stroke-width",2)
     	.style("fill","none");	


</script>
