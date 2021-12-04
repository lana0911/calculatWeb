<template lang="pug">
#navBar
  span  TSET
  el-icon.i-switch
  el-icon       
    info()
  span.icon-home
  .navBar   
    el-radio-group(v-model="isCollapse" style='margin-bottom: 20px')
      el-radio-button(:label='false') expand
      el-radio-button(:label='true') collapse
    el-menu.el-menu-vertical-demo(
      default-active='2' 
      :collapse='isCollapse' 
      @open='handleOpen' 
      @close='handleClose'
    )
      el-sub-menu(index='1')
        template(#title)
          i.icon-calculator
          span &ensp;基本數學
        el-menu-item-group
          template(#title)
            span Group One
          el-menu-item(index='1-1') item one
          el-menu-item(index='1-2') item two
        el-menu-item-group(title='Group Two')
          el-menu-item(index='1-3') item three
        el-sub-menu(index='1-4')
          template(#title)
            span item four
          el-menu-item(index='1-4-1') item one


      el-sub-menu(index='2')
        template(#title)
          i.icon-heart
          span &ensp;健康
        el-menu-item-group
          template(#title)
            span Group One
          el-menu-item(index='1-1') item one
          el-menu-item(index='1-2') item two
        el-menu-item-group(title='Group Two')
          el-menu-item(index='1-3') item three
        el-sub-menu(index='1-4')
          template(#title)
            span item four
          el-menu-item(index='1-4-1') item one

          
      el-sub-menu(index='3')
        template(#title)
          i.icon-coin-dollar
          span &ensp;財經
        el-menu-item-group
          template(#title)
            span Group One
          el-menu-item(index='1-1') item one
          el-menu-item(index='1-2') item two
        el-menu-item-group(title='Group Two')
          el-menu-item(index='1-3') item three
        el-sub-menu(index='1-4')
          template(#title)
            span item four
          el-menu-item(index='1-4-1') item one

          
      el-sub-menu(index='4')
        template(#title)
          i.icon-text-color
          span &ensp;字數
        el-menu-item-group
          template(#title)
            span Group One
          el-menu-item(index='1-1') item one
          el-menu-item(index='1-2') item two
        el-menu-item-group(title='Group Two')
          el-menu-item(index='1-3') item three
        el-sub-menu(index='1-4')
          template(#title)
            span item four
          el-menu-item(index='1-4-1') item one

</template>

<script>
import { defineComponent, ref } from 'vue'


export default defineComponent({
  name: 'navBar',
  components: {

  },
  setup() {
    const isCollapse = ref(true)
    const handleOpen = (key, keyPath) => {
      console.log(key, keyPath)
    }
    const handleClose = (key, keyPath) => {
      console.log(key, keyPath)
    }
    return {
      isCollapse,
      handleOpen,
      handleClose,
    }
  },
})
</script>

<style>
.el-menu-vertical-demo:not(.el-menu--collapse) {
  width: 200px;
  min-height: 400px;
}
</style>