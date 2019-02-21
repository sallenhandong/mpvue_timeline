<template>
  <div class="bgView">
    <div class="content">
        <div class="progress">
            <label for="" >timeline</label>
        </div>
        <div class="timeLineDiv">
               <div v-for="(item, index) in listArr" :key="index">
            <timeLine :obj='item' :index='index' :maxLength='listArr.length' :saClass="'sa_timeClass_Dot'"></timeLine>
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
        },{
          title: "setp 4",
          content: "Whatever is worth doing is worth doing well.任何值得做的，就把它做好。",
          id:'2',
           isSelect:'0'
        },{
          title: "setp 5",
          content: "You may be out of my sight, but never out of my mind.你也许已走出我的视线，但从未走出我的思念。",
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
