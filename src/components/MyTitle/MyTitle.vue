<template>
      <div id="mytitle">
            <h2 :style="{fontSize: fontsize + 'px'}">{{title}}</h2>
            <slot></slot>
      </div>
</template>
<script>
export default {
      props:{
            title:{
                  type: String,
                  required: true
            },
            fontsize:{
                  type: Number,
                  default: 20
            }
      }
}
</script>
<style lang="less" scoped>
#mytitle{
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid rgba(255, 255, 255, 0.5);
      h2{
            
            padding: 10px 0;
            margin:0;
            color: #fff;
      }
}
</style>
