# Introdução
[![NPM](https://img.shields.io/npm/l/react)]([https://github.com/devsuperior/sds1-wmazoni/blob/master/LICENSE](https://github.com/joaogabriel365/Rota-Facil-JD/blob/main/LICENSE)) 

## Objetivos Príncipais e Específicos

Objetivo geral:
O projeto Rota Fácil JD tem como objetivo otimizar a comunicação e a gestão do tráfego nas instalações industriais da John Deere. Após uma análise detalhada das necessidades e desafios da empresa, identificou-se a importância de desenvolver uma aplicação web dedicada para esse fim, visando melhorar a produtividade e a organização no fluxo de trabalho. Os principais usuários serão os motoristas de rebocadores e a linha de produção, que solicitarão carrinhos de transporte.

A aplicação será desenvolvida em HTML e JavaScript, utilizando o editor Sublime. A troca de dados entre dispositivos IoT e servidores web será realizada por meio do protocolo MQTT, enquanto o módulo Wi-Fi do ESP32 se conectará a múltiplos roteadores para obter geolocalização via triangulação. O microcontrolador ESP32 será responsável pela coleta dos dados de localização.

Optou-se pelo desenvolvimento em HTML e JavaScript devido à sua facilidade de uso, flexibilidade, ser gratuito e de código aberto. Já o ESP32, com conexão Wi-Fi, apresenta uma solução de geolocalização com excelente custo-benefício e alcance de sinal, sendo uma alternativa competitiva em relação a outras opções disponíveis no mercado.

Objetivo específico e metas:
Buscando alcançar os pontos esclarecidos até aqui, segue metas que o projeto Rota Fácil JD visa alcançar com a implementação do sistema:

1- Gestão otimizada de tráfego: Coordenar o tráfego de carrinhos e rebocadores para melhorar a eficiência.

2- Aumento da produtividade: Permitir que os motoristas tomem rotas e decisões mais eficientes e evitar que carrinhos fiquem ociosos.

3- Maximizar a eficiência da comunicação: Integrar pedidos, da linha de produção, ao software para prevenir falhas e aperfeiçoar a comunicação.Materiais de Metodologia a Utilizar

## Dor do projeto


A principal dor do projeto "Rota Fácil JD" está relacionada à ineficiência na comunicação e gestão do tráfego interno nas instalações industriais da John Deere. Atualmente, os motoristas de rebocadores e a linha de produção enfrentam dificuldades em coordenar as solicitações de transporte de materiais, o que resulta em desorganização, atrasos e, consequentemente, perda de produtividade.

A ausência de um sistema integrado e automatizado torna a comunicação entre os motoristas e as equipes de produção lenta e suscetível a erros, o que afeta o fluxo operacional. Além disso, a falta de uma solução adequada para rastrear a localização dos rebocadores dentro da planta agrava ainda mais o problema, uma vez que dificulta a otimização das rotas e a alocação eficiente dos recursos de transporte.

O projeto "Rota Fácil JD" busca solucionar essa dor criando uma plataforma dedicada que permitirá uma melhor gestão do tráfego e da comunicação entre os envolvidos, garantindo mais eficiência, organização e produtividade nas operações internas da empresa.



#### Segue modelo de layout da fábrica:

![image](https://github.com/user-attachments/assets/ec91b8e0-685e-4ed3-aa3a-9cd6bbe87ea7)

# Desenvolvimento:

[https://github.com/user-attachments/assets/770adffe-7655-420d-8670-bfd220f3f076](https://github.com/user-attachments/assets/d2f5d585-6a0e-4b64-a517-592f3ca6db43
)
# Resultados:
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rota Fácil JD</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400&display=swap');

        body {
            font-family: 'Montserrat', sans-serif;
            margin: 0;
            padding: 0;
            font-size: 16px;
        }

        header {
            background-color: white;
            border-bottom: 8px solid #E9D711; /* Borda amarela para separar o menu da home */
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 20px;
        }

        .logo-title-container {
            display: flex;
            align-items: center;
        }

        .logo-title-container img {
            height: 120px; /* Tamanho da imagem no menu */
            margin-right: 0px; /* Espaço entre a imagem e o título */
            margin-left: 220px; /* Mover a imagem ligeiramente para a direita */
        }

        .logo-title-container h1 {
            font-size: 24px; /* Tamanho do título "Rota Fácil JD" */
            margin: 0;
            color: #397b29; /* Mudança de cor do título para verde */
            margin-left: 0px; /* Movendo o título um pouco para a direita */
        }

        /* Estilo do seletor de idioma */
        .language-selector {
            position: relative;
            display: inline-block;
            margin-right: 100px; /* Mover o seletor de idiomas um pouco para a esquerda */
        }

        .language-btn {
            background-color: white;
            border: 2px solid #E9D711;
            padding: 5px 10px;
            cursor: pointer;
            display: flex;
            align-items: center;
            font-size: 16px;
        }

        .language-btn img {
            height: 20px;
            margin-right: 8px;
        }

        .language-dropdown {
            display: none;
            position: absolute;
            background-color: white;
            border: 2px solid #E9D711;
            z-index: 1;
            list-style-type: none;
            padding: 0;
            margin: 0;
            width: 150px;
        }

        .language-dropdown li {
            padding: 10px;
            cursor: pointer;
            display: flex;
            align-items: center;
        }

        .language-dropdown li img {
            height: 20px;
            margin-right: 8px;
        }

        .language-dropdown li:hover {
            background-color: #f1f1f1;
        }

        .language-selector:hover .language-dropdown {
            display: block;
        }

        .map-container {
            text-align: center;
            padding: 20px;
        }

        .map {
            width: 60%; /* Diminuir o tamanho do mapa central */
            border: 10px solid #000;
            margin: 0 auto;
            margin-left: 5px; /* Mover a imagem do mapa ligeiramente para a direita */
        }

        .footer {
            background-color: #E9D711;
            padding: 20px;
            display: flex;
            justify-content: center; /* Centraliza os elementos do rodapé */
            align-items: center; /* Alinha verticalmente */
            gap: 800px; /* Espaçamento entre os dois lados do rodapé */
        }

        .footer-left {
            display: flex;
            flex-direction: column;
            align-items: center; /* Centraliza o conteúdo do lado esquerdo */
            margin-left: 20px; /* Para aproximar mais ao centro, ajuste a margem conforme necessário */
        }

        .footer-left img {
            height: 140px; /* Tamanho da imagem no rodapé */
        }

        .footer-left p, .footer-left a {
            font-size: 16px; /* Definir o tamanho da fonte para 16px */
            font-style: italic; /* Deixar o texto em itálico */
            font-weight: bold; /* Negrito no texto */
            color: green; /* Deixar o texto verde */
            margin: 5px 0;
        }

        .footer-right {
            text-align: center; /* Centraliza o texto à direita */
            font-style: italic;
            color: green;
            font-weight: bold; /* Negrito no texto */
        }

        .footer-right p {
            margin: 5px 0;
        }

        .footer a {
            color: green; /* Deixar os links verdes */
            text-decoration: none;
            font-style: italic;
            font-weight: bold; /* Negrito nos links */
        }
    </style>
</head>
<body>

    <header>
        <div class="logo-title-container">
            <img src="https://cdn.discordapp.com/attachments/740174834927140925/1273053043151343657/2000-JD-removebg-preview.png?ex=66e56c49&is=66e41ac9&hm=480c49bbfb1a3648674405138927b598b11bbf75432af0d6a98939d56cb5aff7&" alt="John Deere Logo">
            <h1 id="title">Rota Fácil JD</h1>
        </div>
        <div class="language-selector">
            <button class="language-btn">
                <img id="current-flag" src="https://cdn.countryflags.com/thumbs/brazil/flag-400.png" alt="Portuguese">
                <span id="current-lang">PT</span>
                <span>▼</span>
            </button>
            <ul class="language-dropdown">
                <li onclick="changeLanguage('pt')"><img src="https://cdn.countryflags.com/thumbs/brazil/flag-400.png" alt="Portuguese"> Portuguese</li>
                <li onclick="changeLanguage('en')"><img src="https://cdn.countryflags.com/thumbs/united-states-of-america/flag-400.png" alt="English"> English</li>
                <li onclick="changeLanguage('fr')"><img src="https://cdn.countryflags.com/thumbs/france/flag-400.png" alt="French"> French</li>
                <li onclick="changeLanguage('de')"><img src="https://cdn.countryflags.com/thumbs/germany/flag-400.png" alt="German"> German</li>
                <li onclick="changeLanguage('es')"><img src="https://cdn.countryflags.com/thumbs/spain/flag-400.png" alt="Spanish"> Spanish</li>
            </ul>
        </div>
    </header>

    <div class="map-container">
        <img class="map" src="https://cdn.discordapp.com/attachments/1234630369744261204/1284288177598763078/image.png?ex=66e61612&is=66e4c492&hm=ee3b7113a331381c5426cc9aeb89b385362b2a5cbb7ab405da72ace33b8923ab&" alt="Rota Fácil JD Map">
    </div>

    <div class="footer">
        <div class="footer-left">
            <img src="https://cdn.discordapp.com/attachments/740174834927140925/1273053043151343657/2000-JD-removebg-preview.png?ex=66e56c49&is=66e41ac9&hm=480c49bbfb1a3648674405138927b598b11bbf75432af0d6a98939d56cb5aff7&" alt="John Deere Logo">
            <p id="footer-text">© 2024 John Deere. Uso interno somente.</p>
            <p><a id="privacy" href="#">Política de Privacidade</a> | <a id="terms" href="#">Termos de Uso</a></p>
        </div>
        <div class="footer-right">
            <br>
            <br>
            <img src="https://cdn.discordapp.com/attachments/740174834927140925/1284296226724122674/image.png?ex=66e61d91&is=66e4cc11&hm=12432fbc7b3a36487feb8c76956b21073cd581b2958eb6f94ad74f5ae0b50bd8&" alt="GOAT">
            <br>
            <br>
            <br>
            <p id="project">Projeto Rota Fácil JD</p>
            <p id="developed">Desenvolvido por: Team GOAT</p>
        </div>
    </div>

    <script>
        const translations = {
            pt: {
                title: "Rota Fácil JD",
                footerText: "© 2024 John Deere. Uso interno somente.",
                privacy: "Política de Privacidade",
                terms: "Termos de Uso",
                project: "Projeto Rota Fácil JD",
                developed: "Desenvolvido por: Team GOAT"
            },
            en: {
                title: "Easy Route JD",
                footerText: "© 2024 John Deere. Internal use only.",
                privacy: "Privacy Policy",
                terms: "Terms of Use",
                project: "Easy Route JD Project",
                developed: "Developed by: Team GOAT"
            },
            fr: {
                title: "Route Facile JD",
                footerText: "© 2024 John Deere. Utilisation interne uniquement.",
                privacy: "Politique de Confidentialité",
                terms: "Conditions d'Utilisation",
                project: "Projet Route Facile JD",
                developed: "Développé par: Team GOAT"
            },
            de: {
                title: "Einfache Route JD",
                footerText: "© 2024 John Deere. Nur für internen Gebrauch.",
                privacy: "Datenschutzrichtlinie",
                terms: "Nutzungsbedingungen",
                project: "Einfaches Route JD Projekt",
                developed: "Entwickelt von: Team GOAT"
            },
            es: {
                title: "Ruta Fácil JD",
                footerText: "© 2024 John Deere. Solo para uso interno.",
                privacy: "Política de Privacidad",
                terms: "Términos de Uso",
                project: "Proyecto Ruta Fácil JD",
                developed: "Desarrollado por: Team GOAT"
            }
        };

        function changeLanguage(lang) {
            document.getElementById('title').innerText = translations[lang].title;
            document.getElementById('footer-text').innerText = translations[lang].footerText;
            document.getElementById('privacy').innerText = translations[lang].privacy;
            document.getElementById('terms').innerText = translations[lang].terms;
            document.getElementById('project').innerText = translations[lang].project;
            document.getElementById('developed').innerText = translations[lang].developed;

            const langBtn = document.getElementById('current-lang');
            const flagImg = document.getElementById('current-flag');

            const flags = {
                pt: "https://cdn.countryflags.com/thumbs/brazil/flag-400.png",
                en: "https://cdn.countryflags.com/thumbs/united-states-of-america/flag-400.png",
                fr: "https://cdn.countryflags.com/thumbs/france/flag-400.png",
                de: "https://cdn.countryflags.com/thumbs/germany/flag-400.png",
                es: "https://cdn.countryflags.com/thumbs/spain/flag-400.png"
            };

            flagImg.src = flags[lang];
            langBtn.innerText = lang.toUpperCase();
        }
    </script>

</body>
</html>






