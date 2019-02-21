<template>
  <div>
    <div class="listDiv">
      <div :class="index==0?'listDivItemFirst':'listDivItem'">
        <div :class="obj.isSelect=='1'?'circleSelect':'circle'">{{index + 1}}</div>
        <div class="timeLinelineTitle">{{obj.title}}</div>
      </div>
      <div :class="index==maxLength-1?'listDivItem1End':'listDivItem1'">
        <div  :class="index==maxLength-1?'timeLinelineEnd':'timeLineline'" v-bind:style="{ backgroundColor: lineColor }"></div>
        <div class="timeLinecontent">{{obj.content}}</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
   data() {
    return {
    
    };
  },
    //   "state":''
    //   "title":''
    //   "content":''
    //   "index":''
    //   "id",:''
    //   "isSelect":''
  props: ['obj','index','maxLength','lineColor'
  ],
  
};
</script>
<style>
.listDiv {
  display: flex;
  flex-direction: column;
}
.listDivItemFirst {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-left: 40rpx;
  margin-top: 40rpx;
}

.listDivItem {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-left: 40rpx;
}
.listDivItem1 {
  display: flex;
}
.listDivItem1End {
  margin-bottom: 20rpx;
  display: flex;
}
.timeLinelineTitle {
  font-size: 30rpx;
  color: #363636;
  font-weight: 650;
  margin-left: 20rpx;
  margin-top: -10rpx;
}
.timeLinecontent {
  font-size: 28rpx;
  color: #999999;
  padding-bottom: 20rpx;
  width: 600rpx;
}
.circleSelect {
  width: 60rpx;
  height: 60rpx;
  color: white;
  background-color: rgba(0, 121, 254, 1);
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.circle {
  width: 60rpx;
  height: 60rpx;
  color: #999999;
  background-color: white;
  border-radius: 50%;
  border: 2rpx solid lightgray;
  display: flex;
  justify-content: center;
  align-items: center;
}
.timeLineline {
  width: 4rpx;
  background-color: rgba(38, 156, 255, 1);
  margin-left: 70rpx;
  margin-right: 44rpx;
  box-shadow: 0rpx 0rpx 2rpx rgba(53, 210, 250, 1);
}
.timeLinelineEnd {
  height: 0rpx;
  margin-left: 70rpx;
  margin-right: 52rpx;
}
</style>
