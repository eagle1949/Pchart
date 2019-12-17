# 堆叠图

#### 示例
<vuep template="#simple"></vuep>

<script v-pre type="text/x-template" id="simple">
<template>
    <p-stack-bar :data="data" style="width: 600px; height: 400px;"></p-stack-bar>
</template>

<script>
  export default {
    data () {
      return {
        data: {
            xAxis: ['2015年', '2016年', '2017年'],
            series: [
                { name: '优', data: [20, 25, 30] },
                { name: '良', data: [20, 25, 30] },
                { name: '轻度污染', data: [60, 50, 40] }
            ]
        }
      }
    }
  }
</script>
</script>

#### 横向展示
<vuep template="#simple_1"></vuep>

<script v-pre type="text/x-template" id="simple_1">
<template>
    <p-stack-bar 
        :data="data"
        style="width: 600px; height: 400px;"
    ></p-stack-bar>
</template>

<script>
  export default {
    data () {
      return {
        data: {
            yAxis: ['2015年', '2016年', '2017年'],
            series: [
                { name: '优', data: [20, 25, 30] },
                { name: '良', data: [20, 25, 30] },
                { name: '轻度污染', data: [60, 50, 40] }
            ]
        }
      }
    }
  }
</script>
</script>

#### 指定颜色
<vuep template="#simple_2"></vuep>

<script v-pre type="text/x-template" id="simple_2">
<template>
    <p-stack-bar
        style="width: 600px;height: 400px;"
        :data="data"
        :config="{
            color: 'airGradesColor'
        }"
    ></p-stack-bar>
</template>

<script>
  export default {
    data () {
      return {
        data: {
            xAxis: ['2015年', '2016年', '2017年'],
            series: [
                { name: '优', data: [20, 25, 30] },
                { name: '良', data: [20, 25, 30] },
                { name: '轻度污染', data: [60, 50, 40] }
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
| data.xAxis | x轴类目数据 | array | data.xAxis与data.yAxis 二选一 |
| data.yAxis | y轴类目数据 | array | data.xAxis与data.yAxis 二选一 |
| data.series | 系列数据 | array | 必须 |
| data.series[i].name | 系列名称 | string | 必须 |
| data.series[i].data | 系列中的数据内容数组 | array | 必须 |

#### config 配置项

| 配置项 | 简介 | 类型 | 备注 |
| --- | --- | --- | --- |
| color | 颜色 | array，string | 默认使用常规配色， 指定颜色如["#f00", "#00f"]，  或如"waterGradesColor"指定使用水质等级配色 [参考说明](/color)|
| unit | y轴数值单位 | string | 默认不显示 |
