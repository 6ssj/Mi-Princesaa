<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Apresentação de América do Sul</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        .slide {
            display: none;
            width: 100%;
            height: 100vh;
            position: relative;
            padding: 20px;
            box-sizing: border-box;
            background-color: white;
        }
        .slide.active {
            display: block;
        }
        .title {
            font-size: 48px;
            text-align: center;
            text-shadow: 2px 2px 4px rgba(0, 128, 0, 0.5);
            color: green;
            margin-bottom: 20px;
        }
        .map {
            float: right;
            width: 50%;
            height: auto;
        }
        .button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 20px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 16px;
            margin: 4px 2px;
            cursor: pointer;
            border-radius: 5px;
        }
        .button.dark {
            background-color: #2E8B57;
        }
        .marvel {
            animation: slideIn 1s ease-in-out;
            margin-bottom: 20px;
        }
        @keyframes slideIn {
            from { transform: translateX(-100%); }
            to { transform: translateX(0); }
        }
        .photo {
            width: 300px;
            height: auto;
            margin: 10px;
        }
        .highlight {
            color: #32CD32;
            text-decoration: underline;
            cursor: pointer;
        }
        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.4);
        }
        .modal-content {
            background-color: #fefefe;
            margin: 15% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 80%;
            text-align: center;
        }
        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
        }
        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
        .zoom {
            transition: transform 0.5s;
        }
        .zoom:hover {
            transform: scale(1.2);
        }
        .end {
            text-align: center;
            font-size: 36px;
        }
        .credits {
            position: absolute;
            bottom: 10px;
            left: 10px;
            font-size: 12px;
        }
    </style>
</head>
<body>
    <div id="slide1" class="slide active">
        <h1 class="title">Apresentação de América do Sul</h1>
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0f/South_America_%28orthographic_projection%29.svg/400px-South_America_%28orthographic_projection%29.svg.png" alt="Mapa de América do Sul" class="map">
        <button class="button" onclick="nextSlide()">Próximo</button>
    </div>

<div id="slide2" class="slide">
        <h2>Países e Capitais de América do Sul</h2>
        <ul>
            <li>Brasil - Brasília</li>
            <li>Argentina - Buenos Aires</li>
            <li>Colômbia - Bogotá</li>
            <li>Peru - Lima</li>
            <li>Venezuela - Caracas</li>
            <li>Chile - Santiago</li>
            <li>Equador - Quito</li>
            <li>Bolívia - Sucre (capital constitucional), La Paz (capital administrativa)</li>
            <li>Paraguai - Assunção</li>
            <li>Uruguai - Montevideu</li>
            <li>Guiana - Georgetown</li>
            <li>Suriname - Paramaribo</li>
            <li>Guiana Francesa - Caiena (território francês)</li>
        </ul>
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4a/South_America_political_map.svg/400px-South_America_political_map.svg.png" alt="Mapa político de América do Sul" style="width: 100%;">
        <button class="button" onclick="prevSlide()">Anterior</button>
        <button class="button" onclick="nextSlide()">Próximo</button>
    </div>

<div id="slide3" class="slide">
        <h2>Clima de América do Sul</h2>
        <p>No norte, o clima é equatorial, com chuvas abundantes e temperaturas altas, como na Amazónia. No sul, é temperado, com estações bem definidas, como na Argentina e no Chile. Nas regiões andinas, é alpino, frio e seco. A costa oeste tem clima desértico, enquanto a leste é mais húmido.</p>
        <button class="button" onclick="prevSlide()">Anterior</button>
        <button class="button" onclick="nextSlide()">Próximo</button>
    </div>

 <div id="slide4" class="slide">
        <h2>Maravilhas de América do Sul</h2>
        <div id="marvel1" class="marvel">
            <h3>Machu Picchu (Peru)</h3>
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/eb/Machu_Picchu%2C_Peru.jpg/400px-Machu_Picchu%2C_Peru.jpg" alt="Machu Picchu" class="photo">
            <button class="button dark" onclick="nextMarvel()">Próxima Maravilha</button>
        </div>
        <div id="marvel2" class="marvel" style="display: none;">
            <h3>Cataratas de Iguazú (Brasil e Argentina)</h3>
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Iguazu_Falls.jpg/400px-Iguazu_Falls.jpg" alt="Cataratas de Iguazú" class="photo">
            <button class="button dark" onclick="nextMarvel()">Próxima Maravilha</button>
        </div>
        <div id="marvel3" class="marvel" style="display: none;">
            <h3>Amazónia (Brasil, Peru, Colômbia, etc.)</h3>
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/8a/Amazon_rainforest.jpg/400px-Amazon_rainforest.jpg" alt="Amazónia" class="photo">
        </div>
        <button class="button" onclick="prevSlide()">Anterior</button>
        <button class="button" onclick="nextSlide()">Próximo</button>
    </div>

<div id="slide5" class="slide">
        <h2>Limites Naturais de América do Sul</h2>
        <button class="button zoom" onclick="zoomLimit('norte')">Norte: Oceano Atlântico e Mar do Caribe</button>
        <button class="button zoom" onclick="zoomLimit('oeste')">Oeste: Oceano Pacífico</button>
        <button class="button zoom" onclick="zoomLimit('este')">Este: Oceano Atlântico</button>
        <button class="button zoom" onclick="zoomLimit('sul')">Sul: Oceano Atlântico e Estreito de Magalhães</button>
        <div id="limitInfo"></div>
        <button class="button" onclick="prevSlide()">Anterior</button>
        <button class="button" onclick="nextSlide()">Próximo</button>
    </div>

   <div id="slide6" class="slide">
        <h2>Curiosidades Geográficas</h2>
        <p>A América do Sul é dominada pela <span class="highlight" onclick="showModal('andes')">Cordilheira dos Andes</span>, a mais longa do mundo, com picos como o <span class="highlight" onclick="showModal('aconcagua')">Aconcágua</span> e o <span class="highlight" onclick="showModal('ojos')">Ojos del Salado</span>, abrangendo vários países. Os rios principais incluem o <span class="highlight" onclick="showModal('amazonas')">Amazonas</span>, <span class="highlight" onclick="showModal('parana')">Paraná</span> e <span class="highlight" onclick="showModal('orinoco')">Orinoco</span>. As ilhas notáveis são as <span class="highlight" onclick="showModal('galapagos')">Galápagos (Equador)</span> e as <span class="highlight" onclick="showModal('falkland')">Falkland/Malvinas (território disputado)</span>, além de algumas na costa, como a <span class="highlight" onclick="showModal('marajo')">Ilha de Marajó</span>.</p>
        <button class="button" onclick="prevSlide()">Anterior</button>
        <button class="button" onclick="nextSlide()">Próximo</button>
    </div>

<div id="slide7" class="slide">
        <h2>Microestados em América do Sul</h2>
        <p>Não existem microestados em América do Sul, mas existem países muito pequenos como o Suriname, o Uruguai e a Guiana. A Guiana não é um território 100% independente; é um território que depende da França.</p>
        <button class="button" onclick="prevSlide()">Anterior</button>
        <button class="button" onclick="nextSlide()">Próximo</button>
    </div>

<div id="slide8" class="slide">
        <h2>Conclusão</h2>
        <p>Esta apresentação cobriu os principais aspetos de América do Sul, desde a sua geografia até às suas maravilhas.</p>
        <button class="button" onclick="prevSlide()">Anterior</button>
        <button class="button" onclick="nextSlide()">Próximo</button>
    </div>

<div id="slide9" class="slide">
        <div class="end">Fim</div>
        <div class="credits">Federico Aguilera Nº4<br>João Silva Nº7<br>Zi Chen Nº14</div>
        <button class="button" onclick="prevSlide()">Anterior</button>
    </div>

div id="myModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <div id="modalContent"></div>
        </div>
    </div>

<script>
        let currentSlide = 1;
        let currentMarvel = 1;

        function nextSlide() {
            document.getElementById('slide' + currentSlide).classList.remove('active');
            currentSlide++;
            if (currentSlide > 9) currentSlide = 9;
            document.getElementById('slide' + currentSlide).classList.add('active');
        }

        function prevSlide() {
            document.getElementById('slide' + currentSlide).classList.remove('active');
            currentSlide--;
            if (currentSlide < 1) currentSlide = 1;
            document.getElementById('slide' + currentSlide).classList.add('active');
        }

        function nextMarvel() {
            document.getElementById('marvel' + currentMarvel).style.display = 'none';
            currentMarvel++;
            if (currentMarvel > 3) currentMarvel = 3;
            document.getElementById('marvel' + currentMarvel).style.display = 'block';
        }

        function zoomLimit(limit) {
            const info = {
                norte: 'Norte: Oceano Atlântico e Mar do Caribe, limitando com países como a Colômbia e a Venezuela.',
                oeste: 'Oeste: Oceano Pacífico, limitando com o Chile e o Peru.',
                este: 'Este: Oceano Atlântico, limitando com o Brasil e a Argentina.',
                sul: 'Sul: Oceano Atlântico e Estreito de Magalhães, limitando com a Argentina e o Chile.'
            };
            document.getElementById('limitInfo').innerHTML = info[limit];
        }

        function showModal(place) {
            const content = {
                andes: '<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Andes.jpg/400px-Andes.jpg" class="photo"><br>Cordilheira dos Andes',
                aconcagua: '<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9b/Aconcagua.jpg/400px-Aconcagua.jpg" class="photo"><br>Aconcágua',
                ojos: '<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0f/Ojos_del_Salado.jpg/400px-Ojos_del_Salado.jpg" class="photo"><br>Ojos del Salado',
                amazonas: '<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/8a/Amazon_river.jpg/400px-Amazon_river.jpg" class="photo"><br>Rio Amazonas',
                parana: '<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4a/Parana_River.jpg/400px-Parana_River.jpg" class="photo"><br>Rio Paraná',
                orinoco: '<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3e/Orinoco_River.jpg/400px-Orinoco_River.jpg" class="photo"><br>Rio Orinoco',
                galapagos: '<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2b/Galapagos_Islands.jpg/400px-Galapagos_Islands.jpg" class="photo"><br>Ilhas Galápagos',
                falkland: '<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/8c/Falkland_Islands.jpg/400px-Falkland_Islands.jpg" class="photo"><br>Ilhas Falkland/Malvinas',
                marajo: '<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1e/Maraj%C3%B3_Island.jpg/400px-Maraj%C3%B3_Island.jpg" class="photo"><br>Ilha de Marajó'
            };
            document.getElementById('modalContent').innerHTML = content[place];
            document.getElementById('myModal').style.display = 'block';
        }

        function closeModal() {
            document.getElementById('myModal').style.display = 'none';
        }
    </script>
</body>
</html>
