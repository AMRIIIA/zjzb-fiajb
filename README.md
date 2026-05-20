<!DOCTYPE html>
<html lang="ro">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Acces platformă</title>
<style>
body {
    font-family: Arial, sans-serif;
    background: #0f172a;
    color: white;
    text-align: center;
    margin: 0;
    padding: 20px;
}
.container {
    max-width: 400px;
    margin: auto;
}
h1 {
    font-size: 22px;
}
.btn {
    display: block;
    background: #22c55e;
    color: white;
    padding: 15px;
    margin: 10px 0;
    text-decoration: none;
    border-radius: 8px;
    font-size: 16px;
}
.btn:hover {
    background: #16a34a;
}
.hidden {
    display: none;
}
</style>
</head>

<body>

<div class="container">

    <!-- STEP 1 -->
    <div id="step1">
        <h1>Platformă nouă pentru români</h1>
        <p>Ai peste 18 ani?</p>
        <a class="btn" onclick="nextStep(2)">Da</a>
        <a class="btn" onclick="nextStep(2)">Nu</a>
    </div>

    <!-- STEP 2 -->
    <div id="step2" class="hidden">
        <h1>Experiență</h1>
        <p>Ai mai jucat la cazinou online?</p>
        <a class="btn" onclick="nextStep(3)">Da</a>
        <a class="btn" onclick="nextStep(3)">Nu</a>
    </div>

    <!-- STEP 3 -->
    <div id="step3" class="hidden">
        <h1>Câștig</h1>
        <p>Cât vrei să câștigi lunar?</p>
        <a class="btn" onclick="nextStep(4)">500€</a>
        <a class="btn" onclick="nextStep(4)">1000€</a>
        <a class="btn" onclick="nextStep(4)">3000€+</a>
    </div>

    <!-- FINAL -->
    <div id="step4" class="hidden">
        <h1>Felicitări!</h1>
        <p>Ai fost selectat pentru acces.</p>
        <a class="btn" href="https://1wthlj.life/casino?p=ekxe">Intră acum</a>
    </div>

</div>

<script>
function nextStep(step) {
    document.querySelectorAll("div[id^='step']").forEach(el => el.classList.add("hidden"));
    document.getElementById("step" + step).classList.remove("hidden");
}
</script>

</body>
</html>