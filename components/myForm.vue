<template>
    <div>
        <form class="new-comment" method="post">
            <slot></slot>
            <textarea name="comment-content" placeholder="写下你的评论"  v-model="value"></textarea>
            <div class="write-function-block">
                <div class="emoji-modal-wrap">
                    <a href="javascript:" @click="isShow=!isShow" class="emoji-a">
                        <i class="fa fa-smile-o"></i>
                    </a>
                    <div class="emoji-modal"></div>
                </div>
                <div class="hint">Ctrl+Enter发送</div>
                <a href="#" class="btn-send">发送</a>
                <a href="#" class="btn-cancel">取消</a>
            </div>
            <emoji v-show="isShow" @select="selectEmoji"></emoji>
        </form>
    </div>
</template>

<script>
import emoji from "../components/emoji";
export default {
  name: "myForm",
  data() {
    return {  
      isShow: false,
      value: "",
    };
  },
  components: {
    emoji
  },
  methods: {
    selectEmoji(code) {
      this.showEmoji = false;
      this.value += code;
    }
  }
};
</script>