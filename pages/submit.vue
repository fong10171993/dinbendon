<template>
<div class="order-page">
  <span class="submit-title"><h2>今天吃&#160;&#160;\派克雞排/</h2></span>
<div class="submit">
  <div class="food-form">
    <table width="500" border="1">
　<tr>
    <td>+1選購</td>
    <td>品項</td>
    <td>單價</td>
    <td>數量</td>
    <td>總價</td>
    <td>訂單量</td>
　</tr>
  <tr>
    <td><input type="checkbox" value="1" name="Product_1"></td>　
    <td>脆皮雞排</td>
      <td>$65</td>
    　<td><ol>
      <li><input type="number" id="tea" value="0"> 項</li>
      </ol></td>
      <td><span id="subtotal">0</span>元</td>
      <td></td>
　</tr>
  <tr>
    <td><input type="checkbox" value="1" name="Product_1"></td>　
    <td>無骨雞塊</td>
      <td>$65</td>
    　<td><ol>
      <li><input type="number" id="tea" value="0"> 項</li>
      </ol></td>
    <td><span id="subtotal">0</span>元</td>
    <td></td>
</tr>
<tr>
    <td><input type="checkbox" value="1" name="Product_1"></td>
    <td>脆皮鮮魷</td>
      <td>$65</td>
    　<td><ol>
      <li><input type="number" id="tea" value="0"> 項</li>
      </ol></td>
    <td><span id="subtotal">0</span>元</td>
    <td></td>
</tr>
<tr>
    <td><input type="checkbox" value="1" name="Product_1"></td>　
    <td>脆皮雞翅</td>
      <td>$25</td>
    　<td><ol>
      <li><input type="number" id="tea" value="0"> 項</li>
      </ol></td>
    <td><span id="subtotal">0</span>元</td>
    <td></td>
</tr>
<tr>
    <td><input type="checkbox" value="1" name="Product_1"></td>　
    <td>七里香</td>
      <td>$25</td>
    　<td><ol>
      <li><input type="number" id="tea" value="0"> 項</li>
      </ol></td>
    <td><span id="subtotal">0</span>元</td>
    <td></td>
</tr>
</table>
<button class=add-items>新增品項</button>
<button class=add-items>確認</button>
    <div class="form-group">
    <label for="formGroupExampleInput2">有什麼特殊需求？跟我說</label><br>
    <input type="text" class="form-control" id="formGroupExampleInput2" placeholder="例如:雞排加辣不要切">
    </div>
    </div>
    <button class="btn btn-primary" @click="createPost">送出</button>
</div>
<a href="http://localhost:3000/addlist"><button class=add-list>＋建立新團購單</button></a>


</div>
</template>

<style>
.add-list{
  height: 50px;
  width: 120px;
  border-radius: 50px;
  background-color: #FFBB00	;
  color:black;
  position: absolute;
    top: 5%;
    left:88%

}
.submit-title{
  position: absolute;
    top: 45%;
    left: 50%;
    margin-top: -170px;
    margin-left: -125px;
  font-weight: 10000;
  color: #007799
}
.submit {
  position: absolute;
    top: 42%;
    left: 44%;
    margin-top: -100px;
    margin-left: -200px;
    text-align: center;
}
.form-group{
  position: absolute;
    top: 50%;
    left: 50%;
    margin-top: 180px;
    margin-left: -90px;
  font-weight: 10000;
  color: #526488
}
.add-items{
  margin-top:20px
}
.form-control{
  width: 300px;
  position: absolute;
    top: 100%;
    left: -35%;
}
.btn-primary{
  height: 30px;
  width: 300px;
  color: #f8f8f8;
  background-color: #E63F00;
  position: absolute;     /*絕對位置*/
    top: 50%;               /*從上面開始算，下推 50% (一半) 的位置*/
    left: 50%;              /*從左邊開始算，右推 50% (一半) 的位置*/
    margin-top: 230px;
    margin-left: -150px;
}
.qty {
  width: 40px;
  height: 35px;
  text-align: center;
  border: 0;
  border-top: 1px solid #aaa;
  border-bottom: 1px solid #aaa;
}


input.qtyplus {
  width: 25px;
  height: 35px;
  border: 1px solid #aaa;
  background: #f8f8f8;
}

input.qtyminus {
  width: 25px;
  height: 35px;
  border: 1px solid #aaa;
  background: #f8f8f8;
}
</style>
