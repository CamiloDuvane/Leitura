<html><head><base href="https://camiloduvane.github.io/Leitura/">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minha história, Nosso Mundo - Histórias Completas</title>
    <style>
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f0f8ff;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #ff69b4;
            color: #fff;
            text-align: center;
            padding: 2rem 0;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        h1 {
            margin: 0;
            font-size: 2.5rem;
            text-shadow: 2px 2px #ff1493;
        }
        nav {
            background-color: #ff1493;
            padding: 1rem 0;
        }
        nav ul {
            list-style-type: none;
            padding: 0;
            margin: 0;
            display: flex;
            justify-content: center;
        }
        nav ul li {
            margin: 0 1rem;
        }
        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
        }
        #navUserName {
            font-weight: normal;
            font-style: italic;
            margin-left: 5px;
        }
        #adminPanelButton {
            background-color: #4169e1;
            color: #fff;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            text-decoration: none;
        }
        #adminPanelButton:hover {
            background-color: #1e90ff;
        }
        main {
            max-width: 800px;
            margin: 2rem auto;
            padding: 0 1rem;
        }
        .content-wrapper {
            display: block;
            max-width: 100%;
            margin: 0;
        }
        .left-column {
            width: 100%;
            padding: 0;
        }
        .right-column {
            display: none;
        }
        #highlightedNews {
            position: relative;
            width: 100%;
            max-width: 100%;
            margin: 0;
            padding: 40px;
            background-color: #fff;
            border-radius: 0;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        #highlightedNews h3 {
            text-align: center;
            color: #ff1493;
            font-size: 1.8rem;
            margin-bottom: 20px;
        }
        .news-carousel {
            width: 100%;
            overflow: hidden;
        }
        .news-slider {
            display: flex;
            transition: transform 0.5s ease;
        }
        .news-item {
            flex: 0 0 100%;
            padding: 0 20px;
            box-sizing: border-box;
            text-align: center;
        }
        .news-image {
            width: 100%;
            height: 400px;
            object-fit: cover;
            border-radius: 10px;
            margin-bottom: 20px;
        }
        .news-item h4 {
            color: #ff1493;
            font-size: 1.2rem;
            margin-bottom: 10px;
        }
        .news-item p {
            margin-bottom: 15px;
        }
        .read-more {
            display: inline-block;
            background-color: #ff69b4;
            color: #fff;
            padding: 8px 15px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s ease;
        }
        .read-more:hover {
            background-color: #ff1493;
        }
        .carousel-controls {
            position: absolute;
            top: 50%;
            left: 20px;
            right: 20px;
            display: flex;
            justify-content: space-between;
            transform: translateY(-50%);
            z-index: 10;
        }
        .prev-btn, .next-btn {
            background-color: rgba(255, 105, 180, 0.7);
            color: white;
            border: none;
            padding: 10px 15px;
            font-size: 18px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .prev-btn:hover, .next-btn:hover {
            background-color: rgba(255, 20, 147, 0.9);
        }
        .story-highlights {
            background-color: #ffe4e1;
            border-radius: 10px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .story-highlights h2 {
            color: #ff1493;
            font-size: 2rem;
            margin-top: 0;
            text-align: center;
        }
        .story-highlights ul {
            list-style-type: none;
            padding: 0;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }
        .story-highlights li {
            margin: 0.5rem;
        }
        .introduction {
            background-color: #fff;
            border-radius: 10px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .story {
            background-color: #fff;
            border-radius: 10px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .story h2 {
            color: #ff1493;
            font-size: 2rem;
            margin-top: 0;
        }
        .story img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            margin-bottom: 1rem;
        }
        .moral {
            font-style: italic;
            color: #4b0082;
            margin-top: 1rem;
            font-weight: bold;
        }
        .interpretation-questions {
            background-color: #e6f2ff;
            border-radius: 10px;
            padding: 1rem;
            margin-top: 1rem;
        }
        .interpretation-questions h3 {
            color: #ff1493;
            margin-top: 0;
        }
        .interpretation-questions .question {
            margin-bottom: 1rem;
        }
        .interpretation-questions .options {
            display: flex;
            flex-direction: column;
            margin-left: 1rem;
        }
        .interpretation-questions label {
            margin-bottom: 0.5rem;
            cursor: pointer;
        }
        .interpretation-questions input[type="radio"] {
            margin-right: 0.5rem;
        }
        .interpretation-questions ol {
            padding-left: 1.5rem;
        }
        .interpretation-questions li {
            margin-bottom: 0.5rem;
        }
        .read-button {
            background-color: #ff1493;
            color: #fff;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: background-color 0.3s ease;
        }
        .read-button:hover {
            background-color: #ff69b4;
        }
        #loginForm, #registerForm {
            background-color: #fff;
            border-radius: 10px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        #registerForm {
            display: none;
        }
        .form-group {
            margin-bottom: 1rem;
        }
        label {
            display: block;
            margin-bottom: 0.5rem;
        }
        input[type="text"], input[type="password"], input[type="number"], select {
            width: 100%;
            padding: 0.5rem;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button[type="submit"], #showRegisterFormButton {
            background-color: #ff1493;
            color: #fff;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: background-color 0.3s ease;
        }
        button[type="submit"]:hover, #showRegisterFormButton:hover {
            background-color: #ff69b4;
        }
        #userProfile {
            background-color: #fff;
            border-radius: 10px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        #userProfile h2 {
            color: #ff1493;
            font-size: 2rem;
            margin-top: 0;
        }
        #userProfile ul {
            list-style-type: none;
            padding: 0;
            display: none;
        }
        #profileInfo {
            display: none;
            list-style-type: none;
            padding: 0;
            margin: 10px 0;
            background-color: #fff;
            border-radius: 5px;
            padding: 15px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        #userProfile li {
            margin-bottom: 0.5rem;
        }
        #editProfileForm {
            margin-top: 1rem;
        }
        #logoutButton {
            background-color: #ff4500;
            color: #fff;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: background-color 0.3s ease;
        }
        #logoutButton:hover {
            background-color: #ff6347;
        }
        #adminPanel {
            background-color: #fff;
            border-radius: 10px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        #adminPanel h2 {
            color: #ff1493;
            font-size: 2rem;
            margin-top: 0;
        }
        #adminPanel ul {
            list-style-type: none;
            padding: 0;
        }
        #adminPanel li {
            margin-bottom: 0.5rem;
        }
        .admin-button {
            background-color: #4169e1;
            color: #fff;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: background-color 0.3s ease;
            margin-right: 0.5rem;
        }
        .admin-button:hover {
            background-color: #1e90ff;
        }
        footer {
            background-color: #ff69b4;
            color: #fff;
            text-align: center;
            padding: 1rem 0;
            margin-top: 2rem;
        }
        .social-links {
            display: flex;
            justify-content: center;
            margin-top: 1rem;
        }
        .social-links a {
            color: #fff;
            font-size: 1.5rem;
            margin: 0 0.5rem;
            text-decoration: none;
        }
        #loginOverlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.7);
            z-index: 1000;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        #loginForm {
            background-color: #fff;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            max-width: 400px;
            width: 90%;
        }
        #loginForm h2 {
            color: #ff1493;
            text-align: center;
            margin-bottom: 1.5rem;
        }
        #loginForm .form-group {
            margin-bottom: 1rem;
        }
        #loginForm label {
            display: block;
            margin-bottom: 0.5rem;
            color: #333;
        }
        #loginForm input[type="text"],
        #loginForm input[type="password"] {
            width: 100%;
            padding: 0.5rem;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        #loginForm button {
            width: 100%;
            padding: 0.75rem;
            background-color: #ff1493;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            margin-top: 1rem;
        }
        #loginForm button:hover {
            background-color: #ff69b4;
        }
        #showRegisterFormButton {
            background-color: transparent;
            color: #ff1493;
            border: none;
            cursor: pointer;
            text-decoration: underline;
            margin-top: 1rem;
            display: block;
            text-align: center;
        }
        #showRegisterFormButton:hover {
            color: #ff69b4;
        }
        #closeLoginButton {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: transparent;
            border: none;
            color: #fff;
            font-size: 24px;
            cursor: pointer;
        }
        #storyModal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.4);
        }
        .modal-content {
            background-color: #fefefe;
            margin: 5% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 80%;
            max-width: 800px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }
        .close:hover,
        .close:focus {
            color: #000;
            text-decoration: none;
            cursor: pointer;
        }
        #modalTitle {
            color: #ff1493;
            font-size: 2rem;
            text-align: center;
            margin-bottom: 20px;
        }
        #modalContent {
            text-align: justify;
            line-height: 1.6;
        }
        #modalContent p {
            margin-bottom: 15px;
        }
        #registerForm {
            background-color: #fff;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            max-width: 400px;
            width: 90%;
        }
        #registerForm h2 {
            color: #ff1493;
            text-align: center;
            margin-bottom: 1.5rem;
        }
        #registerForm .form-group {
            margin-bottom: 1rem;
        }
        #registerForm label {
            display: block;
            margin-bottom: 0.5rem;
            color: #333;
        }
        #registerForm input[type="text"],
        #registerForm input[type="password"],
        #registerForm input[type="number"],
        #registerForm select {
            width: 100%;
            padding: 0.5rem;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        #registerForm button[type="submit"] {
            width: 100%;
            padding: 0.75rem;
            background-color: #ff1493;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            margin-top: 1rem;
        }
        #registerForm button[type="submit"]:hover {
            background-color: #ff69b4;
        }
    </style>
</head>
<body>
    <header>
        <h1>Minha história, Nosso Mundo</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#" id="homeButton">Início</a></li>
            <li><a href="#" id="storiesButton">Histórias</a></li>
            <li><a href="#" id="profileButton">Perfil <span id="navUserName"></span></a></li>
            <li><a href="#" id="chatButton">Chat</a></li>
            <li><a href="#" id="adminPanelButton" style="display: none;">Painel do Administrador</a></li>
            <li><a href="#" id="loginButton">Login</a></li>
        </ul>
    </nav>
    <div id="loginOverlay">
        <button id="closeLoginButton">&times;</button>
        <div id="loginForm">
            <h2>Login</h2>
            <form id="loginFormElement">
                <div class="form-group">
                    <label for="loginName">Nome:</label>
                    <input type="text" id="loginName" required>
                </div>
                <div class="form-group">
                    <label for="loginPassword">Senha:</label>
                    <input type="password" id="loginPassword" required>
                </div>
                <button type="submit">Entrar</button>
            </form>
            <button id="showRegisterFormButton">Não tem uma conta? Cadastre-se</button>
            <div id="registerForm" style="display: none;">
                <h2>Cadastro</h2>
                <form id="registerFormElement">
                    <div class="form-group">
                        <label for="registerName">Nome:</label>
                        <input type="text" id="registerName" required>
                    </div>
                    <div class="form-group">
                        <label for="registerPassword">Senha:</label>
                        <input type="password" id="registerPassword" required>
                    </div>
                    <div class="form-group">
                        <label for="registerAge">Idade:</label>
                        <input type="number" id="registerAge" required>
                    </div>
                    <div class="form-group">
                        <label for="registerGender">Sexo:</label>
                        <select id="registerGender" required>
                            <option value="male">Masculino</option>
                            <option value="female">Feminino</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="registerContact">Contato (WhatsApp):</label>
                        <input type="text" id="registerContact" required>
                    </div>
                    <button type="submit">Cadastrar</button>
                </form>
            </div>
        </div>
    </div>
    <main id="mainContent">
        <div id="welcomeMessage" style="display: none;"></div>
        <div class="content-wrapper">
            <div class="left-column">
                <div id="highlightedNews">
                    <h3>Notícias em Destaque</h3>
                    <div class="news-carousel">
                        <div class="news-slider">
                            <div class="news-item">
                                <img src="https://images.app.goo.gl/qAwmGLmeUFW9eet2A" alt="Nova história adicionada" class="news-image">
                                <h4>Nova história adicionada</h4>
                                <p>"A Princesa e o Sapo" agora disponível para leitura!</p>
                                <a href="#" class="read-more">Leia mais</a>
                            </div>
                            <div class="news-item">
                                <img src="https://picsum.photos/300/200?random=2" alt="Concurso de desenho infantil" class="news-image">
                                <h4>Concurso de desenho infantil</h4>
                                <p>Participe até 30/06 e ganhe prêmios incríveis!</p>
                                <a href="#" class="read-more">Saiba mais</a>
                            </div>
                            <div class="news-item">
                                <img src="https://picsum.photos/300/200?random=3" alt="Evento de contação de histórias" class="news-image">
                                <h4>Evento de contação de histórias</h4>
                                <p>Junte-se a nós no próximo sábado para uma tarde mágica!</p>
                                <a href="#" class="read-more">Detalhes do evento</a>
                            </div>
                        </div>
                    </div>
                    <div class="carousel-controls">
                        <button class="prev-btn">&lt;</button>
                        <button class="next-btn">&gt;</button>
                    </div>
                </div>
            </div>
        </div>
        <div id="userProfile" style="display: none;">
            <h2>Perfil do Usuário</h2>
            <button id="toggleProfileInfo">Mostrar/Ocultar Informações do Perfil</button>
            <ul id="profileInfo"></ul>
            <form id="editProfileForm">
                <h3>Editar Perfil</h3>
                <div class="form-group">
                    <label for="editName">Nome:</label>
                    <input type="text" id="editName" required>
                </div>
                <div class="form-group">
                    <label for="editAge">Idade:</label>
                    <input type="number" id="editAge" required>
                </div>
                <div class="form-group">
                    <label for="editGender">Sexo:</label>
                    <select id="editGender" required>
                        <option value="male">Masculino</option>
                        <option value="female">Feminino</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="editContact">Contato (WhatsApp):</label>
                    <input type="text" id="editContact" required>
                </div>
                <button type="submit">Salvar Alterações</button>
            </form>
            <button id="logoutButton">Sair</button>
        </div>
        <div id="adminPanel" style="display: none;">
            <h2>Painel do Administrador</h2>
            <ul id="userList"></ul>
            <div id="userDetails"></div>
            <div id="adminChatMessages"></div>
            <div id="storyEditor" style="display: none;">
                <h3>Editor de Histórias</h3>
                <textarea id="storyContent" rows="10" cols="50"></textarea>
                <button id="saveStoryButton" class="admin-button">Salvar História</button>
            </div>
        </div>
        <div id="storyContainer" style="display: none;">
        </div>
        <div id="chatSection" style="display: none;">
            <h2>Chat com Administrador</h2>
            <div id="chatMessages"></div>
            <form id="chatForm">
                <input type="text" id="chatTitle" placeholder="Título da mensagem" required>
                <textarea id="chatBody" placeholder="Corpo da mensagem" required></textarea>
                <button type="submit">Enviar Mensagem</button>
            </form>
        </div>
    </main>
    <footer>
        <p>&copy; CWD2024 Minha história, Nosso Mundo. Todos os direitos reservados.</p>
        <div class="social-links">
            <a href="https://facebook.com/minhahistorianossomundo" target="_blank" rel="noopener noreferrer">
                <i class="fab fa-facebook"></i>
            </a>
            <a href="https://wa.me/message/ABCDEFGHIJKLM" target="_blank" rel="noopener noreferrer">
                <i class="fab fa-whatsapp"></i>
            </a>
            <a href="mailto:contato@minhahistorianossomundo.com">
                <i class="fas fa-envelope"></i>
            </a>
        </div>
    </footer>
    <script src="https://kit.fontawesome.com/your-fontawesome-kit.js" crossorigin="anonymous"></script>
    <script>
        const adminUsername = 'CWD';
        const adminPassword = '6363';
        let users = loadUsers() || [];
        let currentUser = null;

        const stories = [
            {
                id: 1,
                title: 'O Patinho Feio',
                content: 'Era uma vez um patinho diferente dos seus irmãos. Ele era maior, mais desajeitado e tinha uma cor acinzentada, enquanto os outros eram amarelos e fofos. Por causa de sua aparência, ele era rejeitado e zombado pelos outros animais do celeiro. Triste e solitário, o patinho feio decidiu partir em busca de um lugar onde pudesse ser aceito. Durante sua jornada, enfrentou muitas dificuldades e o rigoroso inverno. Mas com a chegada da primavera, algo incrível aconteceu: o patinho feio se transformou em um belo cisne branco. Ele descobriu que nunca foi um pato, mas sim um filhote de cisne que nasceu no ninho errado. Agora, admirado por todos pela sua beleza, o cisne aprendeu que a verdadeira beleza vem de dentro e que ser diferente pode ser uma bênção.',
                questions: [
                    {
                        question: 'Qual é a lição principal da história do Patinho Feio?',
                        options: [
                            'A aparência física é o mais importante',
                            'Não devemos julgar os outros pela aparência',
                            'Os patos são melhores que os cisnes',
                            'É importante ser igual aos outros'
                        ],
                        correctAnswer: 1
                    },
                    {
                        question: 'O que o patinho feio se tornou no final da história?',
                        options: [
                            'Um pato bonito',
                            'Um cisne',
                            'Uma galinha',
                            'Continuou sendo um pato feio'
                        ],
                        correctAnswer: 1
                    }
                ]
            },
            {
                id: 2,
                title: 'Chapeuzinho Vermelho',
                content: 'Era uma vez uma menina que usava um capuz vermelho, dado por sua avó. Um dia, sua mãe pediu que ela levasse uma cesta com comida para a avó doente. No caminho pela floresta, Chapeuzinho encontrou o Lobo Mau, que a enganou e chegou primeiro à casa da avó. O lobo engoliu a avó e se disfarçou com suas roupas. Quando Chapeuzinho chegou, estranhou a aparência da "avó", fazendo as famosas perguntas sobre os olhos, ouvidos e dentes grandes. O lobo então revelou-se e tentou comer Chapeuzinho, mas um caçador que passava por perto ouviu o barulho e salvou as duas. O lobo foi expulso da floresta, e Chapeuzinho aprendeu a importância de não falar com estranhos e seguir as orientações de sua mãe.',
                questions: [
                    {
                        question: 'Qual é a lição principal da história de Chapeuzinho Vermelho?',
                        options: [
                            'Falar com estranhos pode ser perigoso',
                            'Devemos sempre seguir os mandamentos dos pais',
                            'Os lobos são sempre amigos',
                            'As avós devem ter cuidado'
                        ],
                        correctAnswer: 0
                    },
                    {
                        question: 'Quem salvou Chapeuzinho Vermelho e sua avó?',
                        options: [
                            'Um príncipe',
                            'Um caçador',
                            'Um viajante',
                            'O Lobo Mau'
                        ],
                        correctAnswer: 1
                    }
                ]
            },
            {
                id: 3,
                title: 'Os Três Porquinhos',
                content: 'Era uma vez três porquinhos irmãos que decidiram construir suas próprias casas. O primeiro, preguiçoso, fez uma casa de palha rapidamente. O segundo, um pouco mais esforçado, construiu uma casa de madeira. Já o terceiro, muito trabalhador, ergueu uma sólida casa de tijolos. Um dia, o Lobo Mau apareceu e soprou com força, derrubando a casa de palha. O primeiro porquinho correu para a casa do segundo. O lobo soprou novamente e destruiu a casa de madeira. Os dois porquinhos fugiram para a casa de tijolos do terceiro irmão. O Lobo Mau soprou e soprou, mas não conseguiu derrubar a casa forte. Frustrado, tentou entrar pela chaminé, mas caiu em um caldeirão de água fervente e fugiu, nunca mais voltando. Os porquinhos aprenderam a importância do trabalho duro e da precaução.',
                questions: [
                    {
                        question: 'Qual é a principal lição da história dos três porquinhos?',
                        options: [
                            'O trabalho duro compensa',
                            'Casas de palha são melhores',
                            'É importante ter amigos',
                            'O Lobo Mau era um bom personagem'
                        ],
                        correctAnswer: 0
                    },
                    {
                        question: 'Qual casa foi destruída primeiro pelo Lobo?',
                        options: [
                            'Casa de tijolos',
                            'Casa de madeira',
                            'Casa de palha',
                            'Nenhuma das anteriores'
                        ],
                        correctAnswer: 2
                    }
                ]
            },
            {
                id: 4,
                title: 'João e o Pé de Feijão',
                content: 'Era uma vez um menino chamado João que vivia com sua mãe viúva. Um dia, ela mandou João vender sua única vaca para comprar comida. No caminho, João trocou a vaca por feijões mágicos. Sua mãe, furiosa, jogou os feijões pela janela. Na manhã seguinte, um enorme pé de feijão havia crescido até o céu. João subiu e encontrou um castelo nas nuvens, habitado por um gigante malvado. João descobriu que o gigante possuía uma galinha que punha ovos de ouro e uma harpa mágica, que pertenceram ao seu pai. Corajosamente, João conseguiu recuperar os tesouros, fugindo do gigante. Ao chegar em casa, cortou o pé de feijão, fazendo o gigante cair. Com a galinha e a harpa, João e sua mãe nunca mais passaram necessidades, vivendo felizes para sempre.',
                questions: [
                    {
                        question: 'Qual era o produto que João recebeu pelos feijões mágicos?',
                        options: [
                            'Uma vaca',
                            'Um ganso',
                            'Um castelo',
                            'Os feijões'
                        ],
                        correctAnswer: 3
                    },
                    {
                        question: 'Qual era o prêmio que João encontrou no castelo?',
                        options: [
                            'Uma harpa mágica',
                            'Um ovo de ouro',
                            'Um gigante',
                            'Uma princesa'
                        ],
                        correctAnswer: 0
                    }
                ]
            },
            {
                id: 5,
                title: 'A Bela Adormecida',
                content: 'Em um reino distante, nasceu uma princesa chamada Aurora. Durante seu batizado, uma fada má lançou uma maldição: ao completar 16 anos, a princesa espetaria o dedo em uma roca e cairia em um sono profundo. Uma fada boa conseguiu amenizar a maldição: o sono duraria até que um beijo de amor verdadeiro a despertasse. O rei ordenou que todas as rocas do reino fossem queimadas. Aurora cresceu sem saber de seu destino. No dia de seu aniversário de 16 anos, enganada pela fada má, ela espetou o dedo e adormeceu. O reino inteiro caiu em um sono mágico. Cem anos se passaram até que um príncipe corajoso chegasse ao castelo. Ele beijou Aurora, quebrando o feitiço. Todos despertaram, e o príncipe e a princesa se casaram, vivendo felizes para sempre.',
                questions: [
                    {
                        question: 'Qual foi a causa do sono profundo da princesa Aurora?',
                        options: [
                            'Um feitiço de uma fada má',
                            'Um encantamento de um príncipe',
                            'Uma maldição de sua mãe',
                            'Uma doença misteriosa'
                        ],
                        correctAnswer: 0
                    },
                    {
                        question: 'Quem a acordou do sono profundo?',
                        options: [
                            'Uma fada boa',
                            'Um príncipe',
                            'Um rei',
                            'Um viajante'
                        ],
                        correctAnswer: 1
                    }
                ]
            }
        ];

        let chatMessages = [];

        const welcomeMessage = document.getElementById('welcomeMessage');
        const userNameDisplay = document.getElementById('userNameDisplay');
        const highlightedNews = document.getElementById('highlightedNews');
        const homeButton = document.getElementById('homeButton');
        const storiesButton = document.getElementById('storiesButton');
        const profileButton = document.getElementById('profileButton');
        const chatButton = document.getElementById('chatButton');
        const loginButton = document.getElementById('loginButton');
        const adminPanelButton = document.getElementById('adminPanelButton');
        const loginForm = document.getElementById('loginForm');
        const showRegisterFormButton = document.getElementById('showRegisterFormButton');
        const registerForm = document.getElementById('registerForm');
        const userProfile = document.getElementById('userProfile');
        const profileInfo = document.getElementById('profileInfo');
        const editProfileForm = document.getElementById('editProfileForm');
        const logoutButton = document.getElementById('logoutButton');
        const adminPanel = document.getElementById('adminPanel');
        const userList = document.getElementById('userList');
        const userDetails = document.getElementById('userDetails');
        const storyEditor = document.getElementById('storyEditor');
        const storyContent = document.getElementById('storyContent');
        const saveStoryButton = document.getElementById('saveStoryButton');
        const storyContainer = document.getElementById('storyContainer');
        const toggleProfileInfoButton = document.getElementById('toggleProfileInfo');
        const chatMessagesElement = document.getElementById('chatMessages');
        const chatForm = document.getElementById('chatForm');
        const chatTitle = document.getElementById('chatTitle');
        const chatBody = document.getElementById('chatBody');
        const adminChatMessagesElement = document.getElementById('adminChatMessages');

        storyContainer.style.display = 'none';

        function loadUsers() {
            try {
                const savedUsers = localStorage.getItem('users');
                return savedUsers ? JSON.parse(savedUsers) : [];
            } catch (e) {
                console.error('Error loading users:', e);
                return [];
            }
        }

        function saveUsers() {
            try {
                localStorage.setItem('users', JSON.stringify(users));
            } catch (e) {
                console.error('Error saving users:', e);
            }
        }

        function updateNavUserName() {
            const navUserName = document.getElementById('navUserName');
            if (navUserName) {
                navUserName.textContent = currentUser ? currentUser.name : '';
            }
        }

        function isLoggedIn() {
            return currentUser !== null;
        }

        function loginUser(user) {
            currentUser = user;
            hideLoginOverlay();
            updateNavUserName();
            updateNavigation();
            showHome();
        }

        function logoutUser() {
            currentUser = null;
            updateNavUserName();
            updateNavigation();
            const loginOverlay = document.getElementById('loginOverlay');
            if (loginOverlay) {
                loginOverlay.style.display = 'flex';
            }
            hideAllSections();
            const contentWrapper = document.querySelector('.content-wrapper');
            if (contentWrapper) {
                contentWrapper.style.display = 'flex';
            }
        }

        function updateNavigation() {
            if (isLoggedIn()) {
                loginButton.style.display = 'none';
                storiesButton.style.pointerEvents = 'auto';
                profileButton.style.pointerEvents = 'auto';
                chatButton.style.pointerEvents = 'auto';

// Show admin panel button only for admin user
                if (adminPanelButton) {
                    adminPanelButton.style.display = currentUser.isAdmin ? 'inline-block' : 'none';
                }
            } else {
                loginButton.style.display = 'inline-block';
                storiesButton.style.pointerEvents = 'none';
                profileButton.style.pointerEvents = 'none';
                chatButton.style.pointerEvents = 'none';

                if (adminPanelButton) {
                    adminPanelButton.style.display = 'none';
                }
            }
        }

        function initializeNewsCarousel() {
            const newsSlider = document.querySelector('.news-slider');
            const prevBtn = document.querySelector('.prev-btn');
            const nextBtn = document.querySelector('.next-btn');
            let currentSlide = 0;
            const slides = document.querySelectorAll('.news-item');
            const totalSlides = slides.length;

            function updateSlider() {
                newsSlider.style.transform = `translateX(-${currentSlide * 100}%)`;
            }

            if (prevBtn) {
                prevBtn.addEventListener('click', () => {
                    currentSlide = (currentSlide - 1 + totalSlides) % totalSlides;
                    updateSlider();
                });
            }

            if (nextBtn) {
                nextBtn.addEventListener('click', () => {
                    currentSlide = (currentSlide + 1) % totalSlides;
                    updateSlider();
                });
            }

            setInterval(() => {
                currentSlide = (currentSlide + 1) % totalSlides;
                updateSlider();
            }, 5000);
        }

        document.addEventListener('DOMContentLoaded', () => {
            const loginOverlay = document.getElementById('loginOverlay') || null;
            const closeLoginButton = document.getElementById('closeLoginButton') || null;
            const loginFormElement = document.getElementById('loginFormElement') || null;
            const registerForm = document.getElementById('registerForm') || null;
            const userProfile = document.getElementById('userProfile') || null;
            const profileInfo = document.getElementById('profileInfo') || null;
            const editProfileForm = document.getElementById('editProfileForm') || null;
            const logoutButton = document.getElementById('logoutButton') || null;
            const adminPanel = document.getElementById('adminPanel') || null;
            const userList = document.getElementById('userList') || null;
            const userDetails = document.getElementById('userDetails') || null;
            const chatSection = document.getElementById('chatSection') || null;
            const chatMessagesElement = document.getElementById('chatMessages') || null;
            const chatForm = document.getElementById('chatForm') || null;

            if (homeButton) {
                homeButton.addEventListener('click', showHome);
            }

            if (storiesButton) {
                storiesButton.addEventListener('click', showStories);
            }

            if (profileButton) {
                profileButton.addEventListener('click', showProfile);
            }

            if (chatButton) {
                chatButton.addEventListener('click', showChatSection);
            }

            if (adminPanelButton) {
                adminPanelButton.addEventListener('click', () => {
                    if (currentUser && currentUser.isAdmin) {
                        showAdminPanel();
                    }
                });
            }

            if (closeLoginButton) {
                closeLoginButton.addEventListener('click', hideLoginOverlay);
            }

            if (showRegisterFormButton && registerForm) {
                showRegisterFormButton.addEventListener('click', () => {
                    const loginFormElement = document.getElementById('loginFormElement');
                    const registerForm = document.getElementById('registerForm');

                    loginFormElement.style.display = 'none';
                    registerForm.style.display = 'block';
                });
            }

            if (editProfileForm) {
                editProfileForm.addEventListener('submit', (e) => {
                    e.preventDefault();
                    if (currentUser) {
                        currentUser.name = document.getElementById('editName').value;
                        currentUser.age = document.getElementById('editAge').value;
                        currentUser.gender = document.getElementById('editGender').value;
                        currentUser.contact = document.getElementById('editContact').value;
                        saveUsers();
                        updateProfileInfo();
                    }
                });
            }

            if (logoutButton) {
                logoutButton.addEventListener('click', () => {
                    logoutUser();
                });
            }

            if (registerForm) {
                document.getElementById('registerFormElement').addEventListener('submit', (e) => {
                    e.preventDefault();

                    const name = document.getElementById('registerName').value;
                    const password = document.getElementById('registerPassword').value;
                    const age = document.getElementById('registerAge').value;
                    const gender = document.getElementById('registerGender').value;
                    const contact = document.getElementById('registerContact').value;

                    if (users.some(user => user.name === name)) {
                        alert('Este nome de usuário já está em uso. Por favor escolha outro.');
                        return;
                    }

                    const newUser = {
                        name,
                        password,
                        age,
                        gender,
                        contact,
                        history: [],
                        storyReadCount: {}
                    };

                    users.push(newUser);
                    saveUsers();
                    loginUser(newUser);
                    document.getElementById('registerFormElement').reset();
                    registerForm.style.display = 'none';
                    loginFormElement.style.display = 'block';
                });
            }

            if (toggleProfileInfoButton) {
                toggleProfileInfoButton.addEventListener('click', () => {
                    const profileInfo = document.getElementById('profileInfo');
                    if (profileInfo) {
                        profileInfo.style.display = profileInfo.style.display === 'none' ? 'block' : 'none';
                    }
                });
            }

            initializeNewsCarousel();
            updateNavigation();
        });

        function hideLoginOverlay() {
            const loginOverlay = document.getElementById('loginOverlay');
            if (loginOverlay) {
                loginOverlay.style.display = 'none';
            }
        }

        function showLoginOverlay() {
            const loginOverlay = document.getElementById('loginOverlay');
            if (loginOverlay) {
                loginOverlay.style.display = 'flex';
            }
        }

        function showHome() {
            hideAllSections();
            welcomeMessage.style.display = 'block';
            const contentWrapper = document.querySelector('.content-wrapper');
            if (contentWrapper) {
                contentWrapper.style.display = 'block';
            }
        }

        function showStories() {
            hideAllSections();
            storyContainer.style.display = 'block';
            loadStories();
        }

        function showProfile() {
            hideAllSections();
            userProfile.style.display = 'block';
            updateProfileInfo();
        }

        function showChatSection() {
            hideAllSections();
            const chatSection = document.getElementById('chatSection');
            if (chatSection) {
                chatSection.style.display = 'block';
                loadChatMessages();
            }
        }

        function hideAllSections() {
            const sections = [
                'welcomeMessage',
                'storyContainer',
                'userProfile',
                'chatSection',
                'adminPanel'
            ];

            sections.forEach(id => {
                const element = document.getElementById(id);
                if (element) {
                    element.style.display = 'none';
                }
            });

            const contentWrapper = document.querySelector('.content-wrapper');
            if (contentWrapper) {
                contentWrapper.style.display = 'none';
            }
        }

        function showWelcomeMessage() {
            welcomeMessage.innerHTML = `
                <h2>Bem-vindo, ${currentUser.name}!</h2>
                <p>Bem-vindo ao Minha história, Nosso Mundo, o lugar perfeito para explorar histórias encantadoras e divertidas. Aqui você encontrará uma coleção de contos clássicos e modernos para entreter e educar crianças de todas as idades.</p>
            `;
            welcomeMessage.style.display = 'block';
        }

        loginFormElement.addEventListener('submit', (e) => {
            e.preventDefault();
            const name = document.getElementById('loginName').value;
            const password = document.getElementById('loginPassword').value;

            if (name === adminUsername && password === adminPassword) {
                loginAsAdmin();
            } else {
                const user = users.find(u => u.name === name && u.password === password);
                if (user) {
                    loginUser(user);
                } else {
                    alert('Nome de usuário ou senha incorretos.');
                }
            }
        });

        function loginAsAdmin() {
            currentUser = { name: 'Admin', isAdmin: true };
            hideAllSections();
            hideLoginOverlay();
            showAdminPanel();
            updateNavUserName();
            updateNavigation();
        }

        function showAdminPanel() {
            userProfile.style.display = 'none';
            adminPanel.style.display = 'block';
            storyContainer.style.display = 'none';
            loadUserList();
            loadChatMessages();
        }

        function loadStories() {
            storyContainer.innerHTML = stories.map(story => `
                <div class="story">
                    <h2>${story.title}</h2>
                    <p>${story.content.substring(0, 200)}...</p>
                    <button onclick="readFullStory(${story.id})">Ler História Completa</button>
                    ${currentUser ? `<button onclick="readStory(${story.id})">Marcar como Lida</button>` : ''}
                </div>
            `).join('');

            if (!document.getElementById('storyModal')) {
                const modal = document.createElement('div');
                modal.id = 'storyModal';
                modal.innerHTML = `
                    <div class="modal-content">
                        <span class="close">&times;</span>
                        <h2 id="modalTitle"></h2>
                        <div id="modalContent"></div>
                    </div>
                `;
                document.body.appendChild(modal);

                modal.querySelector('.close').addEventListener('click', () => {
                    modal.style.display = 'none';
                });
            }
        }

        function readFullStory(storyId) {
            const story = stories.find(s => s.id === storyId);
            if (story) {
                const modal = document.getElementById('storyModal');
                const modalTitle = document.getElementById('modalTitle');
                const modalContent = document.getElementById('modalContent');

                modalTitle.textContent = story.title;

                const paragraphs = story.content.split('\n\n');
                modalContent.innerHTML = paragraphs.map(paragraph => `<p>${paragraph}</p>`).join('');

                // Add questions after story content
                if (story.questions) {
                    modalContent.innerHTML += `
                        <div class="interpretation-questions">
                            <h3>Perguntas sobre a história:</h3>
                            ${story.questions.map((q, index) => `
                                <div class="question">
                                    <p>${q.question}</p>
                                    <div class="options">
                                        ${q.options.map((option, optionIndex) => `
                                            <label>
                                                <input type="radio" name="question${index}" value="${optionIndex}">
                                                ${option}
                                            </label>
                                        `).join('')}
                                    </div>
                                </div>
                            `).join('')}
                            <button onclick="submitAnswers(${storyId})" class="read-button">Enviar Respostas</button>
                        </div>
                    `;
                }

                modal.style.display = 'block';
            }
        }

        function submitAnswers(storyId) {
            const story = stories.find(s => s.id === storyId);
            if (!story || !story.questions) return;

            const answers = story.questions.map((_, index) => {
                const selected = document.querySelector(`input[name="question${index}"]:checked`);
                return selected ? parseInt(selected.value) : -1;
            });

            // Check if all questions are answered
            if (answers.includes(-1)) {
                alert('Por favor, responda todas as perguntas.');
                return;
            }

            // Save answers to user profile
            if (currentUser) {
                if (!currentUser.answers) {
                    currentUser.answers = {};
                }
                currentUser.answers[storyId] = answers;
                saveUsers();
            }

            // Show results
            let correctCount = answers.reduce((count, answer, index) => {
                return count + (answer === story.questions[index].correctAnswer ? 1 : 0);
            }, 0);

            alert(`Você acertou ${correctCount} de ${story.questions.length} perguntas!`);

            // Update profile if visible
            if (userProfile.style.display === 'block') {
                updateProfileInfo();
            }

            // Close modal after submission
            document.getElementById('storyModal').style.display = 'none';
        }

        function loadUserList() {
            userList.innerHTML = users.map(user => user ? `
                <li>
                    ${user.name}
                    <button onclick="showUserDetails('${user.name}')">Detalhes</button>
                    <button onclick="deleteUser('${user.name}')">Excluir</button>
                </li>
            ` : '').join('');
        }

        function showUserDetails(username) {
            const user = users.find(u => u.name === username);
            if (user) {
                let userDetailsHtml = `
                    <h3>Detalhes do Usuário</h3>
                    <p><strong>Nome:</strong> ${user.name}</p>
                    <p><strong>Idade:</strong> ${user.age}</p>
                    <p><strong>Sexo:</strong> ${user.gender === 'male' ? 'Masculino' : 'Feminino'}</p>
                    <p><strong>Contaato:</strong> ${user.contact}</p>
                    <h4>Histórico de Atividade</h4>
                    <ul>
                        ${user.history ? user.history.map(activity => `<li>${activity}</li>`).join('') : 'Nenhuma atividade registrada'}
                    </ul>
                    <h4>Contagem de Leituras</h4>
                    <ul>
                        ${user.storyReadCount ? Object.entries(user.storyReadCount).map(([story, count]) => `
                            <li>${story}: ${count} vezes</li>
                        `).join('') : 'Nenhuma leitura registrada'}
                    </ul>
                `;

                // Add quiz results to user details
                if (user.answers) {
                    userDetailsHtml += '<h4>Resultados dos Quizzes:</h4>';
                    Object.entries(user.answers).forEach(([storyId, answers]) => {
                        const story = stories.find(s => s.id === parseInt(storyId));
                        if (story) {
                            userDetailsHtml += `<h5>${story.title}</h5>`;
                            story.questions.forEach((q, index) => {
                                const userAnswer = answers[index];
                                const isCorrect = userAnswer === q.correctAnswer;
                                userDetailsHtml += `
                                    <p>
                                        Pergunta ${index + 1}: ${isCorrect ? '✓ Correta' : '✗ Incorreta'}
                                        ${isCorrect ? '' : ` (Resposta correta: ${q.options[q.correctAnswer]})`}
                                    </p>
                                `;
                            });
                        }
                    });
                }

                userDetailsHtml += `<button onclick="adminSendChatMessage('${user.name}')">Responder no Chat</button>`;
                userDetails.innerHTML = userDetailsHtml;
            } else {
                userDetails.innerHTML = '<p>Usuário não encontrado.</p>';
            }
        }

        function deleteUser(username) {
            if (confirm(`Tem certeza que deseja excluir o usuário ${username}?`)) {
                users = users.filter(u => u.name !== username);
                saveUsers();
                loadUserList();
                userDetails.innerHTML = '';
            }
        }

        function adminSendChatMessage(userName) {
            const adminTitle = prompt('Enter message title:');
            const adminBody = prompt('Enter message body:');

            if (adminTitle && adminBody) {
                chatMessages.push({
                    sender: 'admin',
                    userName: 'Admin',
                    title: adminTitle,
                    body: adminBody
                });

                loadChatMessages();
            }
        }

        chatForm.addEventListener('submit', (event) => {
            event.preventDefault();
            const title = chatTitle.value;
            const body = chatBody.value;

            chatMessages.push({
                sender: 'user',
                userName: currentUser.name,
                title: title,
                body: body
            });

            chatTitle.value = '';
            chatBody.value = '';

            loadChatMessages();
        });

        function loadChatMessages() {
            const messageHTML = chatMessages.map(message => `
                <div class="chatMessage ${message.sender === 'user' ? 'userMessage' : 'adminMessage'}">
                    <strong>${message.sender === 'user' ? message.userName : 'Admin'}</strong>
                    <h4>${message.title}</h4>
                    <p>${message.body}</p>
                </div>
            `).join('');

            chatMessagesElement.innerHTML = messageHTML;

            if (adminChatMessagesElement) {
                adminChatMessagesElement.innerHTML = messageHTML;
            }
        }

        function updateProfileInfo() {
            const profileInfo = document.getElementById('profileInfo');
            if (!profileInfo || !currentUser) return;

            let profileHtml = `
                <li><strong>Nome:</strong> ${currentUser.name}</li>
                <li><strong>Idade:</strong> ${currentUser.age}</li>
                <li><strong>Sexo:</strong> ${currentUser.gender === 'male' ? 'Masculino' : 'Feminino'}</li>
                <li><strong>Contato:</strong> ${currentUser.contact}</li>
            `;

            // Add quiz results section
            if (currentUser.answers) {
                profileHtml += '<h3>Resultados dos Quizzes:</h3>';
                Object.entries(currentUser.answers).forEach(([storyId, answers]) => {
                    const story = stories.find(s => s.id === parseInt(storyId));
                    if (story) {
                        profileHtml += `<h4>${story.title}</h4>`;
                        story.questions.forEach((q, index) => {
                            const userAnswer = answers[index];
                            const isCorrect = userAnswer === q.correctAnswer;
                            profileHtml += `
                                <p>
                                    Pergunta ${index + 1}: ${isCorrect ? '✓ Correta' : '✗ Incorreta'}
                                    ${isCorrect ? '' : ` (Resposta correta: ${q.options[q.correctAnswer]})`}
                                </p>
                            `;
                        });
                    }
                });
            }

            profileInfo.innerHTML = profileHtml;
            document.body.style.backgroundColor = currentUser.gender === 'male' ? '#e6f2ff' : '#fff0f5';
        }

        function showLoginForm() {
            hideAllSections();
            const loginOverlay = document.getElementById('loginOverlay');
            const registerForm = document.getElementById('registerForm');
            const contentWrapper = document.querySelector('.content-wrapper');
            const highlightedNews = document.getElementById('highlightedNews');

            if (loginOverlay) {
                loginOverlay.style.display = 'flex';
            }

            const loginFormElement = document.getElementById('loginFormElement');
            if (loginFormElement) {
                loginFormElement.style.display = 'block';
            }

            if (registerForm) {
                registerForm.style.display = 'none';
            }

            if (contentWrapper) {
                contentWrapper.style.display = 'flex';
            }

            if (highlightedNews) {
                highlightedNews.style.display = 'block';
            }

            updateNavigation();
        }

    </script>
</body>
</html>
