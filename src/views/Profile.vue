<template>
  <div>
    <header>
      <div>
        <span>博客</span>
      </div>
    </header>
    <div>
      <!-- 1.这里把菜单做成插槽 -->
      <slot name="menu">
        <img src alt />
        <div>
          <span>菜单</span>
        </div>
      </slot>
      <div>
        Hello! 我是黄宇快
        欢迎来到我的博客！我是现读北京邮电大学数字媒体专业大三学生
      </div>
      <div>
        +86 188 1001 5082
        yukuaihuang@icloud.com
      </div>
      <div>
        <a href>
          <svg />
          <span>简历</span>
        </a>
      </div>
      <div>
        <div>
          <span>联系方式</span>
        </div>
        <div>
          <ul>
            <li>
              <div>
                <span>WeChat</span>
                <!-- TODO点击展示图片 -->
                <img src alt />
              </div>
            </li>
            <li>
              <div>
                <span>QQ</span>
                <!-- TODO 放置划出QQ号 -->
                <span>{{qqNum}}</span>
              </div>
            </li>
            <li>
              <a href>
                <span>LinkedIn</span>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>