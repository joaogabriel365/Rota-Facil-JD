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
#### arquitetura do projeto:

![image](https://github.com/user-attachments/assets/1d3de007-44ad-4766-8000-a21e2defe62a)

   O desenvolvimento começa com a configuração do ESP-32, um microcontrolador com conectividade Wi-Fi. Os sensores Wi-Fi capturam o RSSI de pelo menos três roteadores, permitindo estimar a distância em metros. Com essas distâncias, o sistema calcula a localização dos objetos por meio da triangulação, transformando os dados em coordenadas de latitude e longitude.
Essas coordenadas são enviadas a um broker via protocolo MQTT, que é eficiente para aplicações de Internet das Coisas (IoT). Esse broker recebe as informações, para que os dados seja armazenados e processados no NodeRed. O fluxo implementado nesse software permite que esses dados sejam processados para uma API. O site do projeto utiliza essa API para coletar as informações e exibi-las em um mapa interativo, permitindo que os usuários vejam a localização dos carrinhos e rebocadores em tempo real.
 
# Resultados:
### O que nossa aplicação está devolvendo

Nosso grupo desenvolveu o ROTA FÁCIL JD, um sistema personalizado que visa otimizar a produtividade e a logística interna dentro das instalações da John Deere.

Esse sistema de gestão de tráfego integrará a coleta de dados em tempo real, como localização, a uma interface web intuitiva. Com isso, será possível gerenciar de forma eficiente os carrinhos e rebocadores nas instalações da John Deere, aumentando a produtividade e melhorando a organização logística. Os principais beneficiários dessa solução são os motoristas dos rebocadores e os agentes da linha de produção.

Segue abaixo um video demonstrativo do site desenvolvido:


[https://github.com/user-attachments/assets/770adffe-7655-420d-8670-bfd220f3f076](https://github.com/user-attachments/assets/d2f5d585-6a0e-4b64-a517-592f3ca6db43
)





