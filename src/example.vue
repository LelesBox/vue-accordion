<template>

<accordion :auto-shrink="true">
    <accordion-item title="1.SHIPPING">
      <div slot="header" class="header">
        <div class="title">1.CUSTOM ITEM HEADER</div>
        <svg class="icon" viewBox="0,0,22,22" v-show="!open">
        <path d="M 0 11 L 22 11" stroke-width="2" stroke="#5F5F5F"></path>
        <path d="M 11 0 L 11 22" stroke-width="2" stroke="#5F5F5F"></path>
        </svg>
        <svg class="icon" viewBox="0,0,22,22" v-show="open">
        <path d="M 0 11 L 22 11" stroke-width="2" stroke="#5F5F5F"></path>
        </svg>
      </div>
        <div style="height: 400px;width: 100%;background: yellow">
            asd
        </div>
        <div style="height: 400px;width: 100%;background: green">
            zxczxc
        </div>
    </accordion-item>
    <accordion-item title="2.BILLING">
        <div style="height: 400px;width: 100%;background: red">
            zxcz阿斯达xc
        </div>
    </accordion-item>
    <accordion-item title="3.REVIEW">
        <div style="height: 200px;width: 100%;background: red">
            zxczxllxlxlxlxlxlxl
        </div>
    </accordion-item>
    <accordion-item title="3.TEST">
        <div style="height: 400px;width: 100%;background: red">
            zxcz阿斯达xc
        </div>
    </accordion-item>
</accordion>

</template>

<script type="text/ecmascript-6">
require('../release/vue-accordion.css')
import { accordion, accordionItem } from '../release/vue-accordion'
export default {
  components: {
    accordion,
    accordionItem
  }
}
</script>

<style lang="scss">
.header {
  position: relative;
  width: 100%;
  background: white;
  height:150px;
  letter-spacing: 1px;
  z-index: 2;
  &:before {
      content: '';
      display: block;
      height: 1px;
      width: 100%;
      position: absolute;
      top: 0px;
      background-color: #d9d9d9;
  }
  &:after {
      content: '';
      display: block;
      height: 1px;
      width: 100%;
      position: absolute;
      bottom: -1px;
      background-color: #d9d9d9;
  }
}

.title {
  display: inline-block;
  margin-left: 10px;
  position: relative;
  top:50%;
  transform: translateY(-50%);
}

.icon {
  position: absolute;
  height: 15px;
  width: 15px;
  right: 15px;
  top: 50%;
  transform: translateY(-50%);
}
</style>
