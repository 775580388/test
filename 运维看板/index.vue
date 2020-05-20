<template>
  <div class="container">
    <!-- <div class="box" id="lottie_box"></div> -->
    <div class="box" id="lottie_box2"></div>
    <button @click="startFun">播放</button>   
    <button @click="suspendFun">暂停</button>   
  </div>
</template>

<script>

import lottie from 'lottie-web'

export default {

  name:'Lottie',
    data(){
        return{
            lottie:{},  
        }
    },
    methods:{
        suspendFun:function(){
            this.lottie.pause();
        },
        startFun:function(){
            this.lottie.play()
        }
    },
    mounted(){
        this.lottie = lottie.loadAnimation({
            container: document.getElementById('lottie_box2'),
            renderer: 'svg',
            autoplay: true,
            loop: true,
            path: 'https://assets8.lottiefiles.com/packages/lf20_jcM7b2.json'
        })
    }





  // data(){
  //   return{
  //     lottie:{}
  //   }
  // },
  // created(){
    
  // },
  // mounted(){
  //   this.loadAnimation()
  // },
  // methods: {
  //   loadAnimation(){
  //     this.lottie = lottie.loadAnimation({
  //       container: document.getElementById('lottie_box'), // Required
  //       path: 'https://assets4.lottiefiles.com/private_files/lf30_QzWg4W.json', // Required
  //       renderer: 'svg', // Required
  //       loop: true, // Optional
  //       autoplay: true, // Optional
  //       name: "Hello World", // 名称以供将来参考。 可选的。
  //     })
  //   },
  //   suspendFun:function(){
  //     this.lottie.pause();
  //   }, 
  //   startFun:function(){
  //     this.lottie.play()
  //   }  
  // }
}


</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.box{
  width: 300px;
  height: 300px;
}
</style>
