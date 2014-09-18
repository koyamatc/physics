---
title: physics
layout: post
postTitle: Tow-dimentional projectile motion
categories: TwoD-Motion
---

### Visualizing vectors in 2 dimentions

<div class="row">
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6"></div>
</div>

### Projectile an angle

### Different way to determine time in air

### Launching and landing on different elevations

### Total displacement for projectile

### Total final velocity for projectile

### Correction to  total final velocity for projectile

### Projectile on an incline

### Unit vectors and engineering notation

### Unit vector notation

### Unit vector notation(part 2)

### Projectile motion with ordered set notation  
 

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script>
  var pi = Math.PI;
  var aDegree = pi/180;

  function drawVector(svg,x,y,degrees,length,color,name){
    var vectorData = [];
    var radians = degrees * aDegree;
    var radians1 = pi + radians + pi/6;
    var radians2 = pi + radians - pi/6;

    vectorData.push([x,y]);
    vectorData.push([Math.cos(radians)*length+x,Math.sin(radians)*length+y]);
    vectorData.push([vectorData[1][0]+Math.cos(radians1)*10,
                     vectorData[1][1]+Math.sin(radians1)*10]);
    vectorData.push([Math.cos(radians)*length+x,Math.sin(radians)*length+y]);
    vectorData.push([vectorData[3][0]+Math.cos(radians2)*10,
                     vectorData[3][1]+Math.sin(radians2)*10]);

    var vectorArrow = d3.svg.line()
        .x(function(d) { return (d[0]); })
        .y(function(d) { return (d[1]); })
        .interpolate("linear");

    svg.append("path")
          .attr("d", vectorArrow(vectorData))
          .attr("stroke", function(){return color})
          .attr("stroke-width", 2)
          .attr("fill", "none");   
  
  };

  var height = 400;
  var width = 400;

/**
  2-dimentional vectors
*/

var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",height)
                .attr("width",width);

 drawVector(svg01,100,300,-45,100,"red","a");               


</script>
