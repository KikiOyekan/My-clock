<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clock</title>
    <link rel="stylesheet" href="game.css">
</head>
<body>
    <div class="clock">
        <div class="hour-hand" id="hour-hand"></div>
        <div class="minute-hand" id="minute-hand"></div>
        <div class="second-hand" id="second-hand"></div>
        <div class="center-circle"></div>
    </div>
    <script >function updateClock() {
    const now = new Date();
    const hour = now.getHours() % 12;
    const minute = now.getMinutes();
    const second = now.getSeconds();
l
    const hourAngle = (hour * 30) + (minute / 2);
    const minuteAngle = (minute * 6) + (second / 10);
    const secondAngle = second * 6; const hourHand = document.getElementById('hour-hand');
    const minuteHand = document.getElementById('minute-hand');
    const secondHand = document.getElementById('second-hand');
 hourHand.style.transform = `rotate(${hourAngle}deg)`;
    minuteHand.style.transform = `rotate(${minuteAngle}deg)`;
    secondHand.style.transform = `rotate(${secondAngle}deg)`;
}
updateClock();
setInterval(updateClock, 1000);
</script>
</body>
</html
