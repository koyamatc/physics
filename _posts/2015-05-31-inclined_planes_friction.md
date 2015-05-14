---
title: physics
layout: post
date: 2015-05-31 21:00:00
postTitle: Inclined planes and friction 
categories: newton-laws-motion
---

## Inclined plane force components 
<br>
<h3>
<div class="row">
  <div class="col-sm-6">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6">
  </div>
</div>
  
</h3>

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>

<script>

  var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",500)
                .attr("width",500)
                .style("background","#000");
  var svg02 = d3.select("#svg02")
                .append("svg")
                .attr("height",300)
                .attr("width",500)
                .style("background","#000");
  var xScale01 = d3.scale.linear()
                       .domain([0,400])
                       .range([50,450]);              
  var yScale01 = d3.scale.linear()
                       .domain([400,0])
                       .range([50,450]);              
  
  lineData01 = [
    {"x1":0,"y1":0,"x2":400,"y2":0,
      "stroke":"brown","strokeWidth":"4px"},
    {"x1":0,"y1":0,"x2":400,"y2":200,
      "stroke":"brown","strokeWidth":"4px"},
    {"x1":400,"y1":200,"x2":400,"y2":0,
      "stroke":"brown","strokeWidth":"4px"},
    
    {"x1":150,"y1":75,"x2":250,"y2":125,
      "stroke":"#fff","strokeWidth":"2px"},
    {"x1":150,"y1":75,"x2":150-40,"y2":75+80,
      "stroke":"#fff","strokeWidth":"2px"},
    {"x1":250,"y1":125,"x2":250-40,"y2":125+80,
      "stroke":"#fff","strokeWidth":"2px"},
    {"x1":150-40,"y1":75+80,"x2":250-40,"y2":125+80,
      "stroke":"#fff","strokeWidth":"2px"},
  ];

  rectData = [
    {"x":200,"y":130,"height":98,"width":160,
      "stroke":"#fff","strokeWidth":"3px"}
  ];

  vecData01 = [
    {"x1":180,"y1":140,"angles":-90,"length":100,
      "stroke":"#f0f","strokeWidth":"3px"}
  ];
  vecData02 = [
    {"x1":250,"y1":150,"angles":90,"length":100,
      "stroke":"#f0f","strokeWidth":"3px"},
    {"x1":250,"y1":150,"angles":-90,"length":100,
      "stroke":"#0f0","strokeWidth":"3px"},
    {"x1":250,"y1":150,"angles":0,"length":200,
      "stroke":"#fff","strokeWidth":"3px"}
  ];
  textData01 = [
    {"x":255,"y":50,"text":"49N","stroke":"#fff","fontSize":"20px"},
    {"x":255,"y":255,"text":"49N","stroke":"#fff","fontSize":"20px"},
  ];
  textData02 = [
    {"x":255,"y":50,"text":"49N","stroke":"#fff","fontSize":"20px"},
    {"x":255,"y":255,"text":"49N","stroke":"#fff","fontSize":"20px"},
    {"x":400,"y":130,"text":"5m/s","stroke":"#fff","fontSize":"20px"},
  ];

  drawLine(svg01,lineData01,xScale01,yScale01);
  drawVectorA(svg01,vecData01,xScale01,yScale01);
 

</script>
