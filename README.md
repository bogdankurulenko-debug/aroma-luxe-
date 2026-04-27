# aroma-luxe-
<!DOCTYPE html>
<html lang="uk">
<head>
<meta charset="UTF-8">
<title>Aroma Luxe</title>

<style>
body{
    margin:0;
    font-family:Arial;
    background:#f5f5f5;
    color:#111;
}

header{
    background:white;
    padding:15px;
    text-align:center;
    font-size:22px;
    border-bottom:1px solid #ddd;
    position:sticky;
    top:0;
}

.filters{
    display:flex;
    justify-content:center;
    gap:10px;
    padding:10px;
}

.filters button{
    padding:8px 12px;
    border:none;
    background:black;
    color:white;
    border-radius:5px;
}

.container{
    padding:10px;
}

.grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:10px;
}

.card{
    background:white;
    border-radius:10px;
    padding:10px;
    box-shadow:0 2px 10px rgba(0,0,0,0.1);
    text-align:center;
}

.card img{
    width:100%;
    height:140px;
    object-fit:cover;
    border-radius:10px;
}

select{
    width:100%;
    padding:5px;
    margin-top:5px;
}

button.buy{
    margin-top:5px;
    width:100%;
    padding:8px;
    border:none;
    background:black;
    color:white;
    border-radius:5px;
}

.cart{
    position:fixed;
    bottom:0;
    width:100%;
    background:white;
    border-top:1px solid #ddd;
    padding:10px;
    text-align:center;
}
</style>
</head>

<body>

<header>✨ Aroma Luxe</header>

<div class="filters">
<button onclick="filter('all')">Всі</button>
<button onclick="filter('men')">Чоловічі</button>
<button onclick="filter('women')">Жіночі</button>
</div>

<div class="container">
<div class="grid">

<!-- 1 -->
<div class="card product men">
<img src="https://images.unsplash.com/photo-1615634260167-c8cdede054de">
<h3>Dior Sauvage</h3>
<select onchange="update(this,'p1')">
<option value="399">30 ml — 399 грн</option>
<option value="549">50 ml — 549 грн</option>
<option value="749">100 ml — 749 грн</option>
</select>
<p>Ціна: <span id="p1">399</span> грн</p>
<button class="buy" onclick="add('Dior Sauvage','p1')">В корзину</button>
</div>

<!-- 2 -->
<div class="card product men">
<img src="https://images.unsplash.com/photo-1618354691373-d851c5c3a990">
<h3>Chanel Bleu</h3>
<select onchange="update(this,'p2')">
<option value="449">30 ml — 449 грн</option>
<option value="599">50 ml — 599 грн</option>
<option value="799">100 ml — 799 грн</option>
</select>
<p>Ціна: <span id="p2">449</span></p>
<button class="buy" onclick="add('Chanel Bleu','p2')">В корзину</button>
</div>

<!-- 3 -->
<div class="card product men">
<img src="https://images.unsplash.com/photo-1619451334792-150fd785ee74">
<h3>Versace Eros</h3>
<select onchange="update(this,'p3')">
<option value="349">30 ml — 349 грн</option>
<option value="499">50 ml — 499 грн</option>
<option value="699">100 ml — 699 грн</option>
</select>
<p>Ціна: <span id="p3">349</span></p>
<button class="buy" onclick="add('Versace Eros','p3')">В корзину</button>
</div>

<!-- 4 -->
<div class="card product men">
<img src="https://images.unsplash.com/photo-1594035910387-fea47794261f">
<h3>Armani Code</h3>
<select onchange="update(this,'p4')">
<option value="379">30 ml — 379 грн</option>
<option value="529">50 ml — 529 грн</option>
<option value="729">100 ml — 729 грн</option>
</select>
<p>Ціна: <span id="p4">379</span></p>
<button class="buy" onclick="add('Armani Code','p4')">В корзину</button>
</div>

<!-- 5 -->
<div class="card product men">
<img src="https://images.unsplash.com/photo-1615381417851-0c9c0b8b0c52">
<h3>1 Million</h3>
<select onchange="update(this,'p5')">
<option value="399">30 ml — 399 грн</option>
<option value="549">50 ml — 549 грн</option>
<option value="749">100 ml — 749 грн</option>
</select>
<p>Ціна: <span id="p5">399</span></p>
<button class="buy" onclick="add('1 Million','p5')">В корзину</button>
</div>

<!-- 6 -->
<div class="card product men">
<img src="https://images.unsplash.com/photo-1616077168079-7a8f6a3a5a8a">
<h3>Boss Bottled</h3>
<select onchange="update(this,'p6')">
<option value="329">30 ml — 329 грн</option>
<option value="499">50 ml — 499 грн</option>
<option value="699">100 ml — 699 грн</option>
</select>
<p>Ціна: <span id="p6">329</span></p>
<button class="buy" onclick="add('Boss Bottled','p6')">В корзину</button>
</div>

<!-- 7 -->
<div class="card product women">
<img src="https://images.unsplash.com/photo-1615634260167-c8cdede054de">
<h3>YSL Y</h3>
<select onchange="update(this,'p7')">
<option value="449">30 ml — 449 грн</option>
<option value="599">50 ml — 599 грн</option>
<option value="799">100 ml — 799 грн</option>
</select>
<p>Ціна: <span id="p7">449</span></p>
<button class="buy" onclick="add('YSL Y','p7')">В корзину</button>
</div>

<!-- 8 -->
<div class="card product women">
<img src="https://images.unsplash.com/photo-1618354691373-d851c5c3a990">
<h3>Lacoste Blanc</h3>
<select onchange="update(this,'p8')">
<option value="299">30 ml — 299 грн</option>
<option value="449">50 ml — 449 грн</option>
<option value="649">100 ml — 649 грн</option>
</select>
<p>Ціна: <span id="p8">299</span></p>
<button class="buy" onclick="add('Lacoste Blanc','p8')">В корзину</button>
</div>

</div>
</div>

<div class="cart">
🛒 Товарів: <span id="count">0</span>
<br>
<button onclick="checkout()">Оформити</button>
</div>

<script>
let cart=[];

function update(sel,id){
document.getElementById(id).innerText=sel.value;
}

function add(name,id){
let price=document.getElementById(id).innerText;
cart.push(name+" - "+price+" грн");
document.getElementById("count").innerText=cart.length;
}

function checkout(){
if(cart.length===0){alert("Порожньо");return;}
let text="🛍 Замовлення:%0A";
cart.forEach(i=>text+=i+"%0A");
window.location.href="https://t.me/scrhnrr?text="+text;
}

function filter(type){
let items=document.querySelectorAll(".product");
items.forEach(i=>{
if(type==="all") i.style.display="block";
else if(i.classList.contains(type)) i.style.display="block";
else i.style.display="none";
});
}
</script>

</body>
</html>
