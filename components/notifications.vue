<template>
  <div class="aside">
          <ul>
            <li>
              <nuxt-link to="/notifications/comments">
                <i class="fa fa-comment-o"></i>
                <span>评论</span>
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/notifications/chats">
                <i class="fa fa-envelope-o"></i>
                <span>简信</span>
                <span class="badge">1</span>
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/notifications/follows">
                 <i class="fa fa-plus-square-o"></i>
                <span>关注</span>
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/notifications/likes">
                <i class="fa fa-heart-o"></i>
                <span>喜欢和赞</span>
              </nuxt-link>
            </li>
          </ul>
        </div>
</template>

<script>
export default {
  name: "notifications",
  data() {
    return {
        
    };
  }
};
</script>

<style scoped>
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
</style>
