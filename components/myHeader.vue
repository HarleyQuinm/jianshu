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
                <!-- 右上角，登录和注册 -->
                <!-- 导航部分 -->
                <div class="container">
                    <ul class="nav-list">
                        <li >
                            <nuxt-link to="/" class="active">
                                <i class="fa fa-compass"></i>
                                <span>发现</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/follow">
                                <i class="fa fa-book"></i>
                                <span>关注</span>
                            </nuxt-link>
                        </li>
                        <li class="user" @mouseenter="Inmsg()" @mouseleave="Outmsg()">
                            <nuxt-link to="/notify">
                                <i class="fa fa-bell-o"></i>
                                <span>消息</span>
                            </nuxt-link>
                            <ul class="drop-menu" v-if="isMsg">
                                <li>
                                    <nuxt-link to="/">
                                        <i class="fa fa-comment-o"></i>
                                        <span>评论</span>
                                    </nuxt-link>
                                </li>
                                 <li>
                                    <nuxt-link to="/">
                                        <i class="fa fa-envelope-o"></i>
                                        <span>简信</span>
                                    </nuxt-link>
                                </li>
                                 <li>
                                    <nuxt-link to="/">
                                        <i class="fa fa-heart-o"></i>
                                        <span>喜欢和赞</span>
                                    </nuxt-link>
                                </li>
                                 <li>
                                    <nuxt-link to="/">
                                        <i class="fa fa-plus-square-o"></i>
                                        <span>关注</span>
                                    </nuxt-link>
                                </li>
                            </ul>
                        </li>
                        <li class="search">
                            <form method="post">
                                <input type="text" placeholder="搜索" class="search-input">
                                <a href="#" class="search-btn">
                                    <i class="fa fa-search"></i>
                                </a>
                            </form>
                        </li>
                    </ul>
                </div>
                <div class="menu-btn">
                    <div @click="clickMenu()">
                        <span class="fa fa-bars"></span>
                    </div>
                    <ul class="menu-btn-list" >
                        <li>
                            <nuxt-link to="/" >
                            <span class="active">发现</span>     
                            </nuxt-link>                      
                        </li>
                        <li>
                            <nuxt-link to="/">
                                <span>关注</span>
                            </nuxt-link> 
                        </li>
                        <li>
                            <nuxt-link to="/">
                               <span>消息</span>
                            </nuxt-link> 
                        </li>
                        <li class="search">
                            <form method="post">
                                <input type="text" placeholder="搜索" class="search-input">
                                    <a href="#" class="search-btn">
                                        <i class="fa fa-search"></i>
                                    </a>
                            </form>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </div>
</template>
<script>
export default {
  name: "myHeader",
  data() {
    return {
      clickMenuCount:0,
      isUser: false,
      isMsg: false,
      isClickMenu:false,
    };
  },
  methods: {
    Inuser: function() {
      this.isUser = true;
    },
    Outuser: function() {
      this.isUser = false;
    },
    Inmsg: function() {
      this.isMsg = true;
    },
    Outmsg: function() {
      this.isMsg = false;
    },
    clickMenu:function(){
        this.clickMenuCount++;
        var list = document.querySelector('.menu-btn-list');
        console.log(list)
        if(this.clickMenuCount%2==0){
            list.style.height='0'
            this.isClickMenu=false;
        }else {
            this.isClickMenu=true;
            list.style.height='260px'
        }
    }
  }
};
</script>
<style scoped>
nav {
  width: 100%;
  height: 56px;
}
.navbar {
  position: relative;
  margin-bottom: 56px;
  border-bottom: 1px solid #f0f0f0;
  background: white;
}
navbar::before {
  content: "";
  display: table;
}
.navbar-fixed-top {
  position: fixed;
  left: 0;
  top: 0;
  z-index: 5;
}
nav .width-limit {
  min-width: 768px;
  max-width: 1440px;
  margin: 0 auto;
}
nav .nav-logo {
  float: left;
  height: 56px;
}
nav .nav-logo img {
  height: 100%;
}
nav .write-btn {
  float: right;
  width: 100px;
  height: 40px;
  line-height: 40px;
  margin: 8px 15px 0;
  font-size: 15px;
  border-radius: 20px;
  font-size: 15px;
  color: #fff;
  background: #ea6f5a;
  text-align: center;
}
nav .write-btn:hover {
  background: rgb(236, 74, 93);
  cursor: pointer;
}
nav .user {
  position: relative;
  float: right;
}
nav .user .avatar {
  position: relative;
  display: block;
  width: 40px;
  height: 40px;
  margin: 8px 25px 8px 25px;
  display: inline-block;
}
nav .user:hover,
nav .user .drop-menu li:hover {
  background: #f0f0f0;
}
nav .user .avatar::before {
  content: "";
  position: absolute;
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: 5px solid #999;
  top: 18px;
  right: -14px;
}
nav .user .avatar img {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  border: 1px solid #eee;
}

nav .user .drop-menu {
  background: white;
  position: absolute;
  left: 0;
  top: 56px;
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.3);
  min-width: 160px;
  z-index: 4;
  margin: 0;
  padding: 10px 0;
}
nav .user .drop-menu li a {
  padding: 10px 20px;
  display: block;
}
nav .user .drop-menu li a i {
  margin-right: 15px;
  color: #ea6f5a;
  font-size: 18px;
}
nav .nav-list::after {
  content: "";
  height: 0;
  display: block;
  visibility: hidden;
  clear: both;
}

nav .nav-list > li {
  float: left;
  margin-right: 5px;
}
nav .nav-list > li a {
  display: block;
  height: 56px;
  line-height: 26px;
  padding: 15px;
}
nav .nav-list > li a.active {
  color: #ea6f5a;
  background: none;
}
nav .nav-list > li a:hover {
  background: #f5f5f5;
}
nav .nav-list > li a i {
  font-size: 20px;
  margin-right: 5px;
}
nav  .search {
  padding-left: 15px;
  margin-right: 10px;
}
nav  .search form {
  position: relative;
  margin-bottom: 20px;
  top: 9px;
}
nav  .search form .search-input {
  width: 240px;
  height: 38px;
  font-size: 14px;
  padding: 0 40px 0 20px;
  border: 1px solid #eee;
  background: #eee;
  border-radius: 40px;
  transition: width 0.5s;
}
nav .nav-list .search form .search-input:focus {
  width: 320px;
}
nav  .search form .search-input:focus ~ .search-btn {
  background: #969696;
  color: white;
  border-radius: 50%;
}
nav .search form .search-btn {
  position: absolute;
  width: 30px;
  height: 30px;
  top: 4px;
  right: 5px;
  color: #969696;
  text-align: center;
  padding: 0;
  /* display:inline-block; */
}
nav .search form .search-btn:hover {
  background: none;
}

nav .search form .search-btn i {
  margin: 0;
  text-align: center;
  line-height: 30px;
  font-size: 15px;
  display: block !important;
}
nav .menu-btn {
    height: 56px;
    padding-top: 10px;
    
}
nav .menu-btn div>span{
    width: 44px;
    height: 38px;
    line-height: 56px;
    border:1px solid #eee;
    border-radius: 5px;
    text-align: center;
    padding: 0;
}
nav .menu-btn div>span:hover{
    background: rgb(248, 246, 246);
    cursor: pointer;
}
nav .menu-btn div>span{
    color: #969696;
    line-height: 38px;
    font-size: 22px; 
}

nav .menu-btn .menu-btn-list{
    background: white;
    overflow: hidden;
    height: 0;
    position: absolute;
    top: 57px;
    width: 100%;
    text-align: center;
    margin-top: 5px;
    transition: height 0.5s;
}
nav .menu-btn .menu-btn-list li{
    padding: 15px;
    border-bottom: 1px solid #f0f0f0;
}
nav .menu-btn .menu-btn-list li:hover{
    cursor: pointer;
    
}
nav .menu-btn .menu-btn-list li:nth-of-type(2):hover,nav .menu-btn .menu-btn-list li:nth-of-type(3):hover{
    background: #f5f5f5;
}
nav .menu-btn .menu-btn-list li span.active{
    color: #ea6f5a
}
nav .menu-btn .menu-btn-list li span{
    /* padding: 15px; */
    line-height: 25px;
    font-size: 17px;
}
nav .menu-btn-list form .search-input{
    transition: width .5s;
    width: 2240px;
}




@media (max-width: 1440px) {
  nav .nav-list > li a i {
    display: none;
  }
  nav .nav-list .search form .search-input {
    width: 160px;
  }
  nav .nav-list .search form .search-input:focus {
    width: 240px;
  }
  nav .menu-btn{
      display: none;
  }

}

@media (max-width: 1080px) {
  nav .nav-list li span {
    display: none;
  }
  nav .nav-list > li a i {
    display: block;
  }
  nav .menu-btn{
      display: none;
  }
}
@media (max-width: 768px) {
  nav .nav-list {
    display: none;
  }
  nav .menu-btn{
      display: block;
  }
  /* nav .menu-btn>.menu-btn-list{
    height:250px ;
  } */
  nav .menu-btn-list form .search-input {
      width: 100%;
  }
}
</style>


