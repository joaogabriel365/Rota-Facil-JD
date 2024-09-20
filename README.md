# Introdução
[![NPM](https://img.shields.io/npm/l/react)]([https://github.com/devsuperior/sds1-wmazoni/blob/master/LICENSE](https://github.com/joaogabriel365/Rota-Facil-JD/blob/main/LICENSE)) 

# Objetivos Príncipais e Específicos

Objetivo geral:
O projeto Rota Fácil JD tem como objetivo otimizar a comunicação e a gestão do tráfego nas instalações industriais da John Deere. Após uma análise detalhada das necessidades e desafios da empresa, identificou-se a importância de desenvolver uma aplicação web dedicada para esse fim, visando melhorar a produtividade e a organização no fluxo de trabalho. Os principais usuários serão os motoristas de rebocadores e a linha de produção, que solicitarão carrinhos de transporte.

A aplicação será desenvolvida em HTML e JavaScript, utilizando o editor Sublime. A troca de dados entre dispositivos IoT e servidores web será realizada por meio do protocolo MQTT, enquanto o módulo Wi-Fi do ESP32 se conectará a múltiplos roteadores para obter geolocalização via triangulação. O microcontrolador ESP32 será responsável pela coleta dos dados de localização.

Optou-se pelo desenvolvimento em HTML e JavaScript devido à sua facilidade de uso, flexibilidade, ser gratuito e de código aberto. Já o ESP32, com conexão Wi-Fi, apresenta uma solução de geolocalização com excelente custo-benefício e alcance de sinal, sendo uma alternativa competitiva em relação a outras opções disponíveis no mercado.

Objetivo específico e metas:
Buscando alcançar os pontos esclarecidos até aqui, segue metas que o projeto Rota Fácil JD visa alcançar com a implementação do sistema:

1- Gestão otimizada de tráfego: Coordenar o tráfego de carrinhos e rebocadores para melhorar a eficiência.
2- Aumento da produtividade: Permitir que os motoristas tomem rotas e decisões mais eficientes e evitar que carrinhos fiquem ociosos.
3- Maximizar a eficiência da comunicação: Integrar pedidos, da linha de produção, ao software para prevenir falhas e aperfeiçoar a comunicação.Materiais de Metodologia a Utilizar


## Layout mobile
![Mobile 1](https://github.com/acenelio/assets/raw/main/sds1/mobile1.png) ![Mobile 2](https://github.com/acenelio/assets/raw/main/sds1/mobile2.png)

## Layout web
![Web 1](https://github.com/acenelio/assets/raw/main/sds1/web1.png)

![Web 2](https://github.com/acenelio/assets/raw/main/sds1/web2.png)

## Modelo conceitual
![Modelo Conceitual](https://github.com/acenelio/assets/raw/main/sds1/modelo-conceitual.png)

# Tecnologias utilizadas
## Back end
- Java
- Spring Boot
- JPA / Hibernate
- Maven
## Front end
- HTML / CSS / JS / TypeScript
- ReactJS
- React Native
- Apex Charts
- Expo
## Implantação em produção
- Back end: Heroku
- Front end web: Netlify
- Banco de dados: Postgresql

# Como executar o projeto

## Back end
Pré-requisitos: Java 11

```bash
# clonar repositório
git clone https://github.com/devsuperior/sds1-wmazoni

# entrar na pasta do projeto back end
cd backend

# executar o projeto
./mvnw spring-boot:run
```

## Front end web
Pré-requisitos: npm / yarn

```bash
# clonar repositório
git clone https://github.com/devsuperior/sds1-wmazoni

# entrar na pasta do projeto front end web
cd front-web

# instalar dependências
yarn install

# executar o projeto
yarn start
```

# Autor

Wellington Mazoni de Andrade

https://www.linkedin.com/in/wmazoni

