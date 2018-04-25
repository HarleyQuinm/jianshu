<template>
    <div>
        <my-header></my-header>
        <div class="note">
            <div class="post">
                <!-- 文章正文 -->
                <div class="article">
                    <h1 class="title">观记《解忧杂货》</h1>
                    <div class="author">
                        <div class="avatar">
                            <img src="~assets/img/head.jpg" alt="">
                        </div>
                        <div class="info">
                            <nuxt-link class="name" to="name">秘名</nuxt-link>
                            <a href="#" class="btn btn-follow">
                                <i class="fa fa-plus"></i>
                                <span>关注</span>
                            </a>
                            <div class="meta">
                                <span class="publish-time">
                                    2018.01 21:09
                                </span>
                                <span class="wordage">
                                    字数 1038
                                </span>
                                <span class="view-count">
                                    阅读 12
                                </span>
                                <span class="comment-count">
                                    评论 0
                                </span>
                                <span class="likes-count">
                                    喜欢 27
                                </span>
                            </div>
                        </div>
                    </div>
                    <!-- 底部版权 -->
                    <div class="show-content">
                        <div></div>
                    </div>                  
                </div>
                <div class="show-foot">
                       <nuxt-link to="/note/123" class="notebook">
                            <i class="fa fa-book"></i>
                            日记本
                        </nuxt-link> 
                        <div class="copyright">
                            &copy; 著作版权归作者所有
                        </div>
                 </div>
                 <!-- 底部作者信息 -->
                 <div class="follow-detail">
                     <div class="info">
                         <div class="avatar">
                             <img src="~assets/img/head.jpg" alt="">
                         </div>
                         <a href="#" class="btn-follow">
                             <i class="fa fa-plus"></i>
                             <span>关注</span>
                         </a>
                         <nuxt-link class="title" to="/u/123">
                            秘名
                         </nuxt-link>
                         <i class="fa fa-venus"></i>
                         <p>
                             写了12886字，被22人关注，获得了102个喜欢
                         </p>
                     </div>
                 </div>
                 <!-- 更多分享 -->
                 <div class="meta-bottom">
                     <div class="like">
                         <div class="like-btn">
                             <a href="#" class="">喜欢</a>
                         </div>
                         <div class="like-num">
                             <a href="#">50</a>
                         </div>
                     </div>
                     <div class="share">
                         <a href="#" class="share-btn">
                             <i class="fa fa-weixin weixin"></i>
                         </a>
                         <a href="#" class="share-btn">
                             <i class="fa fa-weibo weibo"></i>
                         </a>
                         <a href="#" class="share-btn">
                             <i class="fa fa-qq qq"></i>
                         </a>
                         <a href="#" class="share-btn more-share">
                             更多分享
                         </a>
                     </div>
                 </div>
            </div>
        </div>
    </div>
</template>
<script>
import myHeader from '~/components/myHeader'
export default {
    head:{
        title:'简书文章详情页面-创作你的创作',
        meta:[
            {charset:'utf-8'},
            {name:'keywards',content:'文章详情页'},
            {name:'description',content:'文章页面'},
        ]
    },
    components:{
        myHeader,
    },
    data(){
        return {

        }
    }
}
</script>

