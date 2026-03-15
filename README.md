<!DOCTYPE html>
<html>
<head>
<title>Factorial Calculator</title>
<style>
body{
    font-family: Arial;
    text-align: center;
    margin-top: 100px;
    background: #f4f4f4;
}

.box{
    background: white;
    padding: 30px;
    display: inline-block;
    border-radius: 10px;
    box-shadow: 0 0 10px gray;
}

input{
    padding:10px;
    font-size:16px;
}

button{
    padding:10px 20px;
    font-size:16px;
    margin-top:10px;
    cursor:pointer;
}

#result{
    margin-top:20px;
    font-size:20px;
    font-weight:bold;
}
</style>
</head>

<body>

<div class="box">
<h2>Factorial Calculator</h2>

<input type="number" id="num" placeholder="Enter a number">

<br>

<button onclick="calculateFactorial()">Calculate</button>

<div id="result"></div>
</div>

<script>
function calculateFactorial(){
    let n = document.getElementById("num").value;
    
    if(n < 0){
        document.getElementById("result").innerText = "Factorial not defined for negative numbers";
        return;
    }

    let fact = 1;

    for(let i = 1; i <= n; i++){
        fact = fact * i;
    }

    document.getElementById("result").innerText = "Factorial = " + fact;
}
</script>

</body>
</html>
