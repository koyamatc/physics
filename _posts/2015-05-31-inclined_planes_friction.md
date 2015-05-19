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
    角度 \\(\theta\\) の斜面に、ブロックがあります<br>
    ブロックの質量(mass)は \\(m\\)<br>
    このブロックにかかる重力は　\\(\vec{F}_{g}=m\cdot \vec{g}\\)<br>
    ブロックが地面から受ける力を考えるときに、重力に対して垂直ではないので
    重力を２つの力、地面に垂直な力と、地面に水平な力に分けて考えます<br>
    地面に垂直な力\\(\vec{F}_{g\bot}\\)
    $$
    \frac{\lVert\vec{F}_{g\bot}\rVert}{\lVert m\vec{g}\rVert}
    = \cos \theta
    $$
    $$
    \lVert\vec{F}_{g\bot}\rVert
    =\lVert m\vec{g}\rVert\cos \theta
    $$
    地面に平行な力を\\(\vec{F}_{g\lVert}\\)<br>
    $$
    \frac{\lVert\vec{F}_{g\lVert}\rVert}{\lVert m\vec{g}\rVert}
    = \sin \theta
    $$
    $$
    \lVert\vec{F}_{g\lVert}\rVert
    =\lVert m\vec{g}\rVert\sin \theta
    $$

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

    {"x1":370,"y1":00,"x2":370,"y2":30,
      "stroke":"#fff","strokeWidth":"2px"},
    {"x1":370,"y1":30,"x2":400,"y2":30,
      "stroke":"#fff","strokeWidth":"2px"},


  ];

  rectData = [
    {"x":200,"y":130,"height":98,"width":160,
      "stroke":"#fff","strokeWidth":"3px"}
  ];

  vecData01 = [
    {"x1":180,"y1":140,"angles":-90,"length":100,
      "stroke":"#f0f","strokeWidth":"3px"},
    {"x1":180,"y1":140,"angles":206,"length":40,
      "stroke":"#ff0","strokeWidth":"2px"},
    {"x1":180,"y1":140,"angles":-64,"length":90,
      "stroke":"#ff0","strokeWidth":"2px"},
    {"x1":220,"y1":57,"angles":206,"length":40,
      "stroke":"#ff0","strokeWidth":"2px"},
  ];
  textData01 = [
    {"x":230,"y":280,"text":"$$mass=m$$","fontSize":"20px"},
    {"x":150,"y":120,"text":"$$\\vec{F}_{g}$$",
      "fontSize":"20px"},
    {"x":220,"y":150,"text":"$$\\vec{F}_{g\\bot}$$",
      "fontSize":"20px"},
    {"x":150,"y":220,"text":"$$\\vec{F}_{g\\lVert}$$","fontSize":"20px"},
    {"x":50,"y":75,"text":"$$\\theta$$",
      "fontSize":"20px"},
    {"x":340,"y":220,"text":"$$90°-\\theta$$",
      "fontSize":"16px"},
  ];

  drawLine(svg01,lineData01,xScale01,yScale01);
  drawVectorA(svg01,vecData01,xScale01,yScale01);
  drawMathjax(svg01,textData01,xScale01,yScale01)

</script>
