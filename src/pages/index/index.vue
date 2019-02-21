<template>
  <div class="bgView">
    <div class="content">
        <div class="progress">
            <label for="" >timeline</label>
        </div>
        <div class="timeLineDiv">
               <div v-for="(item, index) in listArr" :key="index">
            <timeLine :obj='item' :index='index' :maxLength='listArr.length' ></timeLine>
        </div>
        </div>
    </div>
  </div>
</template>
<script>
import timeLine from "@/components/saTimeLine";
export default {
  data() {
    return {
      title: "阿里巴巴",
      content: "授权回话资源背景调查",
       listArr: [
        {
          title: "setp 1",
          content: "开始记录今天的生活",
          id:'0',
          isSelect:'1'
        },
        {
          title: "setp 2",
          content: "Know that I will live in my heart 深知我者才久居我心。",
          id:'1',
           isSelect:'0'
        },{
          title: "setp 3",
          content: "To the time to life, rather than to life in time to the time to life, rather than to life in time.给时光以生命，而不是给生命以时光。",
          id:'2',
           isSelect:'0'
        }
      ]
    };
  },

  components: {timeLine},

  methods: {
  
  },
  created() {
    let app = getApp();
  }
};
</script>

<style scoped>
.bgView {
  background-color: rgba(245, 245, 245, 1);
  height: 1206rpx;
}
.timeLineDiv {
    background-color: white;
    margin-top: 20rpx;
}
.progress {
    margin-left: 40rpx;
    margin-top: 20rpx;
    color: #999999;
}
</style>
