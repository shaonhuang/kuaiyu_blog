<template>
  <div>
    <div>
      <!-- TODO 插入一个header的组件 -->
      <header>
        <div class="logo">
          <a href>
            <!-- TODO 最好用Svg -->
            <img alt="hyk logo" src="~assets/img/logo/homePageLogo.png" />
            <span class="logoText">快宇Blog</span>
          </a>
        </div>
        <div id="playGame" style="display:none;">
          <div id="playGameCircle">
            <span id="want">
              想
              <span id="wantPlay">玩吗？</span>
            </span>
            <span id="wantPlayHover">按下去，来玩</span>
            <svg style="display: none">
              <!-- TODO 一个圆圈 -->
              <circle />
            </svg>
          </div>
        </div>
      </header>
    </div>
    <div class="menu" style="display:none">
      <a class="menuItem"><img /><span> 选单</span></a>
    </div>
    <section>
      <div id="firstMainContent" class="slowShowUp50Percent">
        <p id="firstMainContentOne">干得好呀，在茫茫Blog里找到了快宇Blog。</p>
        <p id="firstMainContentTwo">
          一个小小的Web开发者的博客，所以我决定向 你分享在成为一个程序员的路上，
          我所有的知识和收藏。
        </p>
      </div>
    </section>
    <!-- TODO 条件-webkit-transform:translate(x,y,z) -->
    <section id="ScrollTwoBigWords">
      <h1>
        <!-- <span>{{ position }}</span> -->
        <!-- :class="args" -->
        <span id="firstWord" class="slowShowUp20Percent">超越</span>
        <span id="secondWord" class="slowShowUp20Percent">极限</span>
      </h1>
    </section>

    <section id="codeBlock">
      <div id="codeDiv">
        <img id="codePic" src="~assets/img/homepage/codes.jpeg" />
      </div>
    </section>

    <section id="secondMainContent">
      <div id="secondMainContentHeadLine" class="notShow">
        <span id="secondMainContentHeadLineText">追逐的事情</span>
      </div>
      <div id="secondMainContentTextS">
        <h3 id="secondMainContentTextContent" class="notShow">
          在小的时候，我时常会想这个互联网是怎么样运作的
          ？长大后的我逐渐明白，每个点击背后的都有不计其数的
          代码在为我们的点击事件的目的而运行。通过编程每个人都可以实现自己的价值，思想和想象力。传播出自己的声音，
          让大家可以通过足不出户的交流成为一个大家庭。
          <strong>stay hungry stay foolish</strong>
        </h3>
      </div>
    </section>
    <section id="threePics">
      <div id="threePicsLeft">
        <div id="threePicsFirst">
          <img src="~assets/img/homepage/hackathon.png" />
        </div>
        <div style="display: none">
          <svg />
        </div>
      </div>
      <div id="threePicsRight">
        <div>
          <div id="threePicsSecond">
            <img src="~assets/img/homepage/hackathon-1.png" />
          </div>
          <div id="threePicsThird">
            <img src="~assets/img/homepage/beyond_boundaries_main.png" alt />
          </div>
        </div>
      </div>
    </section>
    <section id="bottom" style="display:block;">
      <div id="bottomContent">
        <div id="bottomTop">
          <span id="bottomTopContent">那我们就开始吧！</span>
        </div>
        <div id="bottomLeft">
          <span id="bottomLeftContent">从</span>
        </div>
        <div id="bottomMiddle">
          <ul id="bottomMiddleContent">
            <li>
              <a href>
                <span>博客</span>
              </a>
            </li>
            <li>
              <a href>
                <span>个人</span>
              </a>
            </li>
            <li>
              <a href="https://github.com/shaonhuang">
                <span>GitHub</span>
              </a>
            </li>
          </ul>
        </div>
        <div id="bottomRight">
          <span id="bottomRightContent">开始</span>
        </div>
      </div>
    </section>
    <section id="linksAndDeclare">
      <div id="linksAndDeclareLeft">
        <div id="linksAndDeclareLeftHeadline">
          <span id="linksAndDeclareLeftHeadlineContent">社交号</span>
        </div>
        <div id="linksAndDeclareLeftContent" c>
          <ul>
            <li class="notShow">
              <a href="https://space.bilibili.com/275587121">
                <!-- <svg href > -->
                <img src="~assets/img/logo/bilibili.svg" />
                <span>BiliBili</span>
              </a>
            </li>
            <li class="notShow">
              <a href="https://github.com/shaonhuang">
                <img src="~assets/img/logo/github.svg" />
                <span>GitHub</span>
              </a>
            </li>
            <li class="notShow">
              <a @click="alertWeChatId()">
                <img src="~assets/img/logo/wechat.svg" />
                <span>WeChat</span>
              </a>
            </li>
            <li class="notShow">
              <a href="www.linkedin.com/in/yukuaihuang">
                <img src="~assets/img/logo/linkedin.svg" />
                <span>Linkedin</span>
              </a>
            </li>
          </ul>
        </div>
      </div>
      <div id="linksAndDeclareRight">
        <div>
          <span>友情链接</span>
        </div>
        <div></div>
      </div>
      <div id="linksAndDeclareBottom">
        <span>
          Copyright © 2020 黄宇快 Built with Myself. 冀ICP备XXXXXXXX号-X
        </span>
      </div>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import HomePage from "@/components/HomePage.vue";

//HomeCss
import "@/assets/css/Home/HomeLogo.css";
import "@/assets/css/Home/HomeFirstMainContent.css";
import "@/assets/css/Home/HomeScrollTwoBigWords.css";
import "@/assets/css/Home/HomeCodePic.css";
import "@/assets/css/Home/HomeSecondMainContent.css";
import "@/assets/css/Home/HomeThreePics.css";
import "@/assets/css/Home/HomeBottom.css";
import "@/assets/css/Home/HomeLinksAndDeclare.css";

export default {
  name: "Home",
  components: {
    HomePage,
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
    window.addEventListener("scroll", this.slowShowSecondContentTitle);
    window.addEventListener("scroll", this.slowShowSecondContent);
    window.addEventListener("scroll", this.slowShowSocialIconTitle);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    alertWeChatId() {
      alert("WeChatID:  wxid_dl12roffmg0q22");
    },
    handleScroll(event) {
      // Any code to be executed when the window is scrolled
      let scroll = window.scrollY;
      // console.log(this.scrollPosition);

      var objFirst = document.getElementById("firstWord");
      var firstX = -parseInt(scroll);
      var tmp = 0;
      var tmp2 = 0;
      var tmp3 = 0;
      // console.log(-firstX);
      if (tmp < -firstX && -firstX < 3000) {
        for (tmp; tmp < -firstX; tmp++) {
          objFirst.style.webkitTransform = "translateX(" + -tmp + "px" + ")";
          this.tmp = tmp;
        }
      }

      var objSecond = document.getElementById("secondWord");
      var secondX = parseInt(scroll);
      if (tmp2 < secondX && secondX < 3000) {
        for (tmp2; tmp2 < secondX; tmp2++) {
          objSecond.style.webkitTransform = "translateX(" + tmp2 + "px" + ")";
          this.tmp2 = tmp2;
        }
      }

      // var objbottom = document.getElementById("bottom");
      // var objlinksAndDeclare = document.getElementById("linksAndDeclare");
      // var bottomY = parseInt(scroll);
      // console.log("bottomY - 4500:" + (bottomY - 4500));
      // if (tmp3 < bottomY - 4500 && bottomY - 4500 < 1200) {
      //   for (tmp3; tmp3 < bottomY - 4500; tmp3++) {
      //     // objbottom.style.paddingTop = tmp3 + "px";
      //     objbottom.style.webkitTransform = "translateY(" + -tmp3 + "px" + ")";
      //     // console.log("tmp3:" + tmp3);
      //     this.tmp3 = tmp3;
      //   }
      //   objbottom.style.backgroundColor = "#fff";
      // }
    },

    slowShowSecondContentTitle(event) {
      let obj_secondMainContentHeadLineText = document.getElementById(
        "secondMainContentHeadLine"
      );
      let scroll = window.scrollY;
      let tmpPosition = parseInt(scroll);
      if (tmpPosition > 1700) {
        setTimeout(() => {
          obj_secondMainContentHeadLineText.classList.add(
            "slowShowUp50Percent"
          );
          obj_secondMainContentHeadLineText.classList.remove("notShow");
        }, 300);
      }
    },

    slowShowSecondContent(event) {
      let obj_secondMainContentTextContent = document.getElementById(
        "secondMainContentTextContent"
      );
      let scroll = window.scrollY;
      let tmpPosition = parseInt(scroll);
      if (tmpPosition > 1700) {
        setTimeout(() => {
          obj_secondMainContentTextContent.classList.add("slowShowUp50Percent");
          obj_secondMainContentTextContent.classList.remove("notShow");
        }, 200);
      }
    },
    slowShowSocialIconTitle(event) {
      let obj_linksAndDeclareLeftContent = document.getElementById(
        "linksAndDeclareLeftContent"
      );
      let obj_ul_linksAndDeclareLeftContent = obj_linksAndDeclareLeftContent.getElementsByTagName(
        "ul"
      )[0];
      let obj_0_li_ul_linksAndDeclareLeftContent = obj_ul_linksAndDeclareLeftContent.getElementsByTagName(
        "li"
      )[0];
      let obj_1_li_ul_linksAndDeclareLeftContent = obj_ul_linksAndDeclareLeftContent.getElementsByTagName(
        "li"
      )[1];
      let obj_2_li_ul_linksAndDeclareLeftContent = obj_ul_linksAndDeclareLeftContent.getElementsByTagName(
        "li"
      )[2];
      let obj_3_li_ul_linksAndDeclareLeftContent = obj_ul_linksAndDeclareLeftContent.getElementsByTagName(
        "li"
      )[3];

      let scroll = window.scrollY;
      let tmpPosition = parseInt(scroll);

      if (tmpPosition > 4282) {
        setTimeout(() => {
          obj_0_li_ul_linksAndDeclareLeftContent.classList.add(
            "slowShowUp150px"
          );
          obj_0_li_ul_linksAndDeclareLeftContent.classList.remove("notShow");
        }, 200);

        setTimeout(() => {
          obj_1_li_ul_linksAndDeclareLeftContent.classList.add(
            "slowShowUp150px"
          );
          obj_1_li_ul_linksAndDeclareLeftContent.classList.remove("notShow");
        }, 400);

        setTimeout(() => {
          obj_2_li_ul_linksAndDeclareLeftContent.classList.add(
            "slowShowUp150px"
          );
          obj_2_li_ul_linksAndDeclareLeftContent.classList.remove("notShow");
        }, 800);

        setTimeout(() => {
          obj_3_li_ul_linksAndDeclareLeftContent.classList.add(
            "slowShowUp150px"
          );
          obj_3_li_ul_linksAndDeclareLeftContent.classList.remove("notShow");
        }, 1000);
      }
    },
  },
  data() {
    return {
      args: "translate3d(100px,100px,100px)",
      secondMainContentPosition: 1500,
    };
  },
  computed: {},
};
</script>
<style scoped>
.menu {
  padding: 0;
  margin: 0;
  /* display: inline; */
  position: fixed;
  left: 60px;
  top: 48%;
  z-index: 999;
}

.menuItem {
  font-size: 120%;
  color: #fff;
}

.notShow {
  opacity: 0;
}
.Show {
  opacity: 1;
}
.slowShowUp20Percent {
  -webkit-animation: slowShowUp20 ease-out 0.7s;
}
.slowShowUp50Percent {
  -webkit-animation: slowShowUp50 ease-out 1.2s;
}
.slowShowUp150px {
  -webkit-animation: slowShowUp150px ease-out 1.2s;
}

@-webkit-keyframes slowShowUp20 {
  0% {
    -webkit-transform: translateY(300px);
    opacity: 0;
  }
  90% {
    opacity: 0.6;
  }
  100% {
    -webkit-transform: translateY(0px);
    opacity: 1;
  }
}
@-webkit-keyframes slowShowUp50 {
  0% {
    -webkit-transform: translateY(750px);
    opacity: 0;
  }
  50% {
    -webkit-transform: translateY(750px);
    opacity: 0;
  }
  70% {
    opacity: 0.6;
  }
  100% {
    -webkit-transform: translateY(0px);
    opacity: 1;
  }
}
@-webkit-keyframes slowShowUp150px {
  0% {
    -webkit-transform: translateY(150px);
    opacity: 0;
  }
  50% {
    opacity: 0;
  }
  70% {
    opacity: 0.6;
  }
  100% {
    -webkit-transform: translateY(0px);
    opacity: 1;
  }
}
@-webkit-keyframes flash {
  0%,
  10%,
  55%,
  90%,
  94%,
  98%,
  30% {
    opacity: 0.2;
  }
  75% {
    opacity: 0.5;
  }
  92% {
    opacity: 0.7;
  }
  96% {
    opacity: 0.9;
  }
  99% {
    opacity: 0.95;
  }
  100% {
    opacity: 1;
  }
}

#playGame {
  position: absolute;
  width: 20%;
  top: 20%;
  left: 74%;
  text-align: center;
  cursor: pointer;
}
#playGameCircle {
  display: block;
  /* border: 3px solid orange; */
  height: 150px;
  width: 150px;
  border-radius: 100%;
  text-align: center;
  z-index: 999;
}
#want {
  display: block;
  padding-top: 40%;
  padding-left: 6%;
  font-size: 100%;
  color: #fff;
  transition: all 0.5s linear;
  -webkit-transform: rotateX(0);
}
#wantPlay {
}
#playGameCircle {
  transition: all 1s linear;
  -webkit-transition: all 1.5s linear;
}
#playGameCircle:active {
  border: 3px solid white;
  -webkit-animation: shake 0.5s;
}
#playGameCircle:hover #want {
  -webkit-transition: all 0.5s linear;
  -webkit-transform: translateY(-30px);
  -webkit-transform: rotateX(40deg);
  opacity: 0;
}

#playGameCircle:hover #wantPlayHover {
  -webkit-animation: fadeIn ease 5s;
}
#wantPlayHover {
  position: absolute;
  z-index: 2;
  font-size: 100%;
  color: #fff;
  opacity: 0;
  left: 30px;
  bottom: 70px;
  perspective: 300px;
  transform-origin: center bottom;
  transition: all 0.5s linear;
  -webkit-transform: rotateX(90deg);
}
@-webkit-keyframes fadeIn {
  0% {
    opacity: 0;
  }
  30% {
    opacity: 1;
    /* -webkit-transform: translateY(-30px); */
  }
  40% {
    -webkit-transform: rotateX(0deg);
  }
  100% {
    opacity: 1;
  }
}
@-webkit-keyframes shake {
  0%,
  10%,
  55%,
  90%,
  94%,
  98%,
  100% {
    -webkit-transform: scale(1, 1);
  }
  30% {
    -webkit-transform: scale(1.14, 0.86);
  }
  75% {
    -webkit-transform: scale(0.92, 1.08);
  }
  92% {
    -webkit-transform: scale(1.04, 0.96);
  }
  96% {
    -webkit-transform: scale(1.02, 0.98);
  }
  99% {
    -webkit-transform: scale(1.01, 0.99);
  }
}
.el-col {
  border-radius: 4px;
}
.bg-purple-dark {
  background: #99a9bf;
}
.bg-purple {
  background: #d3dce6;
}
.bg-purple-light {
  background: #e5e9f2;
}
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
</style>
