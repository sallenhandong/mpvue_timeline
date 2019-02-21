<template>
  <div>
    <div :class="saClass">
      <div :class="index==0?'listDivItemFirst':'listDivItem'">
        <div v-if="saClass=='sa_timeClass_Dot'">
          <div class="style1_circle">
            <div class="style1_circle_dot"></div>
          </div>
        </div>
        <block v-else-if="saClass=='sa_timeClass_Number'">
          <div :class="obj.isSelect=='1'?'circleSelect':'circle'">{{index + 1}}</div>
        </block>
        <div class="timeLinelineTitle">{{obj.title}}</div>
      </div>
      <div :class="index==maxLength-1?'listDivItem1End':'listDivItem1'">
        <div
          :class="index==maxLength-1?'timeLinelineEnd':'timeLineline'"
          v-bind:style="{ backgroundColor: lineColor }"
        ></div>
        <block v-if="saClass=='sa_timeClass_Dot'">
          <div class="contentContainer">
            <div class="timeLinecontent">{{obj.content}}</div>
            <div class="dividing_line"></div>
          </div>
        </block>
        <block v-else-if="saClass=='sa_timeClass_Number'">
          <div class="timeLinecontent">{{obj.content}}</div>
        </block>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  //   "state":''
  //   "title":''
  //   "content":''
  //   "index":''
  //   "id",:''
  //   "isSelect":''
  props: ["obj", "index", "maxLength", "lineColor", "saClass"]
};
</script>
<style>
.sa_timeClass_Number,.sa_timeClass_Dot  {
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
.style1_circle {
  width: 40rpx;
  height: 40rpx;
  color: #999999;
  background-color: white;
  border-radius: 50%;
  border: 2rpx solid rgba(53, 210, 250, 1);
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0rpx 0rpx 10rpx rgba(53, 210, 250, 1);
}
.sa_timeClass_Dot {
  display: flex;
  flex-direction: column;
}
.style1_circle_dot {
  width: 20rpx;
  height: 20rpx;
  background-color: rgba(53, 210, 250, 1);
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0rpx 0rpx 10rpx rgba(53, 210, 250, 1);
}
.style1_circle_dot_clean {
  width: 0rpx;
  height: 0rpx;
}
.sa_timeClass_Dot .timeLineline {
  width: 4rpx;
  background-color: rgba(53, 210, 250, 1);
  margin-left: 62rpx;
  margin-right: 44rpx;
  box-shadow: 0rpx 0rpx 10rpx rgba(53, 210, 250, 1);
}
.sa_timeClass_Dot .timeLinelineEnd {
  height: 0rpx;
  margin-left: 70rpx;
  margin-right: 40rpx;
}
.sa_timeClass_Dot .timeLinelineTitle {
  font-size: 30rpx;
  color: #363636;
  font-weight: 650;
  margin-left: 20rpx;
  margin-top: -10rpx;
}
.sa_timeClass_Dot .contentContainer {
  display: flex;
  flex-direction: column;
}
.dividing_line {
  margin-bottom: 20rpx;
  height: 2rpx;
  width: 600rpx;
  border: none;
  border-bottom: 2rpx dotted lightgray;
}
</style>
