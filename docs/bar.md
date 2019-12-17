# 柱状图

#### 示例
<vuep template="#simple"></vuep>

<script v-pre type="text/x-template" id="simple">
<template>
    <p-bar :data="data" style="width: 600px; height: 400px;"></p-bar>
</template>

<script>
  export default {
    data () {
      return {
        data: {
            xAxis: ['2014年', '2015年', '2016年', '2017年', '2018年', '2019年'],
            series: [
                {
                    name: '2018年',
                    data: [22, 33, 28, 36, 28, 35]
                },
                {
                    name: '2019年',
                    data: [28, 36, 28, 35, 22, 33]
                }
            ]
        }
      }
    }
  }
</script>
</script>


#### 显示数值及单位
<vuep template="#simple_1"></vuep>

<script v-pre type="text/x-template" id="simple_1">
<template>
    <p-bar 
        :data="data" 
        :config="{
            unit: 'mg/L',
            showLabel: true
        }"
        style="width: 600px; height: 400px;"
    ></p-bar>
</template>

<script>
  export default {
    data () {
      return {
        data: {
            xAxis: ['2014年', '2015年', '2016年', '2017年', '2018年', '2019年'],
            series: [
                {
                    name: '2018年',
                    data: [22, 33, 28, 36, 28, 35]
                },
                {
                    name: '2019年',
                    data: [28, 36, 28, 35, 22, 33]
                }
            ]
        }
      }
    }
  }
</script>
</script>

#### 线柱混合
<vuep template="#simple_2"></vuep>

<script v-pre type="text/x-template" id="simple_2">
<template>
    <p-bar 
        :data="data"
        style="width: 600px; height: 400px;"
    ></p-bar>
</template>

<script>
  export default {
    data () {
      return {
        data: {
            xAxis: ['2014年', '2015年', '2016年', '2017年', '2018年', '2019年'],
            series: [
                {
                    name: '均值',
                    type: 'line',
                    data: [2, 1, 2, 4, 5, 3]
                },
                {
                    name: '2018年',
                    data: [2.5, 1.5, 3, 4, 5.5, 3.5]
                },
                {
                    name: '2019年',
                    data: [1.5, 0.5, 1, 4, 4.8, 2.5]
                }
            ]
        }
      }
    }
  }
</script>
</script>

#### data 数据

| 数据项 | 简介 | 类型 | 备注 |
| --- | --- | --- | --- |
| data.xAxis | x轴类目数据 | array | 必须 |
| data.series | 系列数据 | array | 必须 |
| data.series[i].name | 系列名称 | string | 必须 |
| data.series[i].type | 系列类型 | string | 设置为'line'时指定对应数据按折线展示 可选  |
| data.series[i].data | 系列中的数据内容数组 | array | 必须 |

#### config 配置项

| 配置项 | 简介 | 类型 | 备注 |
| --- | --- | --- | --- |
| color | 颜色 | array，string | 默认使用常规配色， 指定颜色如["#f00", "#00f"]，  或如"waterGradesColor"指定使用水质等级配色|
| showLabel | 是否显示数值文字 | boolean | 默认为false |
| unit | y轴数值单位 | string | 默认不显示 |
