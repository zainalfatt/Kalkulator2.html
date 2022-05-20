# Kalkulator2.html

<Style>
  #content{
    background:pink;
    color: purple;
    padding:10px;
    font-size:20px;
    font-weight:900;
    text-align:center;
    box-shadow:2px 2px 7px Black;
  }
    .tampil{
      box-shadow:inset 2px 2px 5px Black;
      color:Black;
      padding:10px;
      margin:10px 0px;
    }
    button{
      border:none;
      outline:none;
      padding:10px;
      margin:3px 0px;
      width: 50px;
      box-shadow: 2px 2px 5px black;
      font-size:15px;
      font-weight: 700;
      color:white;
    }
    button:active{
      box-shadow:inset 2px 2px 5px black;
    }
    .num{
      background:blue;
    }
    .opr{
      background:red;
    }
</Style>
<div id="content">
  Kalkulator Sederhana <br>
  By:<br>
  Zainal Fattah 
  <div id="hasil"class="tampil">Hasil</div>
  <div id="rumus"class="tampil"contenteditable="true"onkeyup="hitung()"></div>
  <button class="num"onclick="rumus.innerHTML+='1' ; hitung()">1</button>
  <button class="num"onclick="rumus.innerHTML+='2' ; hitung()">2</button>
  <button class="num"onclick="rumus.innerHTML+='3' ; hitung()">3</button>
  <button class="opr"onclick="rumus.innerHTML+='+' ; hitung()">+</button>
  <br>
<button class="num"onclick="rumus.innerHTML+='4' ; hitung()">4</button>
  <button class="num"onclick="rumus.innerHTML+='5' ; hitung()">5</button>
  <button class="num"onclick="rumus.innerHTML+='6' ; hitung()">6</button>
  <button class="opr"onclick="rumus.innerHTML+='-' ; hitung()">-</button>
  <br>
<button class="num"onclick="rumus.innerHTML+='7' ; hitung()">7</button>
  <button class="num"onclick="rumus.innerHTML+='8' ; hitung()">8</button>
  <button class="num"onclick="rumus.innerHTML+='9' ; hitung()">9</button>
  <button class="opr"onclick="rumus.innerHTML+='*' ; hitung()">×</button>
  <br>
<button class="opr"onclick="rumus.innerHTML+='(' ; hitung()">(</button>
  <button class="num"onclick="rumus.innerHTML+='0' ; hitung()">0</button>
  <button class="opr"onclick="rumus.innerHTML+=')' ; hitung()">)</button>
  <button class="opr"onclick="rumus.innerHTML+='/' ; hitung()">÷</button>
  <br>
  <button class="opr"onclick="rumus.innerHTML+='.' ; hitung()">.</button>
  <button class="opr"onclick="rumus.innerHTML='' ; hitung()">C</button>
  <button class="opr"onclick="rumus.innerHTML=rumus.innerHTML.slice(0,-1) ; hitung()">D</button>
  <br>
  
  
</div>
<script>
  function hitung(){
    if(rumus.innerHTML==""){
      hasil.innerHTML="hasil";}else{
        hasil.innerHTML=eval(rumus.innerHTML);
    }
  }
</script>
