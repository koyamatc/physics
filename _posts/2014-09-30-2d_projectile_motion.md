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
    <br><br><br><br><br><br><br><br>
    <h3>
    
     $$\vec{a} + \vec{b} = \vec{c}$$
     ---------
     $$\vec{x}_{h}:x \quad horisontal$$
     $$\vec{x}_{v}:x \quad vertical$$
     $$\vec{x} = \vec{x}_{h} + \vec{x}_{v}$$
     
    </h3>
  </div>
</div>

<div class="row">
  <div class="col-sm-6">
    <div id="svg02"></div>
  </div>
  <div class="col-sm-6">
    <br><br><br><br>
    $$displacement:\quad \| \vec{a} \|=5$$
    $$angle \quad \theta = 36.8699°$$
    $$\| \vec{a}_{x} \| = \| \vec{a} \| \centerdot cos\theta = 4 $$
    $$\| \vec{a}_{y} \| = \| \vec{a} \| \centerdot sin\theta = 3 $$
  </div>
</div>

--------

### Projectile an angle

<div class="row">
  <div class="col-sm-6">
    <div id="svg03"></div>
  </div>
  <div class="col-sm-6">
    Lauanch a rocket
    $$\quad velocity:\vec{v}=10m/s$$ 
    $$\quad direction:\theta= 30° \quad upward \quad from \quad the \quad ground$$
    <div class="panel">
      How far does it travel?
    </div> 
  </div>
</div>

<div>
$$\| \vec{v}_{y} \| :$$
$$\quad sin30° = \frac{\|\vec{v}_{y}\|}{\|\vec{v}\|}
\rightarrow \|\vec{v}_{y}\|=\|\vec{v}\|sin30°=10m/s \centerdot \frac{1}{2}=5m/s$$
  
$$\| \vec{v}_{x} \|:$$
$$\quad cos30° = \frac{\|\vec{v}_{x}\|}{\|\vec{v}\|}
\rightarrow \|\vec{v}_{x}\|=\|\vec{v}\|cos30°=10m/s \centerdot \frac{\sqrt{3}}{2}=5\sqrt{3}m/s$$

$$change \quad in \quad velocity:\Delta \vec{v}_{g}
=\vec{v}_{f}-\vec{v}_{i}=\vec{a}_{g} \centerdot \Delta t$$
$$\quad initial \quad velocity = -final \quad velocity$$
$$\quad \Delta \vec{v}_{g}=\vec{v}_{f}-\vec{v}_{i}
=-5m/s-5m/s=-10m/s
$$

$$change \quad in \quad time\quad (time \quad in \quad air): 
\Delta t = \frac{\vec{v}_{g}}{\vec{a}_{g}}$$
$$\quad acceleration:\vec{a}_{g}=-9.8m/s^2$$
$$\quad \Delta t = \frac{-10m/s}{-9.8m/s^2} =1.02s$$ 

$$displacement(how \quad far \quad a \quad rocket \quad travels):
=\vec{v}_{x} \centerdot \Delta t$$
$$\quad \vec{s}_{x}=5\sqrt{3}m/s \centerdot 1.02s = 8.83m$$
</div>

<div class="panel">
  A rocket travels 8.83 meters.
</div>

------------

### Different way to determine time in air

<div class="panel">
$$vertical \quad velocity: \vec{v}_{y}=5m/s$$
$$displacement:\vec{s}=\vec{v}_{average} \centerdot \Delta t$$
$$average \quad velocity:\vec{v}_{avg}=\frac{\vec{v}_{i}+\vec{v}_{f}}{2}$$
$$final \quad velocity:\vec{v}_{f}=\vec{v}_{i}+\vec{a} \centerdot \Delta t$$
</div>

$$\vec{s}=\frac{\vec{v}_{i}+\vec{v}_{i}+\vec{a} \centerdot \Delta t}{2}\centerdot\Delta t$$
<div class="panel">
  $$\vec{s}=\vec{v}_{i}\centerdot \Delta t + \frac{\vec{a}}{2}\centerdot (\Delta t)^2$$
</div>

$$\vec{s}=5m/s \centerdot \Delta t + -4.9m/s^2 \centerdot (\Delta t)^2$$
$$vertical \quad displacement: 0m \nearrow peak \searrow 0m$$
$$0=5m/s \centerdot \Delta t + -4.9m/s^2 \centerdot (\Delta t)^2$$
$$0=\Delta t(5m/s-4.9m/s^2 \centerdot \Delta t)$$

This equation equals to 0 when
$$\Delta t=0$$
and
$$5m/s-4.9m/s^2 \centerdot \Delta t=0$$
$$\Delta t=\frac{-5m/s}{-4.9m/s^2}$$
<div class="panel">
$$\Delta t=1.02s$$
</div>

--------------

### Launching and landing on different elevations

<div class="row">
  <div class="col-sm-6">
    <div id="svg04"></div>
  </div>
  <div class="col-sm-6">
  Launch a rocket
  $$\quad velocity:90m/s$$
  $$\quad direction:53°$$
  How far does a rocket travel?
  $$\|\vec{v}_{y}\|=90sin53°$$
  $$\|\vec{v}_{x}\|=90cos53°$$
    <div class="panel">
    $$\vec{s}=\vec{v}_{i}\centerdot \Delta t + \frac{\vec{a}}{2}\centerdot (\Delta t)^2$$
    </div>
  </div>
</div>
$$-16=(90sin53°)\centerdot \Delta t - 4.9(\Delta t)^2
\rightarrow -4.9(\Delta t)^2 + (90sin53°)\centerdot \Delta t + 16 = 0
$$ 

<div class="panel">
  $$ax^2 + bx + c = 0 \rightarrow
  x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}$$
</div>

$$\Delta t = \frac{-(90sin53°)\pm\sqrt{(90sin53°)^2-4\times (-4.9)\times 16}}{2\times(-4.9)}$$
time is positive
$$\Delta t = \frac{-(71.8772)-\sqrt{5166.3319+313.6}}{-9.8}=14.89s$$
horisontal displacement is
$$\vec{s}_{x}=90cos53°\times 14.89=806.5m$$

--------------

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


  var height = 450;
  var width = 500;
  
  var xScale01 = d3.scale.linear()
                       .domain([-200,200])
                       .range([50,450]);
  
  var yScale01 = d3.scale.linear()
                       .domain([200,-200])
                       .range([50,450]);                       

/**
  2-dimentional vectors
*/

var svg01 = d3.select("#svg01")
                .append("svg")
                .attr("height",height)
                .attr("width",width);

  // left right              
  drawVector(svg01,-150,150,180,50,xScale01,yScale01,"gold");
  drawVector(svg01,-140,150,0,50,xScale01,yScale01,"gold");               
  // up down
  drawVector(svg01,100,160,90,50,xScale01,yScale01,"gold");
  drawVector(svg01,100,150,-90,50,xScale01,yScale01,"gold");  

  drawVector(svg01,-150,-100,30,150,xScale01,yScale01,"red");
  drawVector(svg01,endPoint.x,endPoint.y,-10,100,xScale01,yScale01,"lime");  
  drawVector(svg01,-150,-100,14,235,xScale01,yScale01,"gold");

  drawVectorB(svg01,0,-150,170,-50,xScale01,yScale01,"lime");
  drawVectorB(svg01,0,-150,170,-150,xScale01,yScale01,"#666");
  drawVectorB(svg01,170,-150,170,-50,xScale01,yScale01,"#666");

  var foData = [
    {"x":-220,"y":280,
      "text":"$$one \\quad dimention \\quad  vectors$$"},
    {"x":-220,"y":100,
      "text":"$$two \\quad dimentions \\quad vectors$$"},
    {"x":-180,"y":220,
      "text":"$$\\vec{a}$$"},
    {"x":-120,"y":220,
      "text":"$$\\vec{b}$$"},
    {"x":105,"y":240,
      "text":"$$\\vec{a}$$"},
    {"x":105,"y":195,
      "text":"$$\\vec{b}$$"},
    {"x":-85,"y":10,
      "text":"$$\\vec{a}$$"},
    {"x":10,"y":40,
      "text":"$$\\vec{b}$$"},
    {"x":-40,"y":-25,
      "text":"$$\\vec{c}$$"},

    {"x":80,"y":-20,
      "text":"$$\\vec{x}$$"},
    {"x":80,"y":-105,
      "text":"$$\\vec{x}_{h}$$"},
    {"x":180,"y":-50,
      "text":"$$\\vec{x}_{v}$$"}

  ];
  svg01.selectAll(".fo")
  .data(foData)
  .enter()
  .append("foreignObject")
  .attr("class","fo")
//  .attr("height","100%")
//  .attr("width","100%")
  .attr("x",function(d){ return xScale01(d.x) })
  .attr("y",function(d){ return yScale01(d.y) })
.append("xhtml:body")
  .html(function(d){return d.text;})
  .style("position","fixed")
  .style("font-size","1.2em");   

/** */
var svg02 = d3.select("#svg02")
                .append("svg")
                .attr("height",400)
                .attr("width",400)
                .style("background","black");

  var xScale02 = d3.scale.linear()
                       .domain([-0.5,5])
                       .range([50,350]);
  
  var yScale02 = d3.scale.linear()
                       .domain([5,-0.5])
                       .range([50,350]);                       

  var xAxis02 = d3.svg.axis()
                  .scale(xScale02)
                  .tickValues([])
                  .tickPadding(5)
                  .tickFormat(d3.format("d"));

  var xAxis02Group = svg02.append("g")
                      .attr("transform","translate(0,"+ yScale02(0)+")")
                      .attr("stroke","white")
                      .call(xAxis02);   

  var yAxis02 = d3.svg.axis()
                  .scale(yScale02)
                  .orient(["left"])
                  .tickValues([])
                  .tickPadding(0);

  var yAxis02Group = svg02.append("g")
                      .attr("transform","translate(" + xScale02(0) + ",0)")
                      .attr("stroke","white")
                      .call(yAxis02);

  drawVectorB(svg02,0,0,4,3,xScale02,yScale02,"lime");
  drawVectorB(svg02,0,0,4,0,xScale02,yScale02,"#666");
  drawVectorB(svg02,4,0,4,3,xScale02,yScale02,"#666");

  var foData02 = [
    {"x":0.1,"y":6,"text":"y"},
    {"x":5,"y":0.5,"text":"x"},
    {"x":0.5,"y":1.2,"text":"$$\\theta$$"},
    {"x":2,"y":3,"text":"$$\\vec{a}$$"},
    {"x":2.3,"y":0.5,"text":"$$\\vec{a}_{x}$$"},
    {"x":4.2,"y":2.5,"text":"$$\\vec{a}_{y}$$"}
    
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
  .style("font-size","1.2em");   

/** */
var svg03 = d3.select("#svg03")
                .append("svg")
                .attr("height",100)
                .attr("width",400)
                .style("background","black");

  var xScale03 = d3.scale.linear()
                       .domain([0,20])
                       .range([50,350]);
  
  var yScale03 = d3.scale.linear()
                       .domain([8,0])
                       .range([10,80]);                       

  var xAxis03 = d3.svg.axis()
                  .scale(xScale03)
                  .tickValues([])
                  .tickPadding(5)
                  .tickFormat(d3.format("d"));

  var xAxis03Group = svg03.append("g")
                      .attr("transform","translate(0,"+ yScale03(0)+")")
                      .attr("stroke","white")
                      .call(xAxis03);   

  var yAxis03 = d3.svg.axis()
                  .scale(yScale03)
                  .orient(["left"])
                  .tickValues([])
                  .tickPadding(0);

  var yAxis03Group = svg03.append("g")
                      .attr("transform","translate(" + xScale03(0) + ",0)")
                      .attr("stroke","white")
                      .call(yAxis03);


  drawVector(svg03,0,0,30,10,xScale03,yScale03,"lime");
  drawVectorB(svg03,endPoint.x,0,endPoint.x,endPoint.y,xScale03,yScale03,"#666");                    
  drawVectorB(svg03,0,0,endPoint.x,0,xScale03,yScale03,"#666");                    

  var foData03 = [
    {"x":3,"y":10,"text":"$$\\vec{v}$$"},
    {"x":3,"y":7,"text":"$$\\theta$$"},
    {"x":4,"y":5,"text":"$$\\vec{v}_{x}$$"},
    {"x":9,"y":9,"text":"$$\\vec{v}_{y}$$"}
    
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
  .style("font-size","1.2em");   

/** */
var svg04 = d3.select("#svg04")
                .append("svg")
                .attr("height",400)
                .attr("width",400)
                .style("background","black");

  var xScale04 = d3.scale.linear()
                       .domain([0,300])
                       .range([50,350]);
  
  var yScale04 = d3.scale.linear()
                       .domain([300,0])
                       .range([50,350]);                       

  var line04Data = [{"x":0,"y":250},
                    {"x":50,"y":250},
                    {"x":50,"y":0},
                    {"x":280,"y":0},
                    {"x":280,"y":90},
                    {"x":320,"y":90}
                    ];                       
  var line04 = d3.svg.line()
        .x(function(d) { return xScale04(d.x); })
        .y(function(d) { return yScale04(d.y); })
        .interpolate("linear");

    svg04.append("path")
          .attr("d", line04(line04Data))
          .attr("stroke", function(){return "#fff"})
          .attr("class","vector")
          .attr("stroke-width", 3)
          .attr("fill", "none");   

  drawVector(svg04,40,250,53,40,xScale04,yScale04,"lime");
  drawVectorB(svg04,35,0,35,247,xScale04,yScale04,"#f00");                    
  drawVectorB(svg04,35,247,35,3,xScale04,yScale04,"#f00");                    
  drawVectorB(svg04,300,0,300,87,xScale04,yScale04,"#f00");                    
  drawVectorB(svg04,300,87,300,3,xScale04,yScale04,"#f00");                    
  drawVectorB(svg04,300,93,300,247,xScale04,yScale04,"aqua");                    
  drawVectorB(svg04,300,247,300,93,xScale04,yScale04,"aqua");                    

  var foData04 = [
    {"x":0,"y":200,"text":"$$25m$$"},
    {"x":305,"y":110,"text":"$$9m$$"},
    {"x":305,"y":250,"text":"$$\\vec{s}_{y}=-16m$$"},
    {"x":50,"y":310,"text":"$$53°$$"},
    {"x":20,"y":360,"text":"$$90m/s$$"}
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
  .style("font-size","1.2em");   

</script>
