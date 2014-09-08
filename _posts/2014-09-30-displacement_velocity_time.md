---
title: physics
layout: post
postTitle: Displacement,velocity and time 
categories: OneD-Motion
---

### Vectors and Scalars
 
+ Vectors
  - magnitude/size and direction
  - displacement  -- 5 meters to the left
  - velocity -- 5/2 m/s to the left

+ Scalars
  - magnitude/size
  - distance -- 5 meters
  - speed -- 5/2 m/s 


----

 <h3>A brick moves 5 meters in 2 seconds.</h3> 
 <div id="svg"></div>

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
