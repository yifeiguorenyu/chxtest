<template>
  <el-row :gutter="20" class="panel-group">
    <el-col :xs="12" :sm="12" :lg="7" class="card-panel-col">
      <div class="card-panel" @click="handleSetLineChartData('newVisitis')">
        <div class="card-panel-icon-wrapper icon-people">
          <svg-icon icon-class="distribution" class-name="card-panel-icon" />
        </div>
        <div class="card-panel-description" style="margin-right:0px;margin-top:10px;float: left;margin-left:5px">
          <div class="clearfix">
              <div class="card-panel-text" style="float:left;font-size:14px;margin-right:20px;">当日工单</div>
               <count-to :start-val="0" :end-val="500" :duration="2600" style="float:right"  class="card-panel-num"/>
          </div>
          <div class="clearfix">
              <div class="card-panel-text" style="float:left;font-size:14px;margin-right:20px;">已完成工单</div>
               <count-to :start-val="0" :end-val="320" :duration="2600" style="float:right" class="card-panel-num"/>
          </div>
            <div class="clearfix">
              <div class="card-panel-text" style="float:left;font-size:14px;margin-right:20px;">实时工单</div>
               <count-to :start-val="0" :end-val="25" :duration="2600" style="float:right"  class="card-panel-num"/>
          </div>
            <div class="clearfix">
              <div class="card-panel-text" style="float:left;margin-right:20px;">待完成工单</div>
               <count-to :start-val="0" :end-val="320" :duration="2600" style="float:right"  class="card-panel-num"/>
          </div>
        </div>
      </div>
    </el-col>
    <el-col :xs="12" :sm="12" :lg="7" class="card-panel-col">
      <div class="card-panel clearfix" @click="handleSetLineChartData('messages')" style="display:flex;">
        <div class="card-panel-icon-wrapper icon-message" style="height:88px;">
          <svg-icon icon-class="people" class-name="card-panel-icon" />
        </div>
        <div class="card-panel-description" style="margin-right:0px;margin-top:10px;float: left;margin-left:5px;flex:1">
          <div class="clearfix">
              <div class="card-panel-text" style="float:left;font-size:14px;margin-right:20px;">本站老人</div>
               <count-to :start-val="0" :end-val="800" :duration="2600" style="float:right;margin-right:20px;"  class="card-panel-num"/>
          </div>
          <div class="clearfix">
              <div class="card-panel-text" style="float:left;font-size:14px;margin-right:20px;">服务中老人</div>
               <count-to :start-val="0" :end-val="660" :duration="2600" style="float:right;margin-right:20px;" class="card-panel-num"/>
          </div>
            <div class="clearfix" style="display:flex;">
              <div style="flex:1;">
                 <div class="card-panel-text" style="font-size:14px;margin-bottom:0">2级</div>
               <count-to :start-val="0" :end-val="60" :duration="2600"   class="card-panel-num"/>
              </div>
             <div style="flex:1;">
                 <div class="card-panel-text" style="font-size:14px;margin-bottom:0">3级</div>
               <count-to :start-val="0" :end-val="60" :duration="2600"   class="card-panel-num"/>
              </div>
              <div style="flex:1;">
                 <div class="card-panel-text" style="font-size:14px;margin-bottom:0">4级</div>
               <count-to :start-val="0" :end-val="60" :duration="2600"   class="card-panel-num"/>
              </div>
              <div style="flex:1;">
                 <div class="card-panel-text" style="font-size:14px;margin-bottom:0">5级</div>
               <count-to :start-val="0" :end-val="60" :duration="2600"   class="card-panel-num"/>
              </div>
              <div style="flex:1;">
                 <div class="card-panel-text" style="font-size:14px;margin-bottom:0">6级</div>
               <count-to :start-val="0" :end-val="60" :duration="2600"   class="card-panel-num"/>
              </div>
          </div>
        </div>
      </div>
    </el-col>
    <el-col :xs="12" :sm="12" :lg="7" class="card-panel-col">
      <div class="card-panel" @click="handleSetLineChartData('purchases')" style="display:flex;">
        <div class="card-panel-icon-wrapper icon-money" style="height:88px;">
          <svg-icon icon-class="nurse" class-name="card-panel-icon" />
        </div>
        <div class="card-panel-description" style="margin-right:0px;margin-top:20px;float: left;margin-left:5px;flex:1">
          <div class="clearfix" style="margin-bottom:15px">
              <div class="card-panel-text" style="float:left;font-size:14px;">本站护理员</div>
               <count-to :start-val="0" :end-val="500" :duration="2600" style="float:right;margin-right:30px;"  class="card-panel-num"/>
          </div>
         <div class="clearfix" style="display:flex;">
              <div style="flex:1;">
                 <div class="card-panel-text" style="font-size:14px;margin-bottom:10px">健康照护</div>
               <count-to :start-val="0" :end-val="10" :duration="2600"   class="card-panel-num" style="text-align:center;display:block"/>
              </div>
             <div style="flex:1;">
                 <div class="card-panel-text" style="font-size:14px;margin-bottom:10px">医疗照护</div>
               <count-to :start-val="0" :end-val="25" :duration="2600"   class="card-panel-num" style="text-align:center;display:block"/>
              </div>
               <div style="flex:1;">
                 <div class="card-panel-text" style="font-size:14px;margin-bottom:10px">专业护士</div>
               <count-to :start-val="0" :end-val="5" :duration="2600"   class="card-panel-num" style="text-align:center;display:block"/>
              </div>
          </div>
        </div>
      </div>
    </el-col>
  </el-row>
</template>

<script>
import CountTo from "vue-count-to";

export default {
  components: {
    CountTo
  },
  methods: {
    handleSetLineChartData(type) {
      this.$emit("handleSetLineChartData", type);
    }
  }
};
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
.panel-group {
  margin-top: 18px;
  .card-panel-col {
    margin-bottom: 32px;
  }
  .card-panel {
    height: 130px;
    cursor: pointer;
    font-size: 12px;
    position: relative;
    overflow: hidden;
    color: #666;
    background: #fff;
    box-shadow: 4px 4px 40px rgba(0, 0, 0, 0.05);
    border-color: rgba(0, 0, 0, 0.05);
    &:hover {
      .card-panel-icon-wrapper {
        color: #fff;
      }
      .icon-people {
        background: #40c9c6;
      }
      .icon-message {
        background: #36a3f7;
      }
      .icon-money {
        background: #f4516c;
      }
      .icon-shopping {
        background: #34bfa3;
      }
    }
    .icon-distribution{
      color: #40c9c6;
    }
    .icon-people {
      color: #40c9c6;
    }
    .icon-message {
      color: #36a3f7;
    }
    .icon-money {
      color: #f4516c;
    }
    .icon-shopping {
      color: #34bfa3;
    }
    .card-panel-icon-wrapper {
      float: left;
      margin: 14px 0 0 14px;
      padding: 16px;
      transition: all 0.38s ease-out;
      border-radius: 6px;
    }
    .card-panel-icon {
      float: left;
      font-size: 48px;
    }
    .card-panel-description {
      float: right;
      font-weight: bold;
      margin: 26px;
      margin-left: 0px;
      .card-panel-text {
        line-height: 18px;
        color: rgba(0, 0, 0, 0.45);
        font-size: 16px;
        margin-bottom: 12px;
      }
      .card-panel-num {
        font-size: 16px;
      }
    }
  }
}
</style>
