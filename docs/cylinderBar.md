# 圆柱图

#### 示例
<vuep template="#simple"></vuep>

<script v-pre type="text/x-template" id="simple">
<template>
    <p-cylinder-bar 
        :data="data" 
        style="width: 600px; height: 400px;"
    ></p-cylinder-bar>
</template>

<script>
  export default {
    data () {
      return {
        data: {
            xAxis: ['氨氮', '总磷', '总氮', '生化需氧量', '高锰酸钾指数'],
            data: [26, 22, 15, 8, 5]
        }
      }
    }
  }
</script>
</script>

#### 设置颜色、数值单位和柱宽
<vuep template="#simple_1"></vuep>

<script v-pre type="text/x-template" id="simple_1">
<template>
    <p-cylinder-bar 
        :data="data" 
        :config="{
            color: 'normalColor',
            barWidth: 60,
            unit: '%'
        }"
        style="width: 600px; height: 400px;"
    ></p-cylinder-bar>
</template>

<script>
  export default {
    data () {
      return {
        data: {
            xAxis: ['氨氮', '总磷', '总氮', '生化需氧量', '高锰酸钾指数'],
            data: [26, 22, 15, 8, 5]
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
| data.data | 数据数组 | array | 必须 |

#### config 配置项

| 配置项 | 简介 | 类型 | 备注 |
| --- | --- | --- | --- |
| color | 颜色 | array，string | 默认使用常规配色， 指定颜色如["#f00", "#00f"]，  或如"waterGradesColor"指定使用水质等级配色 [参考说明](/color)|
| unit | 数值单位 | string | 默认不显示 |
| barWidth | 柱宽 | number | 默认为30 |
