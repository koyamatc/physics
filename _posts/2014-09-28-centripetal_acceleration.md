---
title: physics
layout: post
postTitle: Centripetal acceleration
categories: TwoD-Motion
---

## Race cars with constant acceleration around curve

<div class="row">
  <div class="col-sm-7">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-5">
  </div>
</div>

--------

## Centripetal force and acceleratio intuition

<div class="row">
  <div class="col-sm-7">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-5">
  </div>
</div>

--------

## Visual understanding of centripetal acceleration formula

<div class="row">
  <div class="col-sm-7">
    <div id="svg03"></div>
  </div>
  <div class="col-sm-5">
  </div>
</div>

--------

## Optimal turns at Indianapolis Motor Speedway with JR Hildebrand

--------

## Calculus proof of centripetal acceleration formula

--------

## Loop de loop question

--------

## Loop de loop answer Part 1

--------

## Loop de loop answer Part 2


<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>

<script>

  var height = 450;
  var width = 500;
  

/**  */
  var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",400)
                .attr("width",400)
                .style("background","green");

  var xScale01 = d3.scale.linear()
                       .domain([0,300])
                       .range([50,350]);
  
  var yScale01 = d3.scale.linear()
                       .domain([300,0])
                       .range([50,350]);                       

 
  var px,py;

  // Speedway
  drawArc(svg01,0,90,200,350,5,"#ccc","#ccc",xScale01,yScale01);
  drawArc(svg01,0,90,350,350,5,"brown","brown",xScale01,yScale01);
  drawArc(svg01,0,90,200,200,5,"brown","brown",xScale01,yScale01);
  drawArc(svg01,0,90,298,300,3,"blue","blue",xScale01,yScale01);

  // x axis
  drawVector(svg01,300*Math.cos(90*aDegree),300*Math.sin(90*aDegree),-0,100,xScale01,yScale01,"#00f");
  drawVector(svg01,300*Math.cos(70*aDegree),300*Math.sin(70*aDegree),-20,100,xScale01,yScale01,"#00f");
  drawVector(svg01,300*Math.cos(60*aDegree),300*Math.sin(60*aDegree),-30,100,xScale01,yScale01,"#00f");
  drawVector(svg01,300*Math.cos(45*aDegree),300*Math.sin(45*aDegree),-45,100,xScale01,yScale01,"#00f");

/**
  var foData01 = [
    {"x":6,"y":15,"text":"$$\\textcolor(red) \\vec{s}$$"},
    {"x":2,"y":7.7,"text":"$$\\theta$$"},
    {"x":40,"y":5,"text":"$$d$$"}
      ];

  drawText(svg01,foData01,"1.5em",xScale01,yScale01);
*/

/**  */
  var svg02 = d3.select("#svg02")
                .append("svg")
                .attr("height",400)
                .attr("width",600)
                .style("background","#000");

  var xScale02 = d3.scale.linear()
                       .domain([0,500])
                       .range([50,550]);
  
  var yScale02 = d3.scale.linear()
                       .domain([300,0])
                       .range([50,350]);                       

    drawVector(svg02,0,150,60,80,xScale02,yScale02,"#f00");
    drawVector(svg02,endPoint.x,endPoint.y,30,80,xScale02,yScale02,"#ff0");
    drawVector(svg02,endPoint.x,endPoint.y,0,80,xScale02,yScale02,"#0f0");
    drawVector(svg02,endPoint.x,endPoint.y,-30,80,xScale02,yScale02,"#0ff");
    drawVector(svg02,endPoint.x,endPoint.y,-60,80,xScale02,yScale02,"#fff");

    drawVector(svg02,400,150,60,80,xScale02,yScale02,"#f00");
    drawVector(svg02,400,150,30,80,xScale02,yScale02,"#ff0");
    drawVector(svg02,400,150,0,80,xScale02,yScale02,"#0f0");
    drawVector(svg02,400,150,-30,80,xScale02,yScale02,"#0ff");
    drawVector(svg02,400,150,-60,80,xScale02,yScale02,"#fff");

/** Visual understanding .... */
  var svg03 = d3.select("#svg03")
                .append("svg")
                .attr("height",400)
                .attr("width",600)
                .style("background","#000");

  var xScale03 = d3.scale.linear()
                       .domain([0,500])
                       .range([50,550]);
  
  var yScale03 = d3.scale.linear()
                       .domain([300,0])
                       .range([50,350]);

  var circleData03 = [
    {"cx":120,"cy":150,"r":100,"stroke":"#666","StrokeWidth":2,"fillColor":"none"},
    {"cx":120,"cy":150,"r":3,"stroke":"#666","StrokeWidth":2,"fillColor":"#666"},

    {"cx":350,"cy":150,"r":80,"stroke":"#666","StrokeWidth":2,"fillColor":"none"},
    {"cx":350,"cy":150,"r":3,"stroke":"#666","StrokeWidth":2,"fillColor":"#666"}

  ];   

  drawCircle(svg03,circleData03,xScale03,yScale03);                                            

</script>
