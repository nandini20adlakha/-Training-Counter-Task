# -Training-Counter-Task
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DAY 7(TRAINIING)</title>
    <link rel="stylesheet" href="day7.css">
</head>
<body>
    <h1 id="counter">counter:0</h1>
    <button onclick="StartCounter()">start</button>
    <button onclick="PauseCounter()">pause</button>
    <button onclick="ResetCounter()">reset</button>
    <script src="day7.js"></script>
</body>
</html>
CSS
body{
    background-color: rgb(247, 237, 148);
    text-align: center;
}
JS
console.log("-----welcome in JS-----")
//counter task
let counter=0;
let intervalID=null;
const element=document.getElementById("counter")
function startInterval(){
    intervalID=setInterval(function() {
        counter++;
        element.innerText="Counter:"+counter
    },1000)
}
function StartCounter(){
    console.log('start counter')
    startInterval()
}
function PauseCounter(){
    console.log("Pause Counter")
    clearInterval(intervalID)
    intervalID=null
}
function ResetCounter(){
   console.log('Reset Counter')
   if(intervalID)PauseCounter()
   element.innerText="Counter:"+0
   counter=0
}
