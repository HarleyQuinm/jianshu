<template>
    <div>
        <nav class="navbar navbar-fixed-top">
            <div class="width-limit">
                <nuxt-link to="/" class="nav-logo">
                    <img src="~assets/img/navlogo.png" alt="">
                </nuxt-link> 
                <nuxt-link to="/" class="write-btn">
                    <i class="fa fa-">写文章</i>
                </nuxt-link>
                <!-- 登录用户信息 -->
                <div class="user" @mouseenter="Inuser()" @mouseleave="Outuser()">
                    <div class="drop-down">
                        <nuxt-link to="/u/123" class="avatar">
                            <img src="~assets/img/head.jpg" alt="">
                        </nuxt-link>
                    </div>
                    <ul class="drop-menu" v-if="isUser">
                        <li>
                            <nuxt-link to="/">
                                <i class=" fa fa-home fa-fw">                                   
                                </i>
                                我的主页
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/user/123/like">
                                <i class=" fa fa-heart fa-fw">                                    
                                </i>
                                喜欢的文章
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/bookmark">
                                <i class=" fa fa-bookmark fa-fw">                                   
                                </i>
                                收藏的文章
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/settint/basic">
                                <i class=" fa fa-cog fa-fw">                                   
                                </i>
                                设置
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/logout">
                                <i class=" fa fa-sign-out fa-fw">                                
                                </i>
                                退出
                            </nuxt-link>
                        </li>
                    </ul>
                </div> 
            </div>
        </nav>
    </div>
</template>
<script>
export default {
    name:'myHeader',
    data(){
        return {
            isUser:false,
        }
    },
    methods:{
        Inuser:function(){
            this.isUser=true
        },
        Outuser:function(){
            this.isUser=false;
        }
        
    }
}
</script>
<style scoped>
    nav {
        width: 100%;
        height: 56px;
    }
    .navbar {
        margin-bottom: 56px;
        border-bottom: 1px solid #f0f0f0;
    }
    navbar::before{
        content: '';
        display: table;
    }
    .navbar-fixed-top{
        position: fixed;
        left: 0;
        top: 0;
        z-index: 5;
    }
    nav .width-limit {
        min-width:768px;
        max-width: 1440px;
        margin: 0 auto;
    }
    nav .nav-logo{
        float: left;
        height: 56px;
    }
    nav .nav-logo img{
        height: 100%;
    }
    nav .write-btn{
        float: right;
        width: 100px;
        height: 40px;
        line-height: 40px;
        margin: 8px 15px 0;
        font-size: 15px;
        border-radius: 20px;
        font-size: 15px;
        color:#fff;
        background: #ea6f5a;
        text-align: center;
    }
    nav .write-btn:hover{
        background: rgb(236, 74, 93);
        cursor: pointer;
    }
    nav .user {
        position: relative;
        float: right;
    }
    nav .user .avatar{
        position: relative;
        display: block;
        float: right;
        width: 40px;
        height: 40px;
        margin: 8px 25px 8px 25px;
        display: inline-block;
        overflow: hidden;
        zoom: 1;
    }
    nav .user::after{
        content: '';
        clear: both;
    }

    nav .user:hover,nav .user .drop-menu li:hover{
        background: #f0f0f0;
    }
    nav .user .avatar::before{
        content: '';
        position: absolute;
        border-left: 5px solid transparent;
        border-right: 5px solid transparent;
        border-top: 5px solid #999;
        top: 18px;
        right: -14px;
    }
    nav .user .avatar img{
        width: 100%;
        height: 100%;
        border-radius: 50%;
        border: 1px solid #eee;
    }
  

    nav .user .drop-menu {
        position: absolute;
        left: 0;
        top: 56px;
        box-shadow: 0 0 8px rgba(0, 0, 0, .3);
        min-width: 160px;
        z-index: 4;
        margin: 0;
        padding: 10px 0;
    }
    nav .user .drop-menu li a{
        padding: 10px 20px ;
        display:block;  
    }
    nav .user .drop-menu li a i{
        margin-right: 15px;
        color: #ea6f5a;
        font-size: 18px;
    }
</style>


