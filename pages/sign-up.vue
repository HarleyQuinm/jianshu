<template>
    <div class="sign">
        <div class="logo">
            <nuxt-link to="/">
                <img src="~/assets/img/jianshu-logo.png" alt="">
            </nuxt-link>
        </div>
         <!-- 主体部分 -->
        <div class="main">
            <!-- title -->
            <div class="title">
                <h4>
                    <nuxt-link  to="/sign-in">
                        登录
                    </nuxt-link>
                    <big>·</big>
                    <nuxt-link class="active" to="/sign-up">
                        注册
                    </nuxt-link>
                </h4>
            </div>
            <!-- form表单 -->
            <div class="js-form">
                <form method="post">
                    <div class="input-prepend">
                        <input type="text" placeholder="你的昵称">
                        <i class="fa fa-user"></i>
                    </div>
                    <div class="input-prepend">
                        <input type="phone"  placeholder="你的手机号">
                        <i class="fa fa-phone"></i>
                    </div>
                    <div class="input-prepend ssm">
                        <input type="text" placeholder="手机验证码">
                        <i class="fa fa-shield"></i>
                        <div class="send">
                            <a href="">发送验证码</a>
                        </div> 
                    </div>
                    <div class="input-prepend">
                        <input type="password" placeholder="设置密码">
                        <i class="fa fa-lock"></i>
                    </div>
                    <button type="button" class="sign-up-btn" >注册</button>
                    <p class="sign-up-msg">点击 “注册” 即表示您同意并愿意遵守简书<span>用户协议</span>和 <span>隐私政策</span></p>
                </form>
            </div>
            <!-- 第三方登录 -->
            <div class="more-sign">
                <p class="">社交账号直接注册</p>
                <ul>
                    <li class="weixin">
                        <nuxt-link to="/">
                            <i class="fa fa-weixin"></i>
                        </nuxt-link>
                    </li>
                    <li class="qq">
                        <nuxt-link to="/">
                            <i class="fa fa-qq"></i>
                        </nuxt-link>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    layout:'sign',
    head:{
        title:'注册-简书',
        meta:[
            {charset:'utf-8'},
            {name:'keywords',content:'注册页面'},
            {name:'description',content:'注册简书'},
            {name:'authoe',content:'孙路怡'},

        ]
    },
    data () {
        return {

        }
    }
}
</script>
<style scoped>

</style>


