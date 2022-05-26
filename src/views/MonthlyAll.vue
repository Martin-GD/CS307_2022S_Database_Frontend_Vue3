<template>
  <div>
    <div class="home">
      <img alt="Vue logo" src="../assets/logo.png">
      <h1 align = "center" >SUSTC Monthly Bill</h1>

    </div>
    <el-carousel :interval="4000" type="card" height="400px">
      <el-carousel-item v-for="item in 12" :key="item">
        <h1 text="2xl" justify="center">{{item }}</h1>
        <el-table :data="tableData[item]"  align="center" stripe="true">
          <el-table-column prop="revenue_this_month" label="Revenue_this_month" width="200" />
          <el-table-column prop="hot_commodity" label="Hot_commodity" width="200" />
          <el-table-column prop="hot_supply_center" label="Hot_supply_center" width="200" />
          <el-table-column prop="salesKing" label="salesKing" width="200" />
        </el-table>
      </el-carousel-item>
    </el-carousel>
  </div>

</template>
<script>
import axios from 'axios'

export default {
  data(){
    return{
      msg:'hello world!',
      tableData : [],

    }
  },
  created() {
    const _this=this
    const url = "http://10.26.142.228:8181/getMonthlyAll";
    axios.get(url).then(function (resp){
      _this.tableData = resp.data
      console.log(resp.data)
    })
  }
}
</script>
<style scoped>

img {
  margin: 0 auto;
  align-items: center;
  text-align: center;
  display: flex;
}
.el-carousel__item h1 {
  color: #f5ac2c;
  opacity: 0.75;
  line-height: 80px;
  margin: 0;
  text-align: center;
}

.el-carousel__item:nth-child(2n) {
  background-color: #cce7f8;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #b3f5e6;
}
</style>
