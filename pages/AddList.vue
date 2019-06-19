<template>
  <div class="add-list-page">
    <a href="http://localhost:3000/"><button class="back-homepage">回首頁</button></a>
    <span class="addlist-title"><label  for="formGroupExampleInput2"><h1>今天想開什麼團？</h1></label></span><br>
    <label>店家名稱</label>
    <input type="text" class="form-control01" id="formGroupExampleInput2" placeholder="例如:八方雲集"><br><br><br>
    <div class="additems">
    <label>輸入品項</label>
    <input type="text" class="form-control" id="formGroupExampleInput2" placeholder="例如:玉米湯餃">
    <label>商品價格</label>
    <input type="text" class="form-control" id="formGroupExampleInput2" placeholder="例如:65元">
    <button class="add">新增</button>
    </div>
    <div>
        <table width="500" border="1">
        　<tr>
            <td>品項</td>
            <td>單價</td>
        　</tr>
        <tr>
            <td></td>
            <td></td>
        　</tr>
        </table>
    </div>
    <div><button class=submit-list>++建立團購單</button></div>
  </div>
</template>

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
