---
title: physics
layout: post
postTitle: Optimal angle for a projectile
categories: TwoD-Motion
---

## Optimal angle for a projectile Part1

<div class="row">
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>


--------

## Optimal angle for a projectile Part2
### Hangtime

------

## Optimal angle for a projectile Part3
### Horisontal distance as a function of angle (and speed)

-------

## Optimal angle for a projectile Part4
### Finding the optimal angle and distance with a bit of calculus


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
  function drawVector(svg,x0,y0,angles,length,xScale,yScale,color){

    var vectorData = [];
    var radians = angles * aDegree;
    var radians1 = pi + radians + pi/6;
    var radians2 = pi + radians - pi/6;
    var arrowHead = 10/(xScale(1)-xScale(0));

    // 終点の座標
    endPoint.x = Math.cos(radians)*length+x0;
    endPoint.y = Math.sin(radians)*length+y0;
 

    vectorData.push(new Point(x0,y0));
    vectorData.push(new Point(endPoint.x,endPoint.y));
    vectorData.push(new Point(
      endPoint.x+Math.cos(radians1)*arrowHead,
      endPoint.y+Math.sin(radians1)*arrowHead
      ));
    vectorData.push(new Point(endPoint.x,endPoint.y));
    vectorData.push(new Point(
      endPoint.x+Math.cos(radians2)*arrowHead,
      endPoint.y+Math.sin(radians2)*arrowHead
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

  };


  var x1,y1,x2,y2;

  /* 2点間　ベクトル線　描画関数　*/
  function drawVectorB(svg,x1,y1,x2,y2,xScale,yScale,color){

    var vectorData = [];
    var radians = Math.atan2(y2-y1,x2-x1);
    var radians1 = pi + radians + pi/6;
    var radians2 = pi + radians - pi/6;
    var arrowHead = 10/(xScale(1)-xScale(0)); // length of arrow head

    vectorData.push(new Point(x1,y1));
    vectorData.push(new Point(x2,y2));
    vectorData.push(new Point(
      x2 + Math.cos(radians1)*arrowHead,
      y2 + Math.sin(radians1)*arrowHead
      ));
    vectorData.push(new Point(x2,y2));
    vectorData.push(new Point(
      x2+Math.cos(radians2)*arrowHead,
      y2+Math.sin(radians2)*arrowHead
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
 
  };

  /* 2点間　線　描画関数　*/
  function drawLine(svg,x1,y1,x2,y2,xScale,yScale,color){

    svg.append("line")
          .attr("x1", function(){return xScale(x1)})
          .attr("y1", function(){return yScale(y1)})
          .attr("x2", function(){return xScale(x2)})
          .attr("y2", function(){return yScale(y2)})        
          .attr("stroke", function(){return color})
          .attr("class","line")
          .attr("stroke-width", 2)
          .attr("fill", "none");   
 
  };


  var height = 450;
  var width = 500;
  

/** projectile with ordered set notation */
  var svg12 = d3.select("#svg12")
                .append("svg")
                .attr("height",300)
                .attr("width",750)
                .style("background","black");

  var xScale12 = d3.scale.linear()
                       .domain([-10,350])
                       .range([30,730]);
  
  var yScale12 = d3.scale.linear()
                       .domain([50,0])
                       .range([50,250]);                       

  var xAxis12 = d3.svg.axis()
                  .scale(xScale12)
                  .tickValues([350])
                  .tickPadding(5)
                  .tickFormat(d3.format("d"));

  var xAxis12Group = svg12.append("g")
                      .attr("transform","translate(0,"+ yScale12(0)+")")
                      .attr("stroke","white")
                      .call(xAxis12);   

  var yAxis12 = d3.svg.axis()
                  .scale(yScale12)
                  .orient(["left"])
                  .tickValues([4,30])
                  .tickPadding(0)
                  .tickFormat(d3.format("d"));

  var yAxis12Group = svg12.append("g")
                      .attr("transform","translate(" + xScale12(0) + ",0)")
                      .attr("stroke","white")
                      .call(yAxis12);

  drawVector(svg12,0,4,15,10,xScale12,yScale12,"red");
  drawVector(svg12,100,50,0,10,xScale12,yScale12,"green");
  drawVector(svg12,250,50,-90,10,xScale12,yScale12,"gold");
  drawLine(svg12,350,0,350,30,xScale12,yScale12,"aqua");

  var foData12 = [
    {"x":305,"y":40,"text":"$$fence$$"},
    {"x":80,"y":70,"text":"$$wind \\quad gust $$"},
    {"x":10,"y":25,"text":"$$\\vec{v}$$"},
    {"x":255,"y":60,"text":"$$\\vec{a}$$"}
      ];

  svg12.selectAll(".fo12")
  .data(foData12)
  .enter()
  .append("foreignObject")
  .attr("class","fo12")
  .attr("x",function(d){ return xScale12(d.x) })
  .attr("y",function(d){ return yScale12(d.y) })
  .append("xhtml:body")
  .html(function(d){return d.text;})
  .style("position","fixed")
  .style("font-size",".9em"); 

  d3.select("#run12").on("click",function(){

   // ball12.remove();
   var dt = 0;
    var ball12= svg12.append("circle")
                      .attr("cx",function(){return xScale12(0)})
                      .attr("cy",function(){return yScale12(4)})
                      .attr("r",3)
                      .attr("id","ball12")
                      .attr("stroke","#fff")
                      .style("fill","#fff");
    for (var i = 0; i < 3.5; i=i + 0.05) {
      ball12.transition()
            .delay(function(){
              dt = dt+50*i;
              return dt })
            //.duration(100)
            .attr("cx",function(){return xScale12(109*i)})
            .attr("cy",function(){
              return yScale12(4+60*i-16*i*i)
            })
    };

  });  

</script>
