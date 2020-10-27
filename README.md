## 文档提要

本文档为学习openlayers建立，文档不足之处，请各位斧正。

---

## openlayers的安装和使用
### openlayers安装

openlayers的安装
```
npm install ol 
或
yarn add ol 
```
挂载到html上
```
import 'ol/ol.css';                     //引入ol样式
import {Map, View} from 'ol';           //引入Map对象，View对象
import TileLayer from 'ol/layer/Tile';  //引入瓦片图层对象
import OSM from 'ol/source/OSM';        //引入资源对象
const map = new Map({
  target: 'map',
  layers: [
    new TileLayer({
      source: new OSM()
    })
  ],
  view: new View({
    center: [0, 0],
    zoom: 0
  })
});
```
```
<!DOCTYPE html>
<html>
    ...
    <!-- 用于挂载的div -->
    <div id="map"></div>
</html>
```
效果如下
![地图图片展示](/img/mapshow.png)

### openlayers的基本属性
```
const map = new Map({
    target: 'map',          //挂载的DOM对象id
    layers: [],             //图层
    view: {},               //视图
    control: {},            //控件
    interaction: {},        //交互
})
```

---
以下为markdown格式记录，文档完成后删除
Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/wangminger/YSopenlayersdoc.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
