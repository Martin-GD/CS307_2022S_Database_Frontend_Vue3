<template>
  <div>

    <img alt="Vue logo" src="../assets/logo.png">
    <h1 align = "center" >SUSTC Data Import </h1>
    <h1 align = "center" >You can use the following button to update the company's database.</h1>

    <!--    <el-row class="mb-4">-->
    <table align="center">
      <el-button @click="impBasic" type="success">impBasic</el-button>
      <el-button @click="impCenter" type="success">impCenter</el-button>
      <el-button @click="impEnterprise" type="success">impEnterprise</el-button>
      <el-button @click="impStaff" type="success">impStaff</el-button>
      <el-button @click="impModel" type="success">impModel</el-button>
      <el-button @click="setStockIn" type="primary">setStockIn</el-button>
      <el-button @click="placeOrder" type="primary">placeOrder</el-button>
      <el-button @click="updateOrder" type="primary">updateOrder</el-button>
      <el-button @click="deleteOrder" type="warning">deleteOrder</el-button>
      <el-button @click="getAllMonthBill" type="info">getAllMonthBill</el-button>
      <el-button @click="truncateAll" type="danger">truncateAll</el-button>
    </table>
    <table valign="bottom" align="center" >
      <h1 align = "center" >No matter how far you may fly, never forget where you come from.</h1>
    </table>


<!--    </el-row>-->
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: "Import",
  methods:{
    impBasic(){
      const _this = this
      axios.get("http://10.26.142.228:8181/impBasic").then(function (resp){
        alert(resp.data)
      })
    },impCenter(){
      const _this = this
      axios.get("http://10.26.142.228:8181/impCenter").then(function (resp){
        alert(resp.data)
      })
    },
    impEnterprise(){
      const _this = this
      axios.get("http://10.26.142.228:8181/impEnterprise").then(function (resp){
        alert(resp.data)
      })
    },
    impStaff(){
      const _this = this
      axios.get("http://10.26.142.228:8181/impStaff").then(function (resp){
        alert(resp.data)
      })
    },
    impModel(){
      const _this = this
      axios.get("http://10.26.142.228:8181/impModel").then(function (resp){
        alert(resp.data)
      })
    },
    setStockIn(){
      const _this = this
      axios.get("http://10.26.142.228:8181/setStockIn").then(function (resp){
        alert(resp.data)
      })
    },
    placeOrder(){
      const _this = this
      axios.get("http://10.26.142.228:8181/placeOrder").then(function (resp){
        alert(resp.data)
      })
    },
    updateOrder(){
      const _this = this
      axios.get("http://10.26.142.228:8181/updateOrder").then(function (resp){
        alert(resp.data)
      })
    },
    deleteOrder(){
      const _this = this
      axios.get("http://10.26.142.228:8181/deleteOrder").then(function (resp){
        alert(resp.data)
      })
    },
    getAllMonthBill(){
      const _this = this
      axios.get("http://10.26.142.228:8181/getAllMonthBill").then(function (resp){
        alert(resp.data)
      })
    },
    truncateAll(){
      const _this = this
      axios.get("http://10.26.142.228:8181/truncateAll").then(function (resp){
        alert(resp.data)
      })
    }
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

</style>