# ynico
Un increíble juego en el que recuerdas que te amo mucho, Nico.
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tetris Te Amo Nico</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="game-container">
        <div class="tetris-grid" id="grid"></div>
    </div>
    <script src="script.js"></script>
</body>
</html>
body {
    background-color: #FFC0CB;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.game-container {
    background-color: #FF69B4;
    padding: 20px;
    border-radius: 10px;
}

.tetris-grid {
    display: grid;
    grid-template-columns: repeat(10, 30px);
    grid-template-rows: repeat(20, 30px);
    border: 2px solid #FF1493;
}

.tetris-grid div {
    width: 30px;
    height: 30px;
    border: 1px solid #FF69B4;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 12px;
    color: white;
    background-color: #FF69B4;
}

.te-amo-nico {
    background-color: #FF69B4;
    color: white;
}
document.addEventListener('DOMContentLoaded', () => {
    const grid = document.getElementById('grid');
    let squares = Array.from(grid.querySelectorAll('div'));
    const width = 10;
    const height = 20;
    const teAmoNicoBlock = ["T", "e", " ", "A", "m", "o", " ", "N", "i", "c", "o"];

    function draw() {
        for (let i = 0; i < squares.length; i++) {
            if (i >= width * (height - 1)) {
                squares[i].classList.add('te-amo-nico');
                squares[i].innerText = teAmoNicoBlock[i - width * (height - 1)];
            }
        }
    }

    draw();
});
