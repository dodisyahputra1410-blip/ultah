# ultah
hbd
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Aina 🎉</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

body{
    background:linear-gradient(135deg,#ff9a9e,#fad0c4);
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    overflow:hidden;
}

.container{
    background:white;
    padding:30px;
    border-radius:20px;
    width:90%;
    max-width:500px;
    box-shadow:0 10px 30px rgba(0,0,0,0.2);
}

h1{
    color:#ff4081;
    margin-bottom:15px;
}

p{
    color:#555;
    margin-bottom:20px;
}

button{
    padding:12px 20px;
    border:none;
    border-radius:10px;
    cursor:pointer;
    margin:5px;
    font-size:16px;
    transition:0.3s;
}

button:hover{
    transform:scale(1.05);
}

.btn1{
    background:#ff4081;
    color:white;
}

.btn2{
    background:#7c4dff;
    color:white;
}

.btn3{
    background:#00c853;
    color:white;
}

#result{
    margin-top:20px;
    font-size:18px;
    font-weight:bold;
    color:#ff4081;
}

.heart{
    position:absolute;
    font-size:24px;
    animation:fall 4s linear infinite;
}

@keyframes fall{
    from{
        transform:translateY(-100px);
    }
    to{
        transform:translateY(100vh);
    }
}
</style>
</head>
<body>

<div class="container">
    <h1>🎂 Happy Birthday Aina 🎂</h1>

    <p>Pilih salah satu tombol di bawah ya 😊</p>

    <button class="btn1" onclick="wish()">🎁 Buka Hadiah</button>
    <button class="btn2" onclick="message()">💌 Pesan Rahasia</button>
    <button class="btn3" onclick="surprise()">✨ Kejutan</button>

    <div id="result"></div>
</div>

<script>
function wish(){
    document.getElementById("result").innerHTML =
    "🎉 Selamat Ulang Tahun Aina! Semoga selalu dilimpahkan kebahagiaan di setiap langkah yang dijalani ❤️";
}

function message(){
    document.getElementById("result").innerHTML =
    "💖 Hari ini spesial karena Aina bertambah usia. Semoga semua impian dan harapan segera terwujud.";
}

function surprise(){
    document.getElementById("result").innerHTML =
    "🎊 Surprise! Semoga sehat selalu, panjang umur, dan selalu dikelilingi orang-orang baik.";
    
    for(let i=0;i<30;i++){
        let heart=document.createElement("div");
        heart.className="heart";
        heart.innerHTML="🎈";
        heart.style.left=Math.random()*100+"vw";
        heart.style.animationDuration=(Math.random()*3+2)+"s";
        document.body.appendChild(heart);

        setTimeout(()=>{
            heart.remove();
        },5000);
    }
}
</script>

</body>
</html>