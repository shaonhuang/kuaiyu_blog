<template>
  <div>
    <header>
      <div>
        <span>博客</span>
      </div>
    </header>
    <!-- 1.这里把菜单做成插槽 -->
    <slot name="menu">
      <img src alt />
      <div>
        <span>菜单</span>
      </div>
    </slot>
    <!-- 列表形式 -->
    <div>
      <slot></slot>
    </div>
    <!--  -->
    <div>
      <ul>
        <li>
          <a href>
            <svg />
            <span>前</span>
          </a>
        </li>
        <li>
          <a href>
            <span>{{pageNumber}}</span>
          </a>
        </li>
        <li>
          <a href>
            <span>后</span>
            <svg />
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  props: {},
  data() {
    return {
      pageNumber: {
        type: Number,
        default: 1,
      },
    };
  },
  computed: {},
  methods: {},
});
</script>