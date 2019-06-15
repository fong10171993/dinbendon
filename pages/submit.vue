<template>
<div class="order-page">
  <span class="submit-title"><h2>今天吃&#160;&#160;\派克雞排/</h2></span>
<div class="submit">
  <div class="food-form">
    <table width="300" border="1">
　<tr>
    <td>+1選購</td>
    <td>品項</td>
    <td>單價</td>
    <td>數量</td>
    <td>總價</td>
　</tr>
  <tr>
    <td><input type="checkbox" value="1" name="Product_1"></td>　
    <td>脆皮雞排</td>
      <td>$65</td>
    　<td></td>
      <td></td>
　</tr>
  <tr>
    <td><input type="checkbox" value="1" name="Product_1"></td>　
    <td>無骨雞塊</td>
      <td>$65</td>
    　<td></td>
    <td></td>
</tr>
<tr>
    <td><input type="checkbox" value="1" name="Product_1"></td>
    <td>脆皮鮮魷</td>
      <td>$65</td>
    　<td></td>
    <td></td>
</tr>
<tr>
    <td><input type="checkbox" value="1" name="Product_1"></td>　
    <td>脆皮雞翅</td>
      <td>$25</td>
    　<td></td>
    <td></td>
</tr>
<tr>
    <td><input type="checkbox" value="1" name="Product_1"></td>　
    <td>七里香</td>
      <td>$25</td>
    　<td></td>
    <td></td>
</tr>
</table>
    <div class="form-group">
    <label for="formGroupExampleInput2">有什麼特殊需求？跟我說</label><br>
    <input type="text" class="form-control" id="formGroupExampleInput2" placeholder="例如:雞排加辣不要切">
    </div>
    </div>
    <button class="btn btn-primary" @click="createPost">送出</button>
</div>
</div>
</template>

<style>
.sorder-page{
  position: absolute;
    top: 48%;
    left: 43%;
}
.submit-title{
  position: absolute;
    top: 50%;
    left: 50%;
    margin-top: -170px;
    margin-left: -125px;
  font-weight: 10000;
  color: #FF8800
}
.submit {
  position: absolute;
    top: 50%;
    left: 50%;
    margin-top: -120px;
    margin-left: -180px;
    text-align: center;
}
.form-group{
  position: absolute;
    top: 50%;
    left: 50%;
    margin-top: 120px;
    margin-left: -90px;
  font-weight: 10000;
  color: #526488

}
.btn-primary{
  height: 30px;
  width: 300px;
  position: absolute;     /*絕對位置*/
    top: 50%;               /*從上面開始算，下推 50% (一半) 的位置*/
    left: 50%;              /*從左邊開始算，右推 50% (一半) 的位置*/
    margin-top: 175px;
    margin-left: -150px;
}
</style>
