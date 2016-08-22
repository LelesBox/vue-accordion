<template>
<accordion :auto-shrink="true">
    <accordion-item :title="menu.title" v-for="menu in menus" :icon-hide="menu.subtitle.length===0">
        <div v-for="sub in menu.subtitle" style="height:50px;line-height:50px;margin-left:70px;">
          {{sub.title}}
        </div>
    </accordion-item>
</accordion>
</template>

<script type="text/ecmascript-6">
require('../release/vue-accordion.css')
// import { accordion, accordionItem } from '../release/vue-accordion'
import { accordion, accordionItem } from '.'
export default {
  data: function () {
    return {
      menus: [
        {
          title: 'DASHBOARD',
          subtitle: [
            {
              title: 'A'
            },
            {
              title: 'B'
            },
            {
              title: 'C'
            }
          ]
        },
        {
          title: 'CHALLENGES',
          subtitle: [
            {
              title: 'My Challenge'
            },
            {
              title: 'All Challenge'
            },
            {
              title: 'Find Challenge'
            },
            {
              title: 'Create A Challenge'
            }
          ]
        },
        {
          title: 'ANALYSIS',
          subtitle: []
        }
      ]
    }
  },
  components: {
    accordion,
    accordionItem
  }
}
</script>

<style lang="scss">
body{
   
}

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
