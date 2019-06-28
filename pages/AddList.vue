<template>
  <div class="add-list-page">
    <a href="http://localhost:3000/"><button class="back-homepage">回首頁</button></a>
    <span class="addlist-title"><label  for="formGroupExampleInput2"><h1>今天想開什麼團？</h1></label></span><br>
    <label>店家名稱</label>
    <input type="text" class="form-control01" id="formGroupExampleInput2" placeholder="例如:八方雲集" v-model="shop_name"><br><br><br>
    <div class="additems">
    <label>輸入品項</label>
    <input type="text" class="form-control" id="formGroupExampleInput2" placeholder="例如:玉米湯餃" v-model="newProductName">
    <label>商品價格</label>
    <input type="text" class="form-control" id="formGroupExampleInput2" placeholder="例如:65元" v-model="newProductPrice">
    <button class="add" @click="createProduct">新增</button>
    </div>
    <div>
        <table width="500" border="1">
        　<tr>
            <td>品項</td>
            <td>單價</td>
        　</tr>
        <tr v-for="product in products" :key="product.id">
            <td>{{ product.name }}</td>
            <td>{{ product.price }}</td>
        　</tr>
        </table>
    </div>
    <div><button class="submit-list" @click="submit">++建立團購單</button></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      shop_name: '',
      newProductName: '',
      newProductPrice: '',
      products: []
    }
  },
  methods: {
    createProduct() {
      this.products.push({
        name: this.newProductName,
        price: this.newProductPrice
      })
      this.newProductName = ''
      this.newProductPrice = ''
    },
    async submit() {
      const { data } = await this.$axios.post('http://localhost:8000/api/orders', {
        shop_name: this.shop_name
      })
    
      const myOrder_id = data.data.id

      // for (let myProduct of this.products) {
      //   const { data } = await this.$axios.post('http://localhost:8000/api/products', {
      //     name: myProduct.name,
      //     price: myProduct.price,
      //     order_id: myOrder_id
      //   })
      // }


      let pData = await Promise.all(this.products.map((product) => {
        return this.$axios.post('http://localhost:8000/api/products', {
          name: product.name,
          price: product.price,
          order_id: myOrder_id
        })
      }))


      this.$router.push('/submit?order_id=' + myOrder_id)

    }
  }
}
</script>



<style>
.add-list-page{
  position: absolute;
    top: 25%;
    left: 30%;
}
.back-homepage{
  width: 60px;
  height: 40px;
  position: absolute;
    top:-40%;
    left: 88%;
  border-radius: 5px
}
.addlist-title{
  color:#007799
}
.form-control01{
  width: 250px;
  height: 30px;
  margin-left:10px
}
.form-control{
  width: 140px
}
.additems{
  background-color: #eeee;
  border-radius: 5px;
  padding:10px
}
.add{
  color:seashell;
  background-color:#00AAAA
}
.submit-list{
  width: 150px;
  height: 40px;
  margin-top:30px;
  position: absolute;
    top:120%;
    left: 36%;
  background-color:#FFBB00;
  border-radius: 5px

}
</style>
