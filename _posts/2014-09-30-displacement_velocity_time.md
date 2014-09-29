---
title: physics
layout: post
postTitle: Displacement,velocity and time 
categories: OneD-Motion
---

### Vectors and Scalars
 
+ Vectors
  - magnitude/size and direction
  - displacement  -- 5 meters to the right
  - velocity -- 5/2 m/s to the right
  - displacement = velocity * time

+ Scalars
  - magnitude/size
  - distance -- 5 meters
  - speed -- 5/2 m/s 
  - distance = speed * time

<div class="panel">
  ベクトルには移動する方向がある！
</div>

----

 <h4>A brick moves 5 meters in 2 seconds.</h4> 
 <div id="svg"></div>

----

### Calculating average velocity or speed

If Jun was able to travel 5km north in 1 hour in his car, 
what was his velocity?

_Average velocity_
{% math %}
\vec{v}=\frac{\vec{s}}{\Delta t} 
\qquad
\vec{v}:velocity \quad
\vec{s}:displacement \quad
\Delta t:change \quad in \quad time
{% endmath %}
{% math %}
\vec{v}=\frac{5km}{1 hour} \quad north 
{% endmath %}  

--------

_Average speed or rate_
{% math %}
r=\frac{d}{\Delta t}
\qquad
r:rate \quad or \quad speed  \quad
d:distance \quad
\Delta t:change \quad in \quad time
{% endmath %}
$$r=\frac{5km}{1 hour}$$
$$\quad=\frac{5km}{1 hour}*\frac{1000}{1}*\frac{m}{km}$$
$$\quad=5000*\frac{m}{hour}$$
$$\quad=5000*\frac{m}{hour}*\frac{1}{3600}*\frac{hour}{seconds}$$
$$\quad=1.39\frac{m}{s}$$

秒速1.39m(1秒間に1.39m進む)

------

### Solving for time

Jun is running at a constant velocity of 3m/s to the east.

How long will it take him to travel 720 meters?

r: rate or speed, d: distance, t: time 
$$r=\frac{d}{t} \rightarrow t=\frac{d}{r}$$
$$t=\frac{720m}{3m/s}=240seconds$$

--*--*--*--*--*--*--*--*--*--*--*--*--*--*--*

$$\vec{v}:velocity \quad \vec{s}:displacement \quad t:time$$
$$\vec{v}=\frac{\vec{s}}{t} \rightarrow t=\frac{\vec{s}}{\vec{v}}$$
$$t=\frac{720m \quad east}{3m/s}=240seconds \quad east$$


------

### displacement from time and velocity

If Jun travels for 1 minute at 5 m/s to the south, 

how much will he be displaced?

$$\vec{v}:velocity=5 m/s$$
$$\vec{s}:displacement$$
$$t:time=1minute$$
$$\vec{v}=\frac{\vec{s}}{t} \rightarrow \vec{s}= \vec{v}*t$$
$$\vec{s}= \vec{v}*t = 5\frac{m}{s}*1minute
=5\frac{m}{s}*1minute*\frac{60}{1}*\frac{s}{minute}
=300m \quad to \quad the \quad south$$

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script>

  var height = 200;
  var width = 400;

  var svg = d3.select("#svg").append("svg")
                .attr("height",height)
                .attr("width",width);

  /* ground line */
  svg.append("line")
      .attr("x1",50)
      .attr("y1",180)
      .attr("x2",350)
      .attr("y2",180)
      .attr("stroke","lime")
      .attr("stroke-width",3);

  /* bricks */    
  var rectData = [{"x":80,"y":115,"height":60,"width":80},
                  {"x":240,"y":115,"height":60,"width":80} ]    
  
  svg.selectAll("rect")
      .data(rectData)
      .enter()
      .append("rect")
      .attr("x",function(d){return d.x})
      .attr("y",function(d){return d.y})
      .attr("height",function(d){return d.height})
      .attr("width",function(d){return d.width})
      .style("fill","orange");

  /* arrow */
  var arrowData = [{"x1":170,"y1":145,"x2":230,"y2":145},
                   {"x1":230,"y1":145,"x2":220,"y2":140},
                   {"x1":230,"y1":145,"x2":220,"y2":150} ]  
  svg.selectAll(".arrow")
      .data(arrowData)
      .enter()
      .append("line")
      .attr("x1",function(d){return d.x1})
      .attr("y1",function(d){return d.y1})
      .attr("x2",function(d){return d.x2})
      .attr("y2",function(d){return d.y2})
      .attr("class","arrow")
      .attr("stroke","#fff")
      .attr("stroke-width",2);

/* distance */
  var distData = [{"x1":120,"y1":195,"x2":270,"y2":195},
                   {"x1":120,"y1":193,"x2":120,"y2":198},
                   {"x1":270,"y1":193,"x2":270,"y2":198} ]  
  svg.selectAll(".dist")
      .data(distData)
      .enter()
      .append("line")
      .attr("x1",function(d){return d.x1})
      .attr("y1",function(d){return d.y1})
      .attr("x2",function(d){return d.x2})
      .attr("y2",function(d){return d.y2})
      .attr("class","dist")
      .attr("stroke","#fff")
      .attr("stroke-width",2);

  /* texts */    
  var textData = [{"x":190,"y":195,"text":"5m"} ]    
  
  svg.selectAll("text")
      .data(textData)
      .enter()
      .append("text")
      .attr("x",function(d){return d.x})
      .attr("y",function(d){return d.y})
      .text(function(d){return d.text})
      .attr("stroke","#fff")
      .attr("font-size","16px")
      .style("fill","white");        
;

</script>
