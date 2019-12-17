# 水环境业务示例

#### 水质分类构成  
参考说明：[饼图](/pie)
<vuep template="#simple_1"></vuep>
<script v-pre type="text/x-template" id="simple_1">
<template>
    <p-pie business="waterGrades" :data="data" style="width: 400px; height: 300px;"></p-pie>
</template>

<script>
  export default {
    data () {
      return {
        data: [
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

#### 水质分类构成 合并Ⅰ~Ⅱ类
参考说明：[饼图](/pie)
<vuep template="#simple_2"></vuep>
<script v-pre type="text/x-template" id="simple_2">
<template>
    <p-pie business="merge1n2WaterGrades" :data="data" style="width: 400px; height: 300px;"></p-pie>
</template>

<script>
  export default {
    data () {
      return {
        data: [
            { name: 'Ⅰ~Ⅱ类', value: 10 },
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

#### 水质富营养状态分类构成
参考说明：[饼图](/pie)
<vuep template="#simple_3"></vuep>
<script v-pre type="text/x-template" id="simple_3">
<template>
    <p-pie business="eutrophicationColor" :data="data" style="width: 400px; height: 300px;"></p-pie>
</template>

<script>
  export default {
    data () {
      return {
        data: [
            { name: '贫营养', value: 10 },
            { name: '中营养', value: 30 },
            { name: '轻度富营养', value: 20 },
            { name: '中度富营养', value: 10 },
            { name: '重度富营养', value: 2 }
        ]
      }
    }
  }
</script>
</script>

#### 水质分类构成变化
参考说明：[堆叠图](/stackBar)
<vuep template="#simple_4"></vuep>
<script v-pre type="text/x-template" id="simple_4">
<template>
    <p-stack-bar
        style="width: 500px;height: 500px;"
        :data="data"
        :config="{
            color: 'waterGradesColor'
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
                { name: 'Ⅰ类', data: [20, 25, 30] },
                { name: 'Ⅱ类', data: [20, 25, 30] },
                { name: 'Ⅲ类', data: [60, 50, 30] },
                { name: 'Ⅳ类', data: [0, 0, 10] },
                { name: 'Ⅴ类', data: [0, 0, 0] },
                { name: '劣Ⅴ类', data: [0, 0, 0] },
            ]
        }
      }
    }
  }
</script>
</script>

#### 水质构成热力图
参考说明：[热力图](/heatmap)
<vuep template="#simple_5"></vuep>
<script v-pre type="text/x-template" id="simple_5">
<template>
    <p-heatmap
        style="width: 500px;height: 600px;"
        business="waterGrades"
        :data="data"
    ></p-heatmap>

</template>

<script>
  export default {
    data () {
      return {
        data: {
          xAxis: ['2015年', '2016年', '2017年', '2018年', '2019年'],
          series: [
              { name: '广州市', data: [1, 2, 3, 4, 5] },
              { name: '深圳市', data: [1, 2, 3, 4, 5] },
              { name: '东莞市', data: [1, 6, 3, 4, 5] },
              { name: '广州市', data: [1, 2, 3, 4, 5] },
              { name: '广州市', data: [3, 2, 3, 4, 5] },
              { name: '广州市', data: [3, 2, 3, 4, 5] },
              { name: '广州市', data: [1, 2, 3, 4, 5] },
              { name: '广州市', data: [1, 2, 3, 4, 5] },
              { name: '广州市', data: [1, 2, 3, 4, 5] },
              { name: '中山市', data: [6, 2, 3, 4, 5] }
          ]
        }
      }
    }
  }
</script>
</script>

#### 水质指数排名
参考说明：[条纹图](/stripeBar)
<vuep template="#simple_6"></vuep>
<script v-pre type="text/x-template" id="simple_6">
<template>
    <p-stripe-bar
        style="width: 500px;height: 500px;"
        :data="data"
    ></p-stripe-bar>

</template>

<script>
  export default {
    data () {
      return {
        data: [
          { name: '广州', rank: 1, value: 2.5 },
          { name: '广州', rank: 2, value: 2.8 },
          { name: '广州', rank: 3, value: 2.9 },
          { name: '广州', rank: 4, value: 3.1 },
          { name: '广州', rank: 5, value: 3.5 },
          { name: '广州', rank: 6, value: 3.8 },
          { name: '广州', rank: 7, value: 4.5 },
          { name: '广州', rank: 8, value: 4.8 },
          { name: '广州', rank: 9, value: 5.6 },
          { name: '广州', rank: 10, value: 5.8 },
          { name: '广州', rank: 11, value: 5.8 },
          { name: '广州', rank: 12, value: 6.2 }
        ]
      }
    }
  }
</script>
</script>