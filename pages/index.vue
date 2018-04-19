<template>
    <div>
        <my-header></my-header>
        我的主页内容部分
    </div>
</template>
<script>
import myHeader from '../components/myHeader'
export default {
    head:{
        title:'简书-创作你的创作',
        meta:[
            {charset:'utf-8'},
            {name:'keywards',content:'简书首页'},
            {name:'description',content:'简书首页'},
            {name:'authoe',content:'孙路怡'},
        ]
    },
    components:{
        myHeader,
    },
    data(){
        return {
            name :'首页'
        }
    }
}
</script>
<style>

</style>


