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
            <div class="menu">收到的喜欢和赞</div>
            <ul class="like-list">
              <li>
                <nuxt-link to="/u/123" class="avatar">
                  <img src="../../assets/img/default-avatar.jpg" alt="">
                </nuxt-link>
                <div class="info">
                    <nuxt-link to="/u/123" class="user">
                       sky014
                    </nuxt-link>
                    <span>赞你的评论</span>
                    <nuxt-link to="/u/123" class="middle">
                      专业水军20年
                    </nuxt-link>
                    <div class="time">2018.04.25 16:46</div>
                </div>
              </li>
              <li>
                <nuxt-link to="/u/123" class="avatar">
                  <img src="../../assets/img/default-avatar.jpg" alt="">
                </nuxt-link>
                <div class="info">
                    <nuxt-link to="/u/123" class="user">
                      sky014
                    </nuxt-link>
                    <span>赞你的评论</span>
                    <nuxt-link to="/u/123" class="middle">
                      小礼物走一波~
                    </nuxt-link>
                    <div class="time">2018.04.25 16:46</div>
                </div>
              </li>
              <li>
                <nuxt-link to="/u/123" class="avatar">
                  <img src="../../assets/img/default-avatar.jpg" alt="">
                </nuxt-link>
                <div class="info">
                    <nuxt-link to="/u/123" class="user">
                      0缄默0
                    </nuxt-link>
                    <span>赞你的评论</span>
                    <nuxt-link to="/u/123" class="middle">
                      小礼物走一波~
                    </nuxt-link>
                    <div class="time">2018.04.25 16:39</div>
                </div>
              </li>
            </ul>
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
.notification .main {
  padding-left: 0;
}
.notification .main .menu {
  margin-bottom: 20px;
  font-size: 14px;
  font-weight: 700;
}
.notification .main ul {
  list-style: none;
}
ul {
  padding-left: 0;
}
ol,
ul {
  margin-top: 0;
  margin-bottom: 10px;
}
.notification .main .like-list li{
    padding: 20px;
    border-top: 1px solid #f0f0f0;
}
li {
  line-height: 20px;
}
.notification .main .like-list .avatar{
    display: inline-block;
    margin-right: 5px;
    width: 40px;
    height: 40px;
}
.avatar img {
    width: 100%;
    height: 100%;
    border: 1px solid #ddd;
    border-radius: 50%;
}
img {
    vertical-align: middle;
}
.notification .main .like-list .info{
    display: inline-block;
    vertical-align: top;
    width: 535px;
    font-size: 0;
    line-height: 1.7;
}
.notification .main .like-list .info .user{
    margin: 0 5px 0 0;
    color: #333;
}
.notification .main .like-list .info a{
    font-size: 15px;
}
.notification .main .like-list .info span{
    font-size: 15px;
}
.notification .main .like-list .info .middle{
    margin: 0 5px;
}
.notification .main .like-list .info a{
    font-size: 15px;
    color: #3194d0;
}
.notification .main .like-list .time{
    margin-top: 2px;
    font-size: 12px;
    color: #969696;
    line-height: normal;
}
.notification .main .like-list li{
    padding: 20px;
    border-top: 1px solid #f0f0f0;
}
.notification-list-placeholder {
    margin-top: -10px;
    padding: 10px 20px;
}
</style>