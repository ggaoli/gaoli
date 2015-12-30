# 地理位置选择
该插件结合城市三级联动下拉选择与地图选择 ，能够通过填写搜索或者城市地图选择准确定位位置。
##兼容性
- ie6+
- ALL

##插件相关文件介绍
  - map.css：插件样式文件
  - jquery-1.9.1.min.js：插件使用的依赖文件
  - map.js：地图文件
  - jquery.select-city.js：城市三级联动选择文件
  - allareas.json：城市数据文件

##插件使用

###1、css文件引用

```
<link href="style/map.css" rel="stylesheet" type="text/css" />
```     
###2、js文件引用
```
    //jqury文件
    <script src="javascript/jquery-1.9.1.min.js"></script>
    //在线地图
    <script src="http://webapi.amap.com/maps?v=1.3&amp;key=a2627897194b5d9aad9b47e7db2227d5"></script>
    //地图配置文件
    <script src="javascript/map.js"type="text/javascript"charset="utf8"></script>
    //城市三级联动文件
    <script src="javascript/jquery.select-city.js"type="text/javascript" charset="utf8"></script>
```    

###3、html中代码结构

- 必要className、ID介绍
 ` mapPick、areaselct`：必要ID

 `map-pin-box`：地图外层容器
 
 `area-select` ：插件外层容器
 
 `city-province`：省份
 
 `city-city`：市区
 
 `city-district`：县级
- html中代码结构
```
<div class="pad20 clearfix" id="mapPick">
  <div class="row margin-t area-select "id="areaselct">
   <div class="large-2 columns  " >
      <select class="city-province" name="province"></select>
   </div>
   <div class="large-2 columns ">
      <select class="city-city" name="city"></select>
   </div>
   <div class="large-2 columns ">
      <select class="city-district" name="district"></select>
   </div>
   <div class="large-5 columns">
     <div class="map-pin-box">
       <a class="pic-map"></a>
       <input type="text" id="keyword" name="keyword" value="" onkeydown='keydown(event)'/>
       <div id="result1" name="result1" class="result-box"></div>
          <div class="map-piker-show">
             <div id="mapContainer" ></div>
             <div class="map-annotation">
               <span class="annot1">点击地图可直接定位，拖动箭头到新的位置</span>
               <span class="annot2">收起</span>
              </div>
           </div>
       </div>
    </div>
  </div>
</div>
```

- html中插件的初始化
```  
 e.selectareas.init($('#mapPick'));
```
##demo演示
- [地图地址选择插件demo][1]

#更新日志
- 实现城市三级联动以及地图所在区域联动，兼容ie6+ 以及主流浏览器。

    
  

  


  [1]: http://192.168.14.97:8080/acc/plugin/map_picker/map-picker.html
