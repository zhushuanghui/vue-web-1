<!--
 * @Author: your name
 * @Date: 2020-04-10 11:22:32
 * @LastEditTime: 2020-04-10 11:24:22
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /tt/web/src/views/Messages.vue
 -->

<template>
  <div class="messages">
    <div class="banner" :style="bg">
      <!-- <img :src="banner" alt=""> -->
    </div>
    <section class="content">
      <contentslot>
        <span slot="title">在线留言</span>
        <article slot="article">
          this is message
        </article>
      </contentslot>
    </section>
  </div>
</template>
<script>
import contentslot from '@/components/Content.vue';

export default {
  name:'message',
  data(){
    return{
      bg: {
        backgroundImage: "url(" + require("../assets/images/about.jpg") + ")",
        backgroundRepeat: "no-repeat",
        backgroundSize: "cover"
      }
    }
  },
  components:{
    contentslot
  }
}
</script>
<style lang="less" scope>
  .banner{
    width: 100%;
    height: 380px;
    // overflow: hidden;
  }
  .flex{
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .content{
    width: 70%;
    margin: 0 auto;
    padding: 40px 0;
  }
  .article{
    flex: 1;
  }
</style>
