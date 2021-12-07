# area-data-mj

适用于密接业务系统的中国行政区域数据(含港澳台)，基于 area-data 模块改造，精确到乡镇/街道级。

## v1.0.2
- 升级开发依赖模块 lodash 至最新版（v4.7.21）；
- 修复 Bug#00001：引入主模块后控制台报错（找不到 'area-data/pca' 模块）。

## v1.0.1
- 修改 GitHub 仓库名，同时更新 package.json 的相关信息。

## v1.0.0
- 重新改造区市县模块 `pcaa.js`，封装为适用于深圳密接项目的行政区划版本。


## doc


[详见 area-data 文档页](https://github.com/dwqs/area-data#readme)


## Installation
Install the pkg with npm:

```
npm install area-data-mj --save
```

or yarn

```
yarn add area-data-mj
```

or bower

```
bower install area-data-mj
```

## 获取数据
```
// v5之前的版本
import AreaData from 'area-data-mj';

// v5及之后的版本
import { pca, pcaa } from 'area-data-mj';
// 可以根据需要按需引入：
import PCA from 'area-data-mj/pca'; 
import PCAA from 'area-data-mj/pcaa'; 

pca['86'] // 等同于 AreaData['86']
// 所有省份：{'110000': '北京市', '120000': '天津市', '130000': '河北省', ...}

pcaa['130000'] // 等同于 AreaData['130000']
// 对应省份的所有城市：{'130100': '石家庄市', '130200': '唐山市', '130300': '秦皇岛市', ...}

pcaa['130200'] // 等同于 AreaData['130200']
// 对应市的所有县区：{'130201': '市辖区', '130202': '路南区', '130203': '路北区', ...}

### v1
AreaData['130202']
// 对应县区的所有街道：{'130202001000': '学院南路街道', '130202002000': '友谊街道', ...}
```

> 官方数据(截止到2016.07.31): [城乡区域划分](http://www.stats.gov.cn/tjsj/tjbz/tjyqhdmhcxhfdm/2016/index.html)

**数据来源：** 最新省市区数据来自 [area-puppeteer](https://github.com/dwqs/area-puppeteer/).

## LICENSE

MIT

