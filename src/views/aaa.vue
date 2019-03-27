<template>
    <div>
        <img :src="imgUrl" alt="" @click='changeImg'>
    </div>
</template>
<script>
export default {
    data(){
        return{
            imgArr :[require('../assets/001.jpg'),require('../assets/002.jpeg'),require('../assets/003.jpg'),require('../assets/004.jpg'),require('../assets/005.jpeg'),require('../assets/006.png')],
            imgUrl:''
        }
    },
    created(){
        this.imgUrl = this.imgArr[0]
    },
    methods:{
        changeImg(){
            let idx = parseInt(Math.random()*10)%(this.imgArr.length)
            this.imgUrl  = this.imgArr[idx]
        }
    }
}
</script>
<style lang="stylus" scoped>
img 
    width 200px
    cursor pointer
</style>


