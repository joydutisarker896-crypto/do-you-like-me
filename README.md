<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Do you like me?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: #f5f5f5;
        }

        .box {
            position: relative;
            width: 400px;
            height: 400px;
            background: white;
            border-radius: 10px;
            text-align: center;
            padding-top: 40px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }

        button {
            padding: 10px 25px;
            font-size: 16px;
            cursor: pointer;
        }

        #yes {
            margin-right: 20px;
        }

        #no {
            position: absolute;
        }
    </style>
</head>
<body>

<div class="box">
    <h2>Do you like me? ❤️</h2>
    <button id="yes">Yes 😊</button>
    <button id="no">No 😅</button>
</div>

<script>
    const noBtn = document.getElementById("no");
    const box = document.querySelector(".box");

    noBtn.addEventListener("mouseenter", () => {
        const maxX = box.clientWidth - noBtn.offsetWidth;
        const maxY = box.clientHeight - noBtn.offsetHeight;

        const x = Math.random() * maxX;
        const y = Math.random() * maxY;

        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    });

    document.getElementById("yes").addEventListener("click", () => {
        alert("Thanks for accepting ❤️");
    });
</script>

</body>
</html>
