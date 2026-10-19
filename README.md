<!DOCTYPE html>
<html lang="ar" dir="rtl">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>تسيير الفورفاي</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Tahoma,sans-serif;
}

body{
background:#f5f7fa;
padding:10px;
}

.container{
max-width:1200px;
margin:auto;
background:white;
padding:15px;
border-radius:15px;
box-shadow:0 2px 10px rgba(0,0,0,.1);
}

.title{
text-align:center;
margin-bottom:15px;
color:#2c3e50;
}

input{
width:100%;
padding:12px;
margin:5px 0;
border:1px solid #ddd;
border-radius:8px;
font-size:16px;
}

button{
padding:10px;
border:none;
border-radius:8px;
cursor:pointer;
color:white;
font-size:15px;
}

.add-btn{
background:#27ae60;
width:100%;
}

.reset-btn{
background:#e74c3c;
width:100%;
margin-top:10px;
}

.cards{
display:grid;
grid-template-columns:1fr;
gap:10px;
margin-top:15px;
}

.card{
background:#ecf0f1;
padding:15px;
border-radius:12px;
text-align:center;
}

.card h3{
font-size:14px;
margin-bottom:5px;
}

.card span{
font-size:22px;
font-weight:bold;
}

.table-wrapper{
overflow-x:auto;
margin-top:15px;
}

table{
width:100%;
min-width:1000px;
border-collapse:collapse;
}

th,td{
border:1px solid #ddd;
padding:8px;
text-align:center;
}

th{
background:#3498db;
color:white;
}

.edit-btn{
background:#f39c12;
padding:6px 10px;
}

.delete-btn{
background:#e74c3c;
padding:6px 10px;
}

@media(min-width:768px){

.cards{
grid-template-columns:repeat(3,1fr);
}

.form-grid{
display:grid;
grid-template-columns:repeat(5,1fr);
gap:10px;
}

}

</style>
</head>

<body>

<div class="container">

<h1 class="title">📱 تسيير بيع الفورفاي</h1>

<label>الكاسة في الصباح</label>
<input type="number" id="startCash" value="0">

<div class="form-grid">

<input id="type" placeholder="نوع الفورفاي">

<input id="original"
type="number"
placeholder="السوم الأصلي">

<input id="sale"
type="number"
placeholder="سوم البيع">

<input id="stock"
type="number"
placeholder="الستوك الأول">

<input id="sold"
type="number"
placeholder="الكمية المباعة">

</div>

<button class="add-btn"
onclick="addSale()">
➕ إضافة عملية
</button>

<div class="cards">

<div class="card">
<h3>المداخيل</h3>
<span id="income">0</span>
</div>

<div class="card">
<h3>الأرباح</h3>
<span id="profit">0</span>
</div>

<div class="card">
<h3>الكاسة الحالية</h3>
<span id="finalCash">0</span>
</div>

</div>

<label style="margin-top:15px;display:block;">
المصاريف
</label>

<input id="expenses"
type="number"
value="0">

<div class="table-wrapper">

<table>

<thead>
<tr>
<th>النوع</th>
<th>الأصلي</th>
<th>البيع</th>
<th>ربح الوحدة</th>
<th>الستوك</th>
<th>المباع</th>
<th>الباقي</th>
<th>المداخيل</th>
<th>الربح</th>
<th>تعديل</th>
<th>حذف</th>
</tr>
</thead>

<tbody id="salesTable">
</tbody>

</table>

</div>

<button class="reset-btn"
onclick="resetAll()">
🗑️ مسح جميع البيانات
</button>

<script>
/* الجزء 2 هنا */
</script>

</div>

</body>
</html>
