<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>💘 1 Month Together 💘</title>
    <style>
        body {
            background-color: #000000;
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px 0;
        }

        h1 {
            font-size: 60px;
            color: #FF0000;
            margin-bottom: 20px;
        }

        p {
            font-size: 25px;
            color: #FF0000;
            margin-top: 0;
        }

        .name {
            font-size: 25px;
            color: #FF0000;
            margin-top: 50px;
        }

        #countdown {
            font-size: 33px;
            color: #000000;
            margin-top: 50px;
        }
    </style>
</head>
<body>
    <h1>🥰 Happy one month baby 🥰</h1>
    <p> To many more months years always and forever, Together is a beautiful place to be.</p>
    <div class="name">💘 from your boyfriend
        💘</div>
    <div id="countdown"></div>
    <script>
        const countdown = document.getElementById('countdown');
        const targetDate = new Date('2024-02-03T17:40:00');
        const startDate = new Date('2023-12-31T03:00:00');
        const days = document.createElement('span');
        const hours = document.createElement('span');
        const minutes = document.createElement('span');
        const seconds = document.createElement('span');
        days.textContent = '00';
        hours.textContent = '00';
        minutes.textContent = '00';
        seconds.textContent = '00';
        countdown.appendChild(days);
        countdown.appendChild(document.createTextNode(' days '));
        countdown.appendChild(hours);
        countdown.appendChild(document.createTextNode(' hours '));
        countdown.appendChild(minutes);
        countdown.appendChild(document.createTextNode(' minutes '));
        countdown.appendChild(seconds);

        function updateCountdown() {
            const currentDate = new Date();
            const remainingTime = targetDate - currentDate;
            const elapsedTime = currentDate - startDate;
            const totalDays = Math.floor(elapsedTime / (1000 * 60 * 60 * 24));
            const remainingSeconds = Math.floor(remainingTime / 1000);
            const remainingMinutes = Math.floor(remainingSeconds / 60);
            const remainingHours = Math.floor(remainingMinutes / 60);
            days.textContent = totalDays.toString().padStart(2, '0');
            hours.textContent = (remainingHours % 24).toString().padStart(2, '0');
            minutes.textContent = (remainingMinutes % 60).toString().padStart(2, '0');
            seconds.textContent = (remainingSeconds % 60).toString().padStart(2, '0');
        }

        updateCountdown();
        setInterval(updateCountdown, 1000);
    </script>
</body>
</html>
