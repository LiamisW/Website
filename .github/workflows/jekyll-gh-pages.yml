<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Key System</title>
    <style>
        body {
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: rgb(23, 23, 23);
            font-family: Arial, sans-serif;
            color: white;
        }

        .container {
            position: relative;
            text-align: center;
        }

        canvas {
            border-radius: 20px;
            background-color: #333;
            border: 2px solid #444;
        }

        #keyInput {
            position: absolute;
            top: 100px;
            left: 100px;
            width: 200px;
            padding: 10px;
            font-size: 16px;
            border: 2px solid gray;
            outline: none;
            border-radius: 5px;
            transition: border-color 0.3s;
            background: #222;
            color: white;
        }

        #keyInput:focus {
            border-color: #00b4d8;
        }

        #submitButton {
            position: absolute;
            top: 170px;
            left: 150px;
            padding: 5px 10px;
            font-size: 14px;
            border: none;
            border-radius: 5px;
            background-color: #00b4d8;
            color: white;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        #submitButton:hover {
            background-color: #0077a3;
        }

        .message {
            margin-top: 10px;
            font-size: 18px;
            opacity: 0;
            transition: opacity 0.5s;
        }

        .message.show {
            opacity: 1;
        }
    </style>
</head>
<body>
    <div class="container">
        <canvas id="myCanvas" width="400" height="300"></canvas>
        <input type="text" id="keyInput" placeholder="Enter Key">
        <button id="submitButton">Submit</button>
        <div class="message" id="message">Key accepted! You now have access to our Executor.</div>
    </div>

    <script>
        const canvas = document.getElementById('myCanvas');
        const ctx = canvas.getContext('2d');
        const keyInput = document.getElementById('keyInput');
        const submitButton = document.getElementById('submitButton');
        const message = document.getElementById('message');
        const correctKey = 'FluxWare-OnTop-AdminKey';

        // Draw rounded rectangle on canvas
        function drawRoundedRect(x, y, width, height, radius) {
            ctx.beginPath();
            ctx.moveTo(x + radius, y);
            ctx.lineTo(x + width - radius, y);
            ctx.quadraticCurveTo(x + width, y, x + width, y + radius);
            ctx.lineTo(x + width, y + height - radius);
            ctx.quadraticCurveTo(x + width, y + height, x + width - radius, y + height);
            ctx.lineTo(x + radius, y + height);
            ctx.quadraticCurveTo(x, y + height, x, y + height - radius);
            ctx.lineTo(x, y + radius);
            ctx.quadraticCurveTo(x, y, x + radius, y);
            ctx.closePath();
            ctx.fillStyle = '#333';
            ctx.fill();
            ctx.strokeStyle = '#444';
            ctx.lineWidth = 2;
            ctx.stroke();
        }

        // Draw the label inside the canvas
        function drawLabel() {
            ctx.fillStyle = 'white';
            ctx.font = '24px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('Key System', canvas.width / 2, 50);
        }

        // Initial drawing
        function drawUI() {
            drawRoundedRect(0, 0, canvas.width, canvas.height, 20);
            drawLabel();
        }

        // Check the key input when the button is clicked
        function checkKey() {
            const key = keyInput.value.trim();
            if (key === correctKey) {
                message.textContent = 'Key accepted! You now have access to our Executor.';
                message.classList.add('show');
            } else {
                message.textContent = 'Incorrect Key. Please try again.';
                message.classList.add('show');
            }
        }

        // Event listener for the submit button
        submitButton.addEventListener('click', () => {
            checkKey();
            keyInput.value = ''; // Clear the input after checking
        });

        // Initial UI draw
        drawUI();
    </script>
</body>
</html>
