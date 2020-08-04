<template>
  <div>
    <div>
      <!-- TODO 插入一个header的组件 -->
      <header>
        <div>
          <a href>
            <!-- TODO 最好用Svg -->
            <img alt="hyk logo" src="~assets/img/logo/homePageLogo.png" />
            <span>快宇Blog</span>
          </a>
        </div>
        <div>
          <span>
            想
            <span>玩吗？</span>
          </span>
          <span>按下去，来玩</span>
          <svg>
            <!-- TODO 一个圆圈 -->
            <circle />
          </svg>
        </div>
      </header>
    </div>
    <section>
      <div>
        <p>干得好呀，在茫茫Blog里找到了快宇Blog。</p>
        <h2>
          一个小小的Web开发者的博客，所以我决定向
          你分享在成为一个程序员的路上，
          我所有的知识和收藏。
        </h2>
      </div>
    </section>
    <section>
      <h1>
        <span>超越</span>
        <span>极限</span>
      </h1>
    </section>
    <section>
      <div>
        <img src="~assets/img/homepage/codes.jpeg" />
      </div>
    </section>
    <section>
      <div>
        <span>beyond boundaries</span>
      </div>
      <div>
        <h3>
          at abstraction, we go
          <strong>beyond boundaries</strong>
          in everything we do. by constantly
          pushing limits and exploring new territory,
          we help ambitious partners succeed in
          multi-platform game development and
          adaptations.
        </h3>
      </div>
    </section>
    <section>
      <div>
        <div>
          <img src="~assets/img/homepage/hackathon.png" />
        </div>
        <div>
          <svg />
        </div>
      </div>
      <div>
        <div>
          <div>
            <img src="~assets/img/homepage/hackathon-1.png" />
          </div>
          <div>
            <img src="~assets/img/homepage/beyond_boundaries_main.png" alt />
          </div>
        </div>
      </div>
    </section>
    <section>
      <div>
        <span>那我们就开始吧！</span>
      </div>
      <div>
        <span>从</span>
      </div>
      <div>
        <ul>
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
            <a href>
              <span>GitHub</span>
            </a>
          </li>
        </ul>
      </div>
      <div>
        <span>开始</span>
      </div>
    </section>
    <section>
      <div>
        <div>
          <div>
            <span>社交号</span>
          </div>
          <div>
            <ul>
              <li>
                <a href>
                  <svg />
                  <span>BiliBili</span>
                </a>
              </li>
              <li>
                <a href>
                  <svg />
                  <span>GitHub</span>
                </a>
              </li>
              <li>
                <a href>
                  <svg />
                  <span>WeChat</span>
                </a>
              </li>
              <li>
                <a href>
                  <svg />
                  <span>Linked</span>
                </a>
              </li>
            </ul>
          </div>
        </div>
        <div>
          <div>
            <span>友情链接</span>
          </div>
          <div></div>
        </div>
        <div>
          <span>
            Copyright © 2020 黄宇快 Built with Myself.
            冀ICP备XXXXXXXX号-X
          </span>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import HomePage from "@/components/HomePage.vue";

export default {
  name: "Home",
  components: {
    HomePage,
  },
};
</script>
