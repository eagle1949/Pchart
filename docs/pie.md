# 饼图

#### 示例
<vuep template="#simple-pie"></vuep>

<script v-pre type="text/x-template" id="simple-pie">
<template>
    <p-pie :data="pieData" style="width: 400px; height: 400px;"></p-pie>
</template>

<script>
  export default {
    data () {
      return {
        pieData: [
            { name: 'Ⅰ类', value: 5 },
            { name: 'Ⅱ类', value: 5 },
            { name: 'Ⅲ类', value: 30 },
            { name: 'Ⅳ类', value: 20 },
            { name: 'Ⅴ类', value: 10 },
            { name: '劣Ⅴ类', value: 2 }
        ]
      }
    }
  }
</script>
</script>

#### 圆环图
<vuep template="#simple-pie_1"></vuep>
<script v-pre type="text/x-template" id="simple-pie_1">
<template>
    <p-pie
        :data="pieData"
        :config="{
            color: 'waterGradesColor',
            title: '总个数\n300',
            type: 'ring'
        }"
        style="width: 400px;height: 400px;"
    ></p-pie>
</template>

<script>
  export default {
    data () {
      return {
        pieData: [
            { name: 'Ⅰ类', value: 5 },
            { name: 'Ⅱ类', value: 5 },
            { name: 'Ⅲ类', value: 30 },
            { name: 'Ⅳ类', value: 20 },
            { name: 'Ⅴ类', value: 10 },
            { name: '劣Ⅴ类', value: 2 }
        ]
      }
    }
  }
</script>
</script>

#### 玫瑰图
<vuep template="#simple-pie_2"></vuep>

<script v-pre type="text/x-template" id="simple-pie_2">
<template>
    <p-pie
        :data="pieData"
        :config="{
            color: 'waterGradesColor',
            type: 'rose',
            showLegend: true
        }"
        style="width: 400px;height: 400px;"
    ></p-pie>
</template>

<script>
  export default {
    data () {
      return {
        pieData: [
            { name: 'Ⅰ类', value: 5 },
            { name: 'Ⅱ类', value: 5 },
            { name: 'Ⅲ类', value: 30 },
            { name: 'Ⅳ类', value: 20 },
            { name: 'Ⅴ类', value: 10 },
            { name: '劣Ⅴ类', value: 2 }
        ]
      }
    }
  }
</script>
</script>

#### data 数据

| 数据项 | 简介 | 类型 | 备注 |
| --- | --- | --- | --- |
| data[i].name | 数据项名称 | string | 用于tooltip的显示，legend 的图例筛选，必须 |
| data[i].value | 数据值 | number | 必须 |

#### config 配置项

| 配置项 | 简介 | 类型 | 备注 |
| --- | --- | --- | --- |
| color | 颜色 | array，string | 默认使用常规配色， 指定颜色如["#f00", "#00f"]，  或如"waterGradesColor"指定使用水质等级配色 [参考说明](/color)|
| showLegend | 是否显示图例 | boolean | 默认为false 不显示 |
| showLabel | 是否显示线条文字 | boolean | 默认为true |
| title | 中间的文字 | string | 默认不显示 |
| type | 形态类型 | string | 实心圆circle， 圆环ring，  玫瑰图rose， 默认为实心圆 |



