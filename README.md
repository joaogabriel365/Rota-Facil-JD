# Introdução
[![NPM](https://img.shields.io/npm/l/react)]([https://github.com/devsuperior/sds1-wmazoni/blob/master/LICENSE](https://github.com/joaogabriel365/Rota-Facil-JD/blob/main/LICENSE)) 

# Objetivos Príncipais e Específicos

Objetivo geral:
O projeto Rota Fácil JD tem como objetivo aprimorar a comunicação e a gestão de tráfego nas instalações industriais da John Deere. Após uma análise cuidadosa das necessidades e desafios da empresa, identificamos a necessidade de desenvolver um site dedicado para esse fim, visando aumentar a produtividade e a organização nas instalações. Nossos principais usuários serão os motoristas dos rebocadores, juntamente com a linha de produção nas solicitações de carrinhos.
O desenvolvimento da aplicação web será através da plataforma de criação de sites wordpress. Através do protocolo MQTT será realizada a transferência de dados entre dispositivos IoT e servidores web. Entre os IoT’s será utilizado uma célula de carga para verificar se o carrinho está cheio ou vazio e o módulo wifi do ESP32 se conectará a vários roteadores, desse modo obtendo a geolocalização por meio de triangulação. O microcontrolador ESP 32 será usado para coletar dados de geolocalização e peso, aliado a célula de carga. 
A escolha do WordPress se dá pela sua facilidade de uso, flexibilidade, suporte da comunidade, por ser gratuito e de código aberto. Enquanto isso, o ESP32, com conexão a roteadores e sinal Wi-Fi, oferece uma solução de geolocalização com excelente custo-benefício e alcance de sinal suficiente, isso comparado a outras alternativas disponíveis.
Objetivo específico e metas:
Buscando alcançar os pontos esclarecidos até aqui, segue metas que o projeto Rota Fácil JD visa alcançar com a implementação do sistema:


Gestão otimizada de tráfego: Coordenar o tráfego de carrinhos e rebocadores para melhorar a eficiência.
Aumento da produtividade: Permitir que os motoristas tomem rotas e decisões mais eficientes e evitar que carrinhos fiquem ociosos.
Maximizar a eficiência da comunicação: Integrar pedidos, da linha de produção, ao software para prevenir falhas e aperfeiçoar a comunicação.Materiais de Metodologia a Utilizar


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

