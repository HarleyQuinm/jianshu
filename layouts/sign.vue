<template>
  <div id="sign-template">
    <nuxt/>
  </div>
</template>

<script>
import Vue from 'vue'
export default {

}
</script>
<style>
  .sign{
    height:100%;
    font-size: 14px;
    text-align: center;
    background-color: #f1f1f1;
    min-height: 750px;
  }
  .sign::before{
    content: "";
    display: inline-block;
    height: 85px;
    vertical-align: middle;
}
  .sign img{
    width: 100px;
    position: absolute;
    left: 50px;
    top: 50px;
  }
  .sign .main{
    width: 400px;
    margin: 60px 0 0;
    padding: 50px 50px 30px;
    background: #fff;
    border-radius: 4px;
    box-shadow: 0 0 8px rgba(0, 0, 0, .1);
    display: inline-block;
    vertical-align: middle;
  }
  .sign .main .title{
    margin: 0 auto 30px;
    color: #969696;
    font-size: 18px;
  }
  .sign .main h4 a{
    font-weight: 400;
    padding: 10px;
    color: #969696;
  }
  .sign .main h4 a.active{
    color: #ea6f5a;
    border-bottom: 2px solid #ea6f5a;
    font-weight: bold;
  }
  .sign .main h4 a:hover{
    border-bottom: 2px solid #ea6f5a;
    
  }
  .sign .main from {
    color: #969696;
    margin: 0 0 30px;
  }
  .sign .main form .input-prepend {
    position: relative;
    width: 100%;
  }
  .sign .main form .input-prepend input{
    width: 100%;
    height: 50px;
    border: 1px solid #c8c8c8;
    padding: 4px 12px 4px 30px;
    background-color: rgb(248, 248, 248);
    border-bottom: none;
  }
  .sign .main form .input-prepend:nth-of-type(1) input{
    border-radius: 4px 4px 0 0;
  }
  .sign .main form .input-prepend:nth-last-of-type(1) input{
    border-bottom: 1px solid #c8c8c8;
    border-radius: 0 0 4px 4px;
  }
  .sign .main form .input-prepend i {
    position: absolute;
    left: 10px;
    top: 15px;
    font-size: 20px;
    color: #969696
  }
  .sign .main form .ssm input{
    padding-right: 115px;
  }
  .sign .main form .ssm div{
    position: absolute;
    right: 10px;
    top:8px;
    background: #42c021;
    opacity: .5;
    padding: 6px 0;
    width: 100px;
    height:35px;
    border-radius: 35px;
  }
  .sign .main form .ssm div a{
    color: white;
  }


  .sign .main form .remember{
    float: left;
    margin: 20px 0;
  }
  .sign .main form .help {
    float: right;
    margin: 20px 0;
    color: #969696
  }
  .sign .main form .help:hover{
    color: #333
  }
  .sign .main form button{
    font-size: 18px;
    width: 100%;
    margin: 0 ;
    padding: 9px 18px;
    color: #fff;
    background: #3194d0;
    border: none;
    border-radius: 50px;
  }
  .sign .main form button:hover{
    background: #187cb7;
    cursor: pointer;
  }
.sign .main form button.sign-up-btn{
  margin-top: 20px;
  background: #42c021
}
.sign .main form button.sign-up-btn:hover{
  background: #192;
  
}
  .more-sign{
    margin-top: 50px;
  }
  .more-sign>p{
    color: #b8b8b8;
    font-size: 14px;
    position: relative;
  }
  .more-sign>p::before, .more-sign>p::after{
    content: '';
    width: 60px;
    border-bottom: 1px solid #b8b8b8;
    position: absolute;
    top: 10px;  
    }
  .more-sign>p::before{
    left: 30px;
  }
  .more-sign>p::after{
    right: 30px;
  }
  .more-sign ul{
    padding-left: 0;
  }
  .more-sign ul li{
    width: 50px;
    height: 50px;
    display: inline-block;
    margin-left: 10px;
  }
  .more-sign ul li:nth-of-type(-n+3) i{
    font-size: 25px;
  }
  .more-sign ul .weibo i{
    color: #e05244;
  }
  .more-sign ul .weixin i{
    color: rgb(6, 172, 6);
  }
  .more-sign ul .qq i{
    color: #3194d0;
  }

  .sign form .sign-up-msg{
    font-size: 12px;
    color: #969696;
    text-align: center;
    margin: 15px 0;
    line-height: 20px;
    padding: 0 35px;
  }
  .sign form .sign-up-msg span{
    color: #3194d0;
  }

  @media screen and (max-width:768px) {
   .sign{
      background: white;
    }
    .sign::before{
      height: 0;
      content:none;
    }
    .sign .logo{
      display: none;
    }
    .sign .main{
      margin-top:20px; 
      border: none;
      box-shadow: none;
    }
  }

</style>
