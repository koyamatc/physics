---
title: physics
layout: post
postTitle: Acceleration 
categories: OneD-Motion
---

### Acceleration

Acceleration: Change in velocity over time.

<div class="panel">
A car start to move to the east.<br>
Its velocity will be 90kmph in 3 seconds.<br>
How much is the acceleration?
</div>

$$\vec{a}:acceleration$$
$$\vec{v}:velocity=(90-0)kmph$$
$$t:time=3seconds$$

$$\vec{a}=\frac{\vec{v}}{t}=\frac{(90-0)kmph}{3sec}
=\frac{30kmph}{sec}$$

※Velocity increases 30kmph every second.

$$\vec{a}=\frac{30kmph}{sec}=\frac{30\frac{km}{hour}}{sec}
=30\frac{km}{hour*sec}*\frac{1}{3600}*\frac{hour}{sec}
=\frac{1}{120}\frac{km}{sec^2}$$
$$\quad=\frac{1}{120}\frac{km}{sec^2}*\frac{1000}{1}*\frac{meters}{km}=8.33\frac{m}{sec^2}
=\frac{8.33\frac{m}{sec}}{sec}$$

※Velocity increases 8.33mps every second.

<div id="svg01"></div>

-------

### Airbus A380 take-off time

$$take \quad off \quad velocity=280 km/hour$$
$$acceleration=1.0\frac{m/s}{s}=1.0\frac{m}{s^2}$$ 

<div class="panel">
  How long take off last?
</div>

$$\vec{v} = 280\frac{km}{hour} 
= 280\frac{km}{hour}*\frac{1000}{1}*\frac{m}{km}*\frac{1}{3600}*\frac{hour}{s}
=78\frac{m}{s}$$

$$\vec{a}=\frac{\Delta\vec{v}}{\Delta t} \rightarrow 
\Delta t =\frac{\Delta\vec{v}}{\vec{a}}$$
$$\Delta t = \frac{78\frac{m}{s}}{1.0\frac{m}{s^2}}=78s$$

-------

### Airbus A380 take-off distance

<div class="panel">
  How long is a runway needed to take off?
</div>

$$velocity:\vec{v}=78\frac{m}{s}$$
$$acceleration\vec{a}=1.0\frac{m}{s^2}$$ 

if acceleratin is constant,
$$Average \quad velocity 
= \frac{final \quad velocity + initial \quad velocity}{2}$$
$$\vec{v_{a}}=\frac{(78-0)\frac{m}{s}}{2}
=39\frac{m}{s}$$

$$\vec{v}=\frac{\vec{s}}{\Delta t}\rightarrow
\vec{s}=\vec{v}*\Delta t$$
$$\vec{s}=39\frac{m}{s}*78s=3042m$$

--------

### Why distance is area under velocity-time line
 
<div class="panel">
  $$velocity:\vec{v}=5\frac{m}{s}\quad right \quad constant$$
  $$time:t=5seconds$$
</div>
$$\vec{v}=\frac{\vec{s}}{t}\rightarrow
\vec{s}=\vec{v}*t=5\frac{m}{s}*5s=25m$$
<div id="svg02"></div>

<div class="panel">
  $$acceleration:\vec{a}=1\frac{m}{s^2} \quad constant$$
  $$initial\quad velocity:\vec{v_{i}}=0$$
  $$time:t=5seconds$$
</div>
Velocity increases 1m/s every second.

$$\vec{s}= \frac{1}{2}*t*\vec{v}
=\frac{1}{2}*5s*5\frac{m}{s}=12.5m$$

<div id="svg03"></div>

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script>
  
  var pi = Math.PI;
  var height = 400;
  var width = 400;

  var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",height)
                .attr("width",width);

  var arcs = [
    {"innerRadius":120,"outerRadius":180,"start":-90,"end":90,"c":"blue"},
    {"innerRadius":80,"outerRadius":115,"start":-90,"end":-45,"c":"yellow"},
    {"innerRadius":80,"outerRadius":115,"start":-45,"end":0,"c":"brown"},
    {"innerRadius":80,"outerRadius":115,"start":0,"end":45,"c":"red"}   ]

  var arc = d3.svg.arc()
      .innerRadius(function(d){return d.innerRadius})
      .outerRadius(function(d) {return d.outerRadius})
      .startAngle(function(d){return d.start * (pi/180);}) //converting from degs to radians
      .endAngle(function(d) { return d.end * (pi/180);});                               

 svg01.selectAll("path")
    .data(arcs)
    .enter()
    .append("path")
    .attr("d", arc)
    .attr("transform", "translate(200,300)")
    .attr("id",function(d,i){return "spd"+i;})
    .attr("stroke",function(d){return d.c;})
    .attr("stroke-width", 2)
    .attr("fill",function(d,i){return d.c;});


  /* texts */    
  var textData = [
        {"x":160,"y":330,"text":"Speed Meter"},
        {"x":180,"y":270,"text":"kmph"} ];    
  
  svg01.selectAll("text")
      .data(textData)
      .enter()
      .append("text")
      .attr("x",function(d){return d.x})
      .attr("y",function(d){return d.y})
      .text(function(d){return d.text})
      .attr("stroke","#fff")
      .attr("font-size","16px")
      .style("fill","white");        

  /* speeds */
  var step = pi/12;    
  var speeds = [0,1,2,3,4,5,6,7,8,9,10,11,12];    
  
  svg01.selectAll(".speed")
      .data(speeds)
      .enter()
      .append("text")
      .attr("class","speed")
      .attr("transform", "translate(200,300)")
      .attr("x",function(d,i){
        var x1= -Math.cos(d*step)*150;
        return d>9?(x1-10):x1; })
      .attr("y",function(d,i){return -Math.sin(d*step)*150;})
      .text(function(d){return d*10})
      .attr("stroke","#red")
      .attr("font-size","16px")
      .style("fill","gold");        

/**
*/

var curve02Data = [];
for (var i = 0; i <= 5; i++) {
  curve02Data.push(i);
};
var svg02 = d3.select("#svg02")
                .append("svg")
                .attr("height",height)
                .attr("width",width);

/* 軸 */
var scale02X = d3.scale.linear()
                .domain([0,7])
                .range([50,350]);
var scale02Y = d3.scale.linear()
                .domain([0,7])
                .range([350,0]);

var xAxis02 = d3.svg.axis()
                  .scale(scale02X)
                  .tickValues([0, 1, 2, 3, 4, 5, 6])
                  .tickPadding(5)
                  .tickFormat(d3.format("d"));

var xAxis02Group = svg02.append("g")
                      .attr("transform","translate(0,"+ scale02Y(0)+")")
                      .attr("stroke","white")
                      .call(xAxis02);   

var yAxis02 = d3.svg.axis()
                  .scale(scale02Y)
                  .orient(["left"])
                  .tickPadding(0)
                  .tickValues([0, 1, 2, 3, 4, 5, 6]);

var yAxis02Group = svg02.append("g")
.attr("transform","translate(" + scale02X(0) + ",0)")
                      .attr("stroke","white")
                      .call(yAxis02);                                              
var area02 = d3.svg.area()
        .x(function(d,i) { return scale02X(d);})
        .y0(function(d,i) { return scale02Y(0);})
        .y1(function(d,i) { return scale02Y(5);});
    svg02.append("path")
        .attr("d", area02(curve02Data))
        .attr("fill", "blue");

  /* texts */    
  var text02Data = [
        {"x":-0.5,"y":6.5,"text":"V(m/s)"},
        {"x":6.7,"y":-0.5,"text":"t(sec)"},
        {"x":1.5,"y":3,"text":"displacement"} ];    
  
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

/**
*/

var curve03Data = [];
for (var i = 0; i <= 5; i++) {
  curve03Data.push(i);
};
var svg03 = d3.select("#svg03")
                .append("svg")
                .attr("height",height)
                .attr("width",width);

/* 軸 */
var scale03X = d3.scale.linear()
                .domain([0,7])
                .range([50,350]);
var scale03Y = d3.scale.linear()
                .domain([0,7])
                .range([350,0]);

var xAxis03 = d3.svg.axis()
                  .scale(scale03X)
                  .tickValues([0, 1, 2, 3, 4, 5, 6])
                  .tickPadding(5)
                  .tickFormat(d3.format("d"));

var xAxis03Group = svg03.append("g")
                      .attr("transform","translate(0,"+ scale03Y(0)+")")
                      .attr("stroke","white")
                      .call(xAxis03);   

var yAxis03 = d3.svg.axis()
                  .scale(scale03Y)
                  .orient(["left"])
                  .tickPadding(0)
                  .tickValues([0, 1, 2, 3, 4, 5, 6]);

var yAxis03Group = svg03.append("g")
.attr("transform","translate(" + scale03X(0) + ",0)")
                      .attr("stroke","white")
                      .call(yAxis03);                                              
var area03 = d3.svg.area()
        .x(function(d,i) { return scale03X(d);})
        .y0(function(d,i) { return scale03Y(0);})
        .y1(function(d,i) { return scale03Y(d);});
    svg03.append("path")
        .attr("d", area03(curve03Data))
        .attr("fill", "blue");

  /* texts */    
  var text03Data = [
        {"x":-0.5,"y":6.5,"text":"V(m/s)"},
        {"x":6.7,"y":-0.5,"text":"t(sec)"},
        {"x":2,"y":1,"text":"displacement"},
        {"x":6.5,"y":6,"text":"v=a*t"} ];    
  
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

  svg03.append("line")
    .attr("x1",function(){return scale03X(0);})
    .attr("y1",function(){return scale03Y(0);})
    .attr("x2",function(){return scale03X(6);})
    .attr("y2",function(){return scale03Y(6);})
    .attr("stroke","#fff");
  svg03.append("line")
    .attr("x1",function(){return scale03X(0);})
    .attr("y1",function(){return scale03Y(5);})
    .attr("x2",function(){return scale03X(5);})
    .attr("y2",function(){return scale03Y(5);})
    .attr("stroke","#fff");


</script>
