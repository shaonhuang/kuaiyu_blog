<template>
  <div>
    <!-- 1.这里把菜单做成插槽  -->
    <slot name="menu">
      <img src alt />
      <div>
        <span>菜单</span>
      </div>
    </slot>

    <!-- 还缺一个搜索栏 -->
    <!-- <slot><search-bar></search-bar></slot> -->
    <div>
      <ul>
        <li>
          <a>
            <span>首页</span>
          </a>
        </li>
        <li>
          <a>
            <span>工程项目</span>
          </a>
        </li>
        <li>
          <a>
            <span>博客</span>
          </a>
        </li>
        <li>
          <a>
            <span>教程</span>
          </a>
        </li>
        <li>
          <a>
            <span>游记</span>
          </a>
        </li>
        <li>
          <a>
            <span>个人</span>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>