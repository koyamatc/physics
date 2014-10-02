---
title: physics
layout: post
postTitle: Optimal angle for a projectile
categories: TwoD-Motion
---

## Optimal angle for a projectile Part1

<div class="row">
  <div class="col-sm-7">
    <div id="svg01"></div>
  </div>
  <div class="col-sm-5">
  a projectile
  $$s:speed\quad magnitude \quad of \quad \vec{s}$$
  $$\theta:angle\quad of\quad direction$$
  $$d:distance(landing \quad point)$$
  </div>
</div>

<div class="row">
  <div class="col-sm-5">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-7">
    vertical speed
    $$sin\theta=\frac{s_{v}}{s} \rightarrow s_{v}=s \cdot sin\theta$$
    horisontal speed
    $$cos\theta=\frac{s_{h}}{s} \rightarrow s_{h}=s \cdot cos\theta$$
  </div>
</div>


--------

## Optimal angle for a projectile Part2
### Hangtime

<div class="row">
  <div class="col-sm-5">
    <div id="svg03"></div>
  </div>
  <div class="col-sm-7">
    <h3 class="text-gold">
      How long is this object going to be in the air?
    </h3>
    $$Gravity \quad slows \quad it \quad down \quad at \quad 10m/s^2.$$
    $$g=\vec{a}=-10m/s^2$$
    $$\vec{s}_{v}=10m/s \rightarrow 0m/s \quad by \vec{a}:1second$$ 
    $$\vec{s}_{v}=20m/s \rightarrow 0m/s \quad by \vec{a}:2seconds$$
    $$time \quad downward
    =\frac{\vec{s}_{v}}{g}
    =\frac{20m/s}{10m/s^2}=2s$$
    $$time \quad upward=time \quad downward$$
    total time in the air
    $$t_{a}=\frac{\vec{s}_{v}}{g} \times 2 
    = \frac{2 \cdot s \cdot sin\theta}{g}$$
  </div>
</div>

------

## Optimal angle for a projectile Part3
### Horisontal distance as a function of angle (and speed)

Horisontal distance
$$d = rate \cdot time$$

$$d=r \cdot t$$
$$d=s_{h} \cdot t
=s\cdot cos\theta \cdot \frac{2\cdot s \cdot sin\theta}{g}$$

a function of angle
$$d(\theta)=\frac{2s^2}{g}cos\theta sin\theta 
\quad (0 \ge \theta \ge 90)$$

-------

## Optimal angle for a projectile Part4
### Finding the optimal angle and distance with a bit of calculus

<div class="row">
  <div class="col-sm-5">
    <div id="svg04"></div>
  </div>
  <div class="col-sm-7">
  $$d(\theta)=\frac{2s^2}{g}cos\theta sin\theta 
  \quad (0 \ge \theta \ge 90)$$
  $$d(\theta)の導関数d'(\theta)を求めます$$
  $$d'(\theta)=\frac{2s^2}{g}(-sin^2\theta+cos^2\theta)$$
  $$導関数d'(\theta)が表すd(\theta)の接線の傾きが0のとき、d(\theta)の値は最大となります$$
  $$\frac{2s^2}{g}(-sin^2\theta+cos^2\theta)=0$$
  $$s=0のときは考えません$$
  $$-sin^2\theta+cos^2\theta=0$$
  $$cos^2\theta=sin^2\theta$$
  $$\frac{cos^2\theta}{cos^2\theta}=\frac{sin^2\theta}{cos^2\theta}$$
  $$1=tan^2\theta$$
  $$\sqrt{1}=\sqrt{tan^2\theta}$$
  $$1=tan\theta$$
  $$arctan1=45°$$
  <h3 class="text-gold">
    The optimal angle is 45 degrees.
  </h3>
  <h3>
    The optimal distance is 
  </h3>

  $$sin45°=\frac{\sqrt{2}}{2} \qquad cos45°=\frac{\sqrt{2}}{2}$$
  $$d(\theta)=\frac{2s^2}{g}cos\theta sin\theta$$
  $$\quad=\frac{2s^2}{g} \cdot \frac{\sqrt{2}}{2} \cdot \frac{\sqrt{2}}{2}$$
  <h3>
  $$\quad=\frac{s^2}{g}$$
  </h3>


  $$s=10m/s \quad g=10m/s^2$$
  $$d=100/10=10m$$
  </div>
</div>


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

  /* path　描画関数　*/
  function drawPath(svg,data,xScale,yScale,color){

    var pathData = data;

    var path = d3.svg.line()
        .x(function(d) { return xScale(d.x); })
        .y(function(d) { return yScale(d.y); })
        .interpolate("linear");

    svg.append("path")
          .attr("d", path(data))
          .attr("stroke", function(){return color})
          .attr("class","path")
          .attr("stroke-width", 2)
          .attr("fill", "none");   
 
  };


  var height = 450;
  var width = 500;
  

/** projectile with ordered set notation */
  var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",300)
                .attr("width",600)
                .style("background","black");

  var xScale01 = d3.scale.linear()
                       .domain([0,50])
                       .range([50,550]);
  
  var yScale01 = d3.scale.linear()
                       .domain([20,0])
                       .range([50,250]);                       

  // x axis
  drawVector(svg01,0,0,0,50,xScale01,yScale01,"#ccc");
  // y axis
  drawVector(svg01,0,0,90,20,xScale01,yScale01,"#ccc");
  // s vector
  drawVector(svg01,0,0,45,10,xScale01,yScale01,"#f00");

  // projectile path
  var pathData01 = [];
  var px,py;

  for (var i = 0; i < 3; i=i+0.1) {
    px = 20/Math.sqrt(2)*i;
    py = 20/Math.sqrt(2)*i-4.9*i*i;

    pathData01.push(new Point(px,py))
  };

  // path
  drawPath(svg01,pathData01,xScale01,yScale01,"#666");


  var foData01 = [
    {"x":6,"y":15,"text":"$$\\vec{s}$$"},
    {"x":2,"y":7.7,"text":"$$\\theta$$"},
    {"x":40,"y":5,"text":"$$d$$"}
      ];

  svg01.selectAll(".fo01")
  .data(foData01)
  .enter()
  .append("foreignObject")
  .attr("class","fo01")
  .attr("x",function(d){ return xScale01(d.x) })
  .attr("y",function(d){ return yScale01(d.y) })
  .append("xhtml:body")
  .html(function(d){return d.text;})
  .style("position","fixed")
  .style("font-size","1.1em"); 

  var svg02 = d3.select("#svg02")
                .append("svg")
                .attr("height",400)
                .attr("width",400)
                .style("background","black");

  var xScale02 = d3.scale.linear()
                       .domain([0,15])
                       .range([50,350]);
  
  var yScale02 = d3.scale.linear()
                       .domain([15,0])
                       .range([50,350]);                       

  // s vector 
  drawVector(svg02,0,0,45,15,xScale02,yScale02,"#f00");
  // s x vector
  drawVectorB(svg02,0,0,endPoint.x,0,xScale02,yScale02,"#ff0");
  // s y vector
  drawVectorB(svg02,endPoint.x,0,endPoint.x,endPoint.y,xScale02,yScale02,"#ff0");
  drawLine(svg02,endPoint.x-1,0,endPoint.x-1,1,xScale02,yScale02,"#666");
  drawLine(svg02,endPoint.x-1,1,endPoint.x,1,xScale02,yScale02,"#666");

  var foData02 = [
    {"x":4,"y":10,"text":"$$\\vec{s}$$"},
    {"x":2,"y":4,"text":"$$\\theta$$"},
    {"x":11,"y":9,"text":"$$\\vec{s}_{v}$$"},
    {"x":5,"y":2,"text":"$$\\vec{s}_{h}$$"}
      ];

  svg02.selectAll(".fo02")
  .data(foData02)
  .enter()
  .append("foreignObject")
  .attr("class","fo02")
  .attr("x",function(d){ return xScale02(d.x) })
  .attr("y",function(d){ return yScale02(d.y) })
  .append("xhtml:body")
  .html(function(d){return d.text;})
  .style("position","fixed")
  .style("font-size","1.1em"); 

  var svg03 = d3.select("#svg03")
                .append("svg")
                .attr("height",400)
                .attr("width",400)
                .style("background","black");

  var xScale03 = d3.scale.linear()
                       .domain([0,20])
                       .range([50,350]);
  
  var yScale03 = d3.scale.linear()
                       .domain([20,0])
                       .range([50,350]);                       

  // s y vector
  drawVectorB(svg03,5,0,5,10,xScale03,yScale03,"#0f0");
  drawVectorB(svg03,15,0,15,20,xScale03,yScale03,"#0f0");
  // a vector
  drawVectorB(svg03,8,10,8,0,xScale03,yScale03,"#ff0");
  drawVectorB(svg03,18,20,18,10,xScale03,yScale03,"#ff0");
  drawVectorB(svg03,18,10,18,0,xScale03,yScale03,"#ff0");
  drawLine(svg03,0,0,20,0,xScale03,yScale03,"#fff");

  var foData03 = [
    {"x":2,"y":15,"text":"10m/s"},
    {"x":12,"y":24,"text":"20m/s"},
    {"x":10,"y":10,"text":"1s"},
    {"x":20,"y":20,"text":"2s"},
    {"x":-1,"y":3,"text":"0"}
      ];

  svg03.selectAll(".fo03")
  .data(foData03)
  .enter()
  .append("foreignObject")
  .attr("class","fo03")
  .attr("x",function(d){ return xScale03(d.x) })
  .attr("y",function(d){ return yScale03(d.y) })
  .append("xhtml:body")
  .html(function(d){return d.text;})
  .style("position","fixed")
  .style("font-size","1.1em"); 


  var svg04 = d3.select("#svg04")
                .append("svg")
                .attr("height",400)
                .attr("width",400)
                .style("background","black");

  var xScale04 = d3.scale.linear()
                       .domain([0,90])
                       .range([50,350]);
  
  var yScale04 = d3.scale.linear()
                       .domain([10,0])
                       .range([50,350]);                       

  var xAxis04 = d3.svg.axis()
                  .scale(xScale04)
                  .tickValues([0,45,90])
                  .tickPadding(5)
                  .tickFormat(d3.format("d"));

  var xAxis04Group = svg04.append("g")
                      .attr("transform","translate(0,"+ yScale04(0)+")")
                      .attr("stroke","white")
                      .call(xAxis04);   

  var yAxis04 = d3.svg.axis()
                  .scale(yScale04)
                  .orient(["left"])
                  .tickValues([])
                  .tickPadding(0);

  var yAxis04Group = svg04.append("g")
                      .attr("transform","translate(" + xScale04(0) + ",0)")
                      .attr("stroke","white")
                      .call(yAxis04);

  drawLine(svg04,45,0,45,7.5,xScale04,yScale04,"#666");
  drawLine(svg04,0,7.5,90,7.5,xScale04,yScale04,"#00f");

  // projectile path
  var pathData04 = [];
  var px,py;

  for (var i = 0; i <= 90; i++) {
    px = i;
    py = 15*Math.cos(aDegree*i)*Math.sin(aDegree*i);

    pathData04.push(new Point(px,py))
  };

  // path
  drawPath(svg04,pathData04,xScale04,yScale04,"#666");

  var foData04 = [
    {"x":0,"y":13,"text":"$$d(\\theta)$$"},
    {"x":95,"y":2,"text":"$$\\theta$$"}
      ];

  svg04.selectAll(".fo04")
  .data(foData04)
  .enter()
  .append("foreignObject")
  .attr("class","fo04")
  .attr("x",function(d){ return xScale04(d.x) })
  .attr("y",function(d){ return yScale04(d.y) })
  .append("xhtml:body")
  .html(function(d){return d.text;})
  .style("position","fixed")
  .style("font-size","1.1em"); 

</script>
