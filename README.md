# sorting-visualizer

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        canvas {
            border: 1px solid black;
        }
    </style>
    <title>Sorting Visualizer</title>
</head>
<body>
    <canvas id="sortingCanvas" width="800" height="400"></canvas>
    <button onclick="randomizeArray()">Randomize Array</button>
    <button onclick="insertionSort()">Insertion Sort</button>


    <script>
        const canvas = document.getElementById('sortingCanvas');
        const ctx = canvas.getContext('2d');
        const barWidth = 20;
        const barSpacing = 5;
        const numBars = 50;
        const barColor = 'blue';
        let bars = [];

        function drawBars() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            for (let i = 0; i < bars.length; i++) {
                ctx.fillStyle = barColor;
                ctx.fillRect(i * (barWidth + barSpacing), canvas.height - bars[i], barWidth, bars[i]);
            }
        }

        function randomizeArray() {
            bars = Array.from({ length: numBars }, () => Math.floor(Math.random() * (canvas.height - 10) + 10));
            drawBars();
        }

        function insertionSort() {

        }

        randomizeArray();
    </script>
</body>
</html>
