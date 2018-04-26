<template>
    <div id="sign-template">
        <nuxt/>
    </div>
</template>
<script>
    export default {

    }
</script>
<style>
    .sign {
        height:100%;
        font-size:14px;
        text-align:center;
        background-color:#f1f1f1;
        min-height:750px;
    }
    .sign:before {
        content: "";
        display: inline-block;
        height: 85%;
        vertical-align: middle;
    }
    .sign .logo {
        position:absolute;
        margin-left:50px;
        top:56px;
    }
    .sign img {
        width:100px;
    }
    .sign .main {
        width:400px;
        margin:60px auto 0;
        padding:50px 50px 30px;
        background:#fff;
        border-radius: 4px;
        box-shadow: 0 0 8px rgba(0,0,0,.1);
        display:inline-block;
        vertical-align: middle;
    }
    .sign .main .title {
        margin:0 auto 50px;
        color:#939393;
        font-size:18px;
    }
    .sign .main .title h4 {
        font-size:18px;
    }
    .sign .main h4 a{
        font-weight:400;
        padding:10px;
        color:#969696;
    }
    .sign .main h4 b {
        font-weight:700;
        padding:10px;
        color:#969696;
    }
    .sign .main h4 a.active {
        font-weight:700;
        color:#ea6f5a;
        border-bottom:2px solid #ea6f5a;
    }
    .sign .main h4 a:hover {
        border-bottom:2px solid #ea6f5a;
    }
    .sign .main form {
        color:#969696;
        margin:0 0 30px;
    }
    .sign .main form .input-prepend {
        position:relative;
        width:100%;
    }
    .sign .main form .input-password {
        border-bottom:1px solid #c8c8c8;
        border-radius: 0 0 2px 2px;
    }
    .sign .main form .input-prepend input {
        width:100%;
        height:50px;
        padding:4px 12px 4px 30px;
        border:1px solid #c8c8c8;
        background-color:rgb(248,248,248);
        border-bottom:0;
    }
    .sign .main form .input-prepend:first-of-type input {
        border-radius:2px 2px 0 0;
    }
    .sign .main form .input-prepend:last-of-type input {
        border-bottom:1px solid #c8c8c8;
        border-radius: 0 0 2px 2px;
    }
    .sign .main form .input-prepend i {
        position:absolute;
        left:10px;
        top:15px;
        font-size:20px;
        color:#969696;
    }
    .sign .main form .remember {
        float:left;
        margin:15px 0;
    }
    .sign .main form .help {
        float:right;
        margin:15px 0;
        color:#969696;
    }
    .sign .main form .help:hover {
        color:#333;
    }
    .sign .main form button {
        width:100%;
        padding:9px 18px;
        margin-top:20px;
        text-align:center;
        color:#fff;
        border-radius:25px;
        font-size:18px;
        border:none;
        outline: none;
        display:block;
        clear:both;
    }
    .sign .main form button.sign-in-btn {
        background:#3194D0;
    }
    .sign .main form button.sign-up-btn {
        background:rgb(66,192,46);
    }
    .sign .main form button.sign-in-btn:hover {
        background:#187cb7;
        cursor: pointer;
    }
    .sign .main form button.sign-up-btn:hover {
        background:#3db922;
    }
    .sign .main form p.sign-up-msg {
        font-size:12px;
        margin:15px 0;
        text-align:center;
        line-height:20px;
        color:#969696;
    }
    .sign .main form ssm {
        position:relative;
        line-height: 36px;
    }
    .sign .main form .send-ssm {
        position:absolute;
        right:10px;
        top:10px;
        width:100px;
        height:36px;
        line-height:36px;
        border-radius: 20px;
        color:#fff;
        background:#3db922;
        text-align:center;
    }
    .sign .main .more-sign p {
        position:relative;
        font-size:14px;
        color:#b8b8b8;
        margin-bottom:20px;
    }
    .sign .main .more-sign p:before {
        content:'';
        width:60px;
        border-bottom:1px solid #b8b8b8;
        position:absolute;
        left:30px;
        top:10px;
    }
    .sign .main .more-sign p:after {
        content:'';
        width:60px;
        border-bottom:1px solid #b8b8b8;
        position:absolute;
        right:30px;
        top:10px;
    }
    .sign .main .more-sign ul {
        margin-bottom:10px;
    }
    .sign .main .more-sign ul li {
        display:inline-block;
        color:white;
        margin:0 5px;
        border-radius: 50%;
    }
    .sign .main .more-sign ul li a {
        width: 50px;
        height: 50px;
        line-height: 50px;
        display: block;
    }
    .sign .main .more-sign ul li a i {
        font-size:24px;
        text-align:center;
        line-height:50px;
    }
    .sign .main .more-sign ul li a i.weibo {
        color:#e05244;
    }
    .sign .main .more-sign ul li a i.weixin {
        color:#00bb29;
    }
    .sign .main .more-sign ul li a i.qq {
        color:#498ad5;
    }
    @media (max-width:768px) {
        .sign .logo {
            display:none;
        }
        .sign .main {
            box-shadow: none;
            margin:0 auto;
        }
        .sign {
            background:#fff;
        }
        .sign:before {
            height:0;
        }
    }
</style>
