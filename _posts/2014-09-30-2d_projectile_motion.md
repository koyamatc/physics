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
  <div class="col-sm-6">
    <br><br><br><br><br><br><br><br><br><br>
    <h3>
    {% math %}
     \vec{a} + \vec{b} = \vec{c}
    {% endmath %}
    </h3>
  </div>
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
 

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script>

  

  var pi = Math.PI;
  var aDegree = pi/180;
  
  // Point Object
  function Point(x, y){
    this.x = x;
    this.y = y;
    return this;
  };

  var endPoint = new Point();

  var x0 = y0 = 0;
  /* ベクトル線　描画関数　*/
  function drawVector(svg,x0,y0,angles,length,color,name){

    var vectorData = [];
    var radians = angles * aDegree;
    var radians1 = pi + radians + pi/6;
    var radians2 = pi + radians - pi/6;

    // 終点の座標
    endPoint.x = Math.floor(Math.cos(radians)*length)+x0;
    endPoint.y = Math.floor(Math.sin(radians)*length)+y0;

    vectorData.push(new Point(x0,y0));
    vectorData.push(new Point(endPoint.x,endPoint.y));
    vectorData.push(new Point(
      endPoint.x+Math.floor(Math.cos(radians1)*10),
      endPoint.y+Math.floor(Math.sin(radians1)*10)
      ));
    vectorData.push(new Point(endPoint.x,endPoint.y));
    vectorData.push(new Point(
      endPoint.x+Math.floor(Math.cos(radians2)*10),
      endPoint.y+Math.floor(Math.sin(radians2)*10)
      ));

    var vectorArrow = d3.svg.line()
        .x(function(d) { return xScale(d.x); })
        .y(function(d) { return yScale(d.y); })
        .interpolate("linear");

    svg.append("path")
          .attr("d", vectorArrow(vectorData))
          .attr("stroke", function(){return color})
          .attr("class","vector")
          .attr("stroke-width", 2)
          .attr("fill", "none");   
 
    /* texts */  
 //   var delta = Math.abs(angles) <= 90 ? 10 : -10;  
    var delta = 0;
 
    svg.append("text")
      .attr("class","text")
      .attr("x",function(){
        return xScale(Math.floor(Math.cos(radians)*length/2)+x0)
      })
      .attr("y",function(d){
        return yScale(Math.floor(Math.sin(radians)*length/2)+y0)
      })
      .text(name)
      .attr("stroke","#fff")
      .attr("font-size","16px")
      .style("fill","white");   

   svg.append("text")
      .attr("class","text")
      .attr("x",function(){
        return xScale(Math.floor(Math.cos(radians)*length/2)+x0-3)
      })
      .attr("y",function(d){
        return yScale(Math.floor(Math.sin(radians)*length/2)+y0+10)
      })
      .text("→")
      .attr("stroke","#fff")
      .attr("font-size","16px")
      .style("fill","white");   


  };

  var height = 500;
  var width = 500;
  
  var xScale = d3.scale.linear()
                       .domain([-200,200])
                       .range([50,450]);
  
  var yScale = d3.scale.linear()
                       .domain([200,-200])
                       .range([50,450]);                       

/**
  2-dimentional vectors
*/

var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",height)
                .attr("width",width);

  svg01
  .append("foreignObject")
  .attr("class","fo")
  .attr("height",200)
  .attr("width",200)
  .attr("x",0)
  .attr("y",200)
  .text("$$ \\frac{1}{2} \\centerdot \\Delta (\\vec{a})^2$$") 
  ;   

  // left right              
  drawVector(svg01,-150,150,180,50,"gold","a");
  drawVector(svg01,-140,150,0,50,"gold","b");               
  // up down
  drawVector(svg01,100,160,90,50,"gold","a");
  drawVector(svg01,100,150,-90,50,"gold","b");  

  drawVector(svg01,-150,-100,30,150,"red","a");
  drawVector(svg01,endPoint.x,endPoint.y,-10,100,"lime","b");  
  drawVector(svg01,-150,-100,14,235,"gold","c");


  var textData = [
    {"x":-150,"y":190,"text":"one dimention vectors"},
    {"x":-150,"y":0,"text":"two dimentions vectors"}
  ];

  svg01.selectAll(".msg")
       .data(textData)
       .enter()
       .append("text")
       .attr("class","msg")
       .attr("x",function(d){ return xScale(d.x) })
       .attr("y",function(d){ return yScale(d.y) })
      .text(function(d){return d.text })
      .attr("stroke","#fff")
      .attr("font-size","18px")
      .style("fill","white"); 


</script>
