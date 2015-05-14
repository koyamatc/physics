---
title: physics
layout: post
date: 2015-05-31 22:00:00
postTitle: Normal force and contact force 
categories: newton-laws-motion
---

<br>
<h3>
<div class="row">
  <div class="col-sm-6">
    静止
    <div id="svg01"></div>
  </div>
  <div class="col-sm-6">
    等速度運動
    <div id="svg02"></div>
  </div>
</div>
  
  + ２つのブロックは地球上においてともに\\(5kg\\)

  + 右のブロックは等速度\\(5m/s\\)で移動している（摩擦や抵抗は無視する）

    左のブロックは、静止している。等速度\\(0m/s\\)で動いてるといえる

  + 地球表面近くで、地球がブロックを引く力（重量加速度）は
    \\(\,\vec{g}=9.8m/s^2 \\)なので

    ピンクの力は\\(\,\vec{F}=9.8m/s^2\cdot 5kg=49N\\)

  + ニュートンの第３法則の通り、ピンクの力と同じ大きさで反対方向の力（緑色の力）が発生する
  
    接触面に垂直な力、これを垂直効力（normal force） という

    \\(\vec{F_{N}}=49N\\)

    また、ブロックの面と、地表面が接触したときに働く力であることから、接触力(contact force)ともいう

------

## Normal force in an elevator

$$重力加速度は\,\vec{g}=-9.8m/s^2$$
$$人の質量は、地表面近くで\,10kg$$
$$\vec{F_{g}}=-98N \jmath（垂直方向の移動）$$

<div class="row">
  <div class="col-sm-3">
    静止している
    <div id="svg031"></div>
    $$\vec{V}=0m/s$$
    $$\vec{a}=0m/s^2$$
    $$\vec{F_{N}}=98N \cdot \jmath$$
  </div>
  <div class="col-sm-3">
    加速して上昇
    <div id="svg032"></div>
    $$$$
    $$\vec{a}=2m/s^2 \cdot \jmath$$
    $$\vec{F_{net}}=10kg*2m/s^2 \cdot \jmath$$
    $$\vec{F_{N}}=118N \cdot \jmath$$
  </div>
  <div class="col-sm-3">
    等速で下降する
    <div id="svg033"></div>
    $$\vec{V}=-2m/s^2 \cdot \jmath$$
    $$\vec{a}=0m/s^2$$
    $$\vec{F_{N}}=98N \cdot \jmath$$
  </div>
  <div class="col-sm-3">
    加速して下降している
    <div id="svg034"></div>
    $$$$
    $$\vec{a}=-2m/s^2 \cdot \jmath$$
    $$\vec{F_{net}}=10kg*(-2m/s^2) \cdot \jmath$$
    $$\vec{F_{N}}=78N \cdot \jmath$$

  </div>
</div>
</h3>

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_SVG"></script>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="{{site.url}}/js/d3draws.js" charset="utf-8"></script>

<script>

  var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",300)
                .attr("width",500)
                .style("background","#000");
  var svg02 = d3.select("#svg02")
                .append("svg")
                .attr("height",300)
                .attr("width",500)
                .style("background","#000");
  var svg031 = d3.select("#svg031")
                .append("svg")
                .attr("height",300)
                .attr("width",200)
                .style("background","#000");
  var svg032 = d3.select("#svg032")
                .append("svg")
                .attr("height",300)
                .attr("width",200)
                .style("background","#000");
  var svg033 = d3.select("#svg033")
                .append("svg")
                .attr("height",300)
                .attr("width",200)
                .style("background","#000");
  var svg034 = d3.select("#svg034")
                .append("svg")
                .attr("height",300)
                .attr("width",200)
                .style("background","#000");
  
  lineData = [
    {"x1":50,"y1":200,"x2":450,"y2":200,
      "stroke":"#fff","strokeWidth":"4px"}
  ];

  rectData = [
    {"x":170,"y":100,"height":98,"width":160,
      "stroke":"#fff","strokeWidth":"3px"}
  ];

  vecData01 = [
    {"x1":250,"y1":150,"angles":90,"length":100,
      "stroke":"#f0f","strokeWidth":"3px"},
    {"x1":250,"y1":150,"angles":-90,"length":100,
      "stroke":"#0f0","strokeWidth":"3px"}
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

  drawLine(svg01,lineData);
  drawLine(svg02,lineData);
  drawRect(svg01,rectData);
  drawRect(svg02,rectData);
  drawVectorA(svg01,vecData01);
  drawVectorA(svg02,vecData02);
  drawText(svg01,textData01);
  drawText(svg02,textData02);

////
  rectData03 = [
    {"x":40,"y":100,"height":150,"width":120,
      "stroke":"#fff","strokeWidth":"3px"}
  ];
  lineData03 = [
    {"x1":100,"y1":20,"x2":100,"y2":98,
      "stroke":"#f0f","strokeWidth":"3px"},
    {"x1":100,"y1":160,"x2":100,"y2":210,
      "stroke":"#fff","strokeWidth":"3px"},
    {"x1":80,"y1":180,"x2":120,"y2":180,
      "stroke":"#fff","strokeWidth":"3px"},
    {"x1":80,"y1":250,"x2":100,"y2":210,
      "stroke":"#fff","strokeWidth":"3px"},
    {"x1":120,"y1":250,"x2":100,"y2":210,
      "stroke":"#fff","strokeWidth":"3px"},
  ];

  circleData03 = [
    {"cx":100,"cy":150,"r":10,
      "stroke":"#fff","strokeWidth":"3px","fillColor":"none"},
  ];
  
  drawRect(svg031,rectData03);
  drawRect(svg032,rectData03);
  drawRect(svg033,rectData03);
  drawRect(svg034,rectData03);

  drawLine(svg031,lineData03);
  drawLine(svg032,lineData03);
  drawLine(svg033,lineData03);
  drawLine(svg034,lineData03);

  drawCircle(svg031,circleData03);
  drawCircle(svg032,circleData03);
  drawCircle(svg033,circleData03);
  drawCircle(svg034,circleData03);

</script>
