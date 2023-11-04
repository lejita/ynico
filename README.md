# ynico

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
