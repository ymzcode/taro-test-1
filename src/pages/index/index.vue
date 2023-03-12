<template>
  <view class="index">
    <nut-collapse v-model="activeNames" @change="collapseChange">
      <nut-collapse-item v-for="(item) in filterListArr" :title="item.title" :key="item.catalogId" :name="item.catalogId">
        NutUI是一套拥有京东风格的轻量级的 Vue 组件库
      </nut-collapse-item>
    </nut-collapse>
  </view>
</template>

<script setup>
import {onMounted, reactive, ref, toRefs} from 'vue';
import Taro from "@tarojs/taro";

const activeNames = ref([1])
const collapseChange = (data) => {
  console.log(data)
}

const filterListArr = ref([
  {
    "catalogId": 1,
    "subjectId": 5,
    "parentId": 0,
    "ancestors": null,
    "title": "1Z301000 建设工程基本法律知识",
    "context": null,
    "total": 24,
    "sort": 1,
    "status": "0",
    "remark": null,
    "recordTotal": 0
  },
  {
    "catalogId": 12,
    "subjectId": 5,
    "parentId": 0,
    "ancestors": null,
    "title": "1Z302000 施工许可法律制度",
    "context": null,
    "total": 9,
    "sort": 12,
    "status": "0",
    "remark": null,
    "recordTotal": 0
  },
  {
    "catalogId": 16,
    "subjectId": 5,
    "parentId": 0,
    "ancestors": null,
    "title": "1Z303000 建设工程发承包法律制度",
    "context": null,
    "total": 11,
    "sort": 16,
    "status": "0",
    "remark": null,
    "recordTotal": 0
  },
  {
    "catalogId": 20,
    "subjectId": 5,
    "parentId": 0,
    "ancestors": null,
    "title": "1Z304000 建设工程合同和劳动合同法律制度",
    "context": null,
    "total": 22,
    "sort": 20,
    "status": "0",
    "remark": null,
    "recordTotal": 0
  },
  {
    "catalogId": 24,
    "subjectId": 5,
    "parentId": 0,
    "ancestors": null,
    "title": "1Z305000 建设工程施工环境保护、节约能源和文物保护法律制度",
    "context": null,
    "total": 8,
    "sort": 24,
    "status": "0",
    "remark": null,
    "recordTotal": 0
  },
  {
    "catalogId": 28,
    "subjectId": 5,
    "parentId": 0,
    "ancestors": null,
    "title": "1Z306000 建设工程安全生产法律制度",
    "context": null,
    "total": 18,
    "sort": 28,
    "status": "0",
    "remark": null,
    "recordTotal": 0
  },
  {
    "catalogId": 34,
    "subjectId": 5,
    "parentId": 0,
    "ancestors": null,
    "title": "1Z307000 建设工程质量法律制度",
    "context": null,
    "total": 13,
    "sort": 34,
    "status": "0",
    "remark": null,
    "recordTotal": 0
  },
  {
    "catalogId": 40,
    "subjectId": 5,
    "parentId": 0,
    "ancestors": null,
    "title": "1Z308000 解决建设工程纠纷法律制度",
    "context": null,
    "total": 20,
    "sort": 40,
    "status": "0",
    "remark": null,
    "recordTotal": 0
  }
])

onMounted(async () => {
  // const res = await Taro.request({
  //   url: 'https://exam.zhengerbajingedu.com/api/catalog/list',
  //   data: {
  //     subjectId: 5,
  //     parentId: 0
  //   }
  // })
  // filterListArr.value = res.data.data
  // console.log(res)
})

</script>

<style lang="scss">

</style>
