<template>
  <el-container>
    <el-header class="headerAll"><img src=""
           class="headImage">
      <el-menu :default-active="activeIndex"
               class="el-menu-demo"
               mode="horizontal"
               background-color="#222a30"
               text-color="#fff"
               active-text-color="#29e2fe"
               @select="handleSelect">
        <el-menu-item v-for="(item, index) in menuList"
                      :key="index"
                      :index="item.index">{{item.name}}</el-menu-item>
      </el-menu>
    </el-header>
    <!-- <Head msg="Welcome to Your Vue.js + TypeScript App"></Head> -->
    <el-main>Main</el-main>
  </el-container>
  <!-- <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>
  </div> -->

</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Head from "@/components/Head.vue"; // @ is an alias to /src

@Component({
  components: {
    Head
  }
})
export default class Home extends Vue {}
</script>
