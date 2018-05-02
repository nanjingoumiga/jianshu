<template>
  <div style="height=100%">
    <my-header></my-header>
    <div class="container notification">
      <div class="row">
        <!-- 左边导航栏 -->
        <div class="aside">
          <ul>
            <li>
              <a href="">
                <i class="fa fa-comment-o"></i>
                <span>评论</span>
              </a>
            </li>
            <li>
              <a href="">
                <i class="fa fa-envelope-o"></i>
                <span>简信</span>
                <span class="badge">1</span>
              </a>
            </li>
            <li>
              <a href="">
                <i class="fa fa-upload"></i>
                <span>投稿请求</span>
              </a>
            </li>
            <li>
              <a href="">
                <i class="fa fa-heart-o"></i>
                <span>喜欢和赞</span>
              </a>
            </li>
            <li>
              <a href="">
                <i class="fa fa-book"></i>
                <span>关注</span>
              </a>
            </li>
            <li>
              <a href="">
                  <i class="fa fa-thumbs-o-up"></i>
                <span>赞赏和付费</span>
              </a>
            </li>
            <li>
              <a href="">
                <i class="fa fa-ellipsis-h"></i>
                <span>其他提醒</span>
              </a>
            </li>
          </ul>
        </div>
        <!-- 右边内容部分 -->
        <div class="col-xs-16 col-xs-offset-8 main">
          <div>
            <div class="menu">收到的评论</div>
            <ul class="comment-list">
              <li>
                <nuxt-link to="/u/123" class="avatar">
                  <img src="../assets/img/default-avatar.jpg" alt="">
                </nuxt-link>
                <div class="info">
                  <div>
                    <nuxt-link to="u/123" class="user">
                      测试用户
                    </nuxt-link>
                    <span class="comment-slogan">
                      在文章
                    </span>
                    <nuxt-link to="u/123">
                      《今天天气不错》
                    </nuxt-link>
                    <span class="comment-slogan">
                      中写了一条新评论
                    </span>
                  </div>
                  <div class="time">
                    2018.04.25 16:45
                  </div>
                </div>
                <p>日发放人防</p>
                <div class="meta">
                  <nuxt-link to="/u/123" class="function-btn">
                    <i class="fa fa-comment-o"></i>
                    <span>回复</span>
                  </nuxt-link>
                  <nuxt-link to="/u/123" class="function-btn">
                    <i class="fa fa-mail-forward"></i> 
                    <span>查看对话</span>
                  </nuxt-link>
                  <nuxt-link to="/u/123" class="report">
                    <span>举报</span>
                  </nuxt-link>
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
export default {
  head: {
    title: "消息 - 简书",
    meta: [
      { charset: "utf-8" },
      { name: "keywords", content: "评论页" },
      { name: "description", content: "评论页" },
      { name: "author", content: "陈佳威" }
    ]
  },
  components: {
    myHeader
  },
  data() {
    return {
      name: "评论页"
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
.notification .aside {
  position: fixed;
  top: 0;
  bottom: 0;
  margin: 86px 0 0;
  padding: 0 0 30px;
  width: 280px;
  overflow: auto;
}
.notification .aside ul {
  padding-left: 0;
  list-style: none;
}
.notification .aside ul li {
  margin: 0;
  line-height: 20px;
}
.notification .aside ul li.active a {
  background-color: #f0f0f0;
  border-radius: 4px;
}
.notification .aside ul a:hover {
  background-color: #f0f0f0;
  border-radius: 4px;
}
.notification .aside ul a {
  height: auto;
  padding: 10px 25px;
  line-height: 30px;
  display: block;
}
.notification .aside ul i {
  margin: 0 15px 0 15px;
  font-size: 24px;
  color: #ea6f5a;
  vertical-align: middle;
}
.notification .aside ul span {
  font-size: 15px;
  vertical-align: middle;
}
.notification .aside ul .badge {
  float: right;
  margin-top: 7px;
}
.badge {
  padding: 3px 6px;
  font-size: 13px !important;
  background-color: #ea6f5a;
  display: inline-block;
  min-width: 10px;
  font-weight: 700;
  color: #fff;
  line-height: 1;
  white-space: nowrap;
  text-align: center;
  border-radius: 10px;
}
a:focus {
  outline: none;
}
a:focus,
a:hover {
  color: #2f2f2f;
  text-decoration: none;
}
a {
  cursor: pointer;
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
.notification .main .comment-list li {
  padding: 20px;
  border-top: 1px solid #f0f0f0;
}
li {
  line-height: 20px;
}
.notification .main .comment-list .avatar {
  display: inline-block;
  margin-right: 5px;
  width: 40px;
  height: 40px;
}
.avatar {
  cursor: pointer;
  width: 32px;
  height: 32px;
  display: block;
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
.notification .main .comment-list .info {
  display: inline-block;
  vertical-align: top;
  width: 535px;
  font-size: 0;
  line-height: 1.7;
}
.notification .main .comment-list .info .user {
  margin: 0 5px 0 0;
  color: #333;
}
.notification .main .comment-list .info a {
  font-size: 15px;
  color: #3194d0;
}
.comment-list .info,
.notification .main .follow-list .info {
  display: inline-block;
  vertical-align: top;
  width: 535px;
  font-size: 0;
  line-height: 1.7;
}
.notification .main .comment-list .info .comment-slogan {
  font-size: 15px;
  color: #333;
}
.notification .main .comment-list .info {
  display: inline-block;
  vertical-align: top;
  width: 535px;
  font-size: 0;
  line-height: 1.7;
}
.notification .main .comment-list .info a {
  font-size: 15px;
  color: #3194d0;
}
.notification .main .comment-list .info .comment-slogan {
  font-size: 15px;
  color: #333;
}
.notification .main .comment-list .info span {
  font-size: 15px;
}
.notification .main .comment-list .info {
  display: inline-block;
  vertical-align: top;
  width: 535px;
  font-size: 0;
  line-height: 1.7;
}
.notification .main .comment-list .time {
  margin-top: 2px;
  font-size: 12px;
  color: #969696;
  line-height: normal;
}
.notification .main .comment-list p {
  margin: 10px 0 0;
  font-size: 15px;
  line-height: 1.7;
}
li {
  line-height: 20px;
}
p {
  margin: 0 0 10px;
}
.notification .main .comment-list .meta {
  margin-top: 10px;
  height: 20px;
}
.notification .main .comment-list .meta .function-btn {
  float: left;
  margin-right: 30px;
  font-size: 13px;
  color: #969696;
}
.notification .main .comment-list .meta .function-btn i {
  margin-right: 5px;
  font-size: 15px;
  vertical-align: middle;
}
.notification .main .comment-list .meta .function-btn {
  float: left;
  margin-right: 30px;
  font-size: 13px;
  color: #969696;
}
.notification .main .comment-list .meta .function-btn span {
  vertical-align: middle;
}
.notification .main .comment-list .meta .report {
  float: right;
  font-size: 13px;
  color: #969696;
  display: none;
}
</style>
