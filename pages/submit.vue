<template>
<div class="submit">
  <div class="food-form">
    <table width="300" border="1">
　<tr>
    <td>+1選購</td>
    <td>品項</td>
    <td>數量</td>
    <td>單價</td>
    <td>誰也訂購</td>
　</tr>
  <tr>
    <td></td>　
    <td>日式豬排飯</td>
      <td></td>
    　<td></td>
      <td></td>
　</tr>
  <tr>
    <td></td>　
    <td>照燒雞腿飯</td>
      <td></td>
    　<td></td>
    <td></td>
</tr>
<tr>
    <td></td>
    <td>檸檬鮭魚飯</td>
      <td></td>
    　<td></td>
    <td></td>
</tr>
<tr>
    <td></td>　
    <td>客家控肉飯</td>
      <td></td>
    　<td></td>
    <td></td>
</tr>
<tr>
    <td></td>　
    <td>檸檬鮭魚飯</td>
      <td></td>
    　<td></td>
    <td></td>
</tr>
<tr>
    <td></td>　
    <td>檸檬鮭魚飯</td>
      <td></td>
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
</template>

<style>

.submit {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.form-group{
  font-weight: 10000;
  color: #526488
}
.btn-primary{
  margin-left: 20px;
  margin-top:42px
}
</style>
