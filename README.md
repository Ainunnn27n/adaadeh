<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Day</title>
    <style>
        body { font-family: Arial, sans-serif; }
        .love-section { font-size: 24px; color: red; }
        .quote { margin: 20px 0; }
        .countdown { font-size: 30px; color: green; }
    </style>
</head>
<body>
    <header>
        <h1>Happy Valentine's Day</h1>
    </header>
    <section class="love-section">
        <h2>Love is in the air!</h2>
        <p>Celebrate love and companionship.</p>
    </section>
    <section class="quotes">
        <div class="quote">
            <blockquote>"Where there is love, there is life." - Mahatma Gandhi</blockquote>
        </div>
        <div class="quote">
            <blockquote>"Love all, trust a few, do wrong to none." - William Shakespeare</blockquote>
        </div>
    </section>
    <section class="countdown">
        <h2>Countdown to Valentine's Day!</h2>
        <div id="timer"></div>
    </section>
    <section class="confession-form">
        <h2>Confession Form</h2>
        <form>
            <label for="name">Your Name:</label>
            <input type="text" id="name" name="name" required>
            <label for="confession">Your Confession:</label>
            <textarea id="confession" name="confession" required></textarea>
            <button type="submit">Submit</button>
        </form>
    </section>
    <script>
        const countDownDate = new Date("2026-02-14T00:00:00").getTime();
        const timer = setInterval(function() {
            const now = new Date().getTime();
            const distance = countDownDate - now;
            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);
            document.getElementById("timer").innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s`;
            if (distance < 0) {
                clearInterval(timer);
                document.getElementById("timer").innerHTML = "EXPIRED";
            }
        }, 1000);
    </script>
</body>
</html>
