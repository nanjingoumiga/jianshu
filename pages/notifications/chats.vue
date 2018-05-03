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
            <div class="menu">全部简信</div>
            <ul class="jianxin-list">
              <li>
                <div class="pull-right">
                    <span class="time">
                        04.26 21:09
                    </span>
                    <div>
                        <a href="">
                            <i class="fa fa-chevron-down"></i>
                        </a>
                        <ul class="dropdown-menu">
                            <li>
                                <a href="">
                                    <i class="fa fa-trash-o"></i>
                                    删除会话
                                </a>
                            </li>
                            <li>
                                <a href="">
                                    <i class="fa fa-ban"></i>
                                    加入黑名单
                                </a>
                            </li>
                            <li>
                                <a href="">
                                    <i class="fa fa-exclamation"></i>
                                    举报用户
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
                <nuxt-link to="/u/123" class="avatar">
                  <img src="../../assets/img/default-avatar.jpg" alt="">
                </nuxt-link>
                <nuxt-link to="/u/123" class="name">
                  茶点故事
                </nuxt-link>
                <nuxt-link to="/u/123" class="wrap">
                  <p>Hi，很高兴能够跟你一起开启简书历史上最特别的篇章 “423简书故事节”。来看看我们为你准备的...</p>
                </nuxt-link>
              </li>
              <li>
                <div class="pull-right">
                    <span class="time">
                        04.20 16:30
                    </span>
                    <div>
                        <a href="">
                            <i class="fa fa-chevron-down"></i>
                        </a>
                        <ul class="dropdown-menu">
                            <li>
                                <a href="">
                                    <i class="fa fa-trash-o"></i>
                                    删除会话
                                </a>
                            </li>
                            <li>
                                <a href="">
                                    <i class="fa fa-ban"></i>
                                    加入黑名单
                                </a>
                            </li>
                            <li>
                                <a href="">
                                    <i class="fa fa-exclamation"></i>
                                    举报用户
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
                <nuxt-link to="/u/123" class="avatar">
                  <img src="../../assets/img/default-avatar.jpg" alt="">
                </nuxt-link>
                <nuxt-link to="/u/123" class="name">
                  简宝玉
                </nuxt-link>
                <nuxt-link to="/u/123" class="wrap">
                  <p>欢迎加入丰富多彩的原创内容社区—简书。新手有关简书的任何疑问请点击链接查看 http://w...</p>
                </nuxt-link>
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
li {
  line-height: 20px;
  display: list-item;
  text-align: -webkit-match-parent;
}
.notification .main .jianxin-list li {
    position: relative;
    border-top: 1px solid #f0f0f0;
}
.notification .main .jianxin-list .pull-right {
    margin: 20px 20px 0 0;
    font-size: 13px;
    visibility: hidden;
}
.pull-right {
    float: right!important;
}
.notification .main .jianxin-list .pull-right .time {
    color: #9b9b9b;
}
.notification .main .jianxin-list .pull-right {
    margin: 20px 20px 0 0;
    font-size: 13px;
}
.notification .main .jianxin-list .pull-right div {
    display: inline;
}
.notification .main .jianxin-list .avatar {
    float: left;
    margin: 20px 10px 20px 20px;
    width: 48px;
    height: 48px;
}
.avatar {
    width: 32px;
    height: 32px;
    display: block;
    cursor: pointer;
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
.notification .main .jianxin-list .name {
    position: absolute;
    top: 25px;
    font-size: 15px;
}
.notification .main .jianxin-list .wrap {
    display: block;
    padding: 20px 20px 20px 0;
    min-height: 88px;
}
.notification .main .jianxin-list p {
    margin: 28px 0 0;
    font-size: 12px;
    color: #999;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}
p {
    margin: 0 0 10px;
}
</style>
