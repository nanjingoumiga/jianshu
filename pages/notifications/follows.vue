<template>
  <div style="height=100%">
    <my-header></my-header>
    <div class="container notification">
      <div class="row">
        <!-- 左边导航栏 -->
        <notifications></notifications>
        <!-- 右边内容部分 -->
        <div class="col-xs-16 col-xs-offset-8 main">
          <div>
            <div class="menu">全部关注</div>
            <ul class="follow-list">
              <div class="notification-list-placeholder">
                  <div class="avatar"></div>
                  <div class="wrap">
                      <div class="btn"></div>
                      <div class="name"></div>
                      <div class="text"></div>
                  </div>
                  <p></p>
                  <p class="animation-delay"></p>
                  <div class="meta"></div>
              </div>
            </ul>
            <div class="find-nothing">
                <img src="../../assets/img/no_follows.png" alt="">
                <div>这里还木有内容哦~</div>
            </div>
            <div></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import myHeader from "~/components/myHeader";
import notifications from "~/components/notifications";
export default {
  head: {
    title: "消息 - 简书",
    meta: [
      { charset: "utf-8" },
      { name: "keywords", content: "简书消息页" },
      { name: "description", content: "简书消息页" },
      { name: "author", content: "陈佳威" }
    ]
  },
  components: {
    myHeader,
    notifications
  },
  data() {
    return {
      name: "简书消息页"
    };
  }
};
</script>

<style scoped>
/*************** 左边导航栏 *********************/
@media (min-width: 992px) {
  .container {
    width: 960px;
  }
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 15px;
  padding-right: 15px;
}
.notification .row {
  padding: 30px 0;
}
.row {
  margin-left: -15px;
  margin-right: -15px;
}
.row:after {
  clear: both;
}
.row:after,
.row:before {
  content: " ";
  display: table;
}
/**************** 右边内容部分 *****************/
.notification .main{
  padding-left: 0;
}
.notification .main .menu{
  margin-bottom: 20px;
  font-size: 14px;
  font-weight: 700;
}
.notification .main ul{
  list-style: none;
  display: none;
}
ul{
  padding-left: 0;
}
ol,
ul{
  margin-top: 0;
  margin-bottom: 10px;
}
li{
  line-height: 20px;
}
.notification-list-placeholder{
  margin-top: -10px;
  padding: 10px 20px;
}
.notification .main .follow-list .avatar{
  display: inline-block;
  margin-right: 5px;
  width: 40px;
  height: 40px;
  display: none;
}
.notification-list-placeholder .avatar{
  position: absolute;
  cursor: default !important;
  margin-top: 20px;
  background-color: #eaeaea;
  border-radius: 50%;
}
.notification-list-placeholder .wrap {
    padding: 23px 20px 20px 72px!important;
    margin: 0 -20px;
    border-top: 1px solid #f0f0f0;
}
.notification .main .follow-list p{
    margin: 10px 0 0;
    font-size: 15px;
    line-height: 1.7;
}
.notification-list-placeholder p {
    display: none;
    margin-bottom: 10px;
    height: 15px;
    background-color: #eaeaea;
    animation: loading 1s ease-in-out infinite;
    -webkit-animation: loading 1s ease-in-out infinite;
    -moz-animation: loading 1s ease-in-out infinite;
    -o-animation: loading 1s ease-in-out infinite;
    -ms-animation: loading 1s ease-in-out infinite;
}
.notification .main .follow-list p{
    margin: 10px 0 0;
    font-size: 15px;
    line-height: 1.7;
}
.notification .main .follow-list .meta{
    margin-top: 10px;
    height: 20px;
}
.notification-list-placeholder .meta{
    display: none;
    margin: 0;
    padding-top: 6px;
    color: #eaeaea;
    font-size: 15px;
}
.notification-list-placeholder .meta i {
    margin-right: 5px;
    vertical-align: middle;
}
.notification-list-placeholder .meta .text {
    display: inline-block;
    vertical-align: middle;
    margin-right: 20px;
    height: 14px;
    width: 26px;
    background-color: #eaeaea;
}
.notification-list-placeholder .meta .text.longer {
    width: 56px;
}
.notification .main .find-nothing {
    margin-top: 90px;
    text-align: center;
}
.notification .main .find-nothing img {
    width: 100px;
}
img {
    vertical-align: middle;
}
img {
    border: 0;
}
.notification .main .find-nothing div {
    margin-top: 20px;
    font-size: 14px;
    font-weight: 700;
}
</style>
