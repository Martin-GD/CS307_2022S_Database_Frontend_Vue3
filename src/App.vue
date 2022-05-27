
<template>
  <div>

    <div class="h-6" />
    <el-menu
        :default-active="activeIndex2"
        class="el-menu-demo"
        mode="horizontal"
        background-color="#86bef3"
        text-color="#fff"
        active-text-color="#ffd04b"
        @select="handleSelect"
    >
      <el-menu-item index="1"><router-link to="/">Home</router-link></el-menu-item>
      <el-menu-item index="2"><router-link to="/Import">Import</router-link></el-menu-item>

      <el-sub-menu index="2">
        <template #title>Check</template>
        <el-menu-item index="2-1"><router-link to="/about">AllStaffCount</router-link></el-menu-item>
        <el-menu-item index="2-2"><router-link to="/ContractCount">ContractCount</router-link></el-menu-item>
        <el-menu-item index="2-3"><router-link to="/OrderCount">OrderCount</router-link></el-menu-item>
        <el-menu-item index="2-4"><router-link to="/NeverSoldProductCount">NeverSoldProductCount</router-link></el-menu-item>
        <el-menu-item index="2-5"><router-link to="/FavoriteProductModel">FavoriteProductModel</router-link></el-menu-item>
        <el-menu-item index="2-6"><router-link to="/AvgStockByCenter">AvgStockByCenter</router-link></el-menu-item>
        <el-menu-item index="2-7"><router-link to="/ProductByNumber">ProductByNumber</router-link></el-menu-item>
        <el-menu-item index="2-8"><router-link to="/ContractInfo">ContractInfo</router-link></el-menu-item>

      </el-sub-menu>
      <el-menu-item index="3"><router-link to="/MonthlyAll">MonthlyAll</router-link></el-menu-item>
      <el-menu-item index="4"><router-link to="/OrderSelect">OrderSelect</router-link></el-menu-item>

      <el-sub-menu index="5">
        <template #title>switchUser</template>
        <el-menu-item index="5-1"><router-link to="/changeToManager">changeToManager</router-link></el-menu-item>
        <el-menu-item index="5-2"><router-link to="/changeBack">changeBack</router-link></el-menu-item>
        <el-menu-item index="5-3"><router-link to="/createRole">changeToStaff</router-link></el-menu-item>

      </el-sub-menu>
    </el-menu>

      <div id="backcont">
        <router-view/>
      </div>

  </div>

</template>

<style>
#backcont {
  background-image: url("./assets/mountain.jpeg");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  min-height: 100vh;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #255586;
  margin-top: 0;
}

</style>


