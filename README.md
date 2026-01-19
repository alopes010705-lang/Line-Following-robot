
# Line-Following-robot
Este projeto consiste no desenvolvimento de um perseguidor de linha profissional e competitivo, utilizando motores brushless com controle FOC, sensores infravermelhos, encoders e giroscópio. O sistema é baseado em ESP32, com capacidade de mapear a pista e otimizar o desempenho em curvas e retas.

# Perseguidor de Linha Brushless com Controle Avançado

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![License](https://img.shields.io/badge/license-a%20definir-lightgrey)
![Platform](https://img.shields.io/badge/platform-ESP32-blue)
![Motors](https://img.shields.io/badge/motor-brushless%201404-red)
![Control](https://img.shields.io/badge/controle-FOC-green)

---

## Descrição Geral

Este repositório apresenta o desenvolvimento de um perseguidor de linha profissional e competitivo, projetado com foco em alto desempenho, precisão e capacidade de análise da pista. O projeto utiliza motores brushless controlados por técnicas avançadas de controle vetorial (*Field-Oriented Control* – FOC), aliados a um conjunto robusto de sensores e a um sistema de processamento embarcado.

O sistema foi concebido tanto para aplicações em competições quanto para fins acadêmicos, servindo como plataforma de estudo nas áreas de controle, eletrônica embarcada, processamento de sinais e robótica móvel.

---

## Objetivo do Projeto

O objetivo principal deste projeto é desenvolver um robô perseguidor de linha de alto desempenho, capaz de:

- Seguir trajetórias com elevada precisão  
- Operar em altas velocidades com estabilidade dinâmica  
- Mapear a pista percorrida, representando-a como sequência de curvas e retas e também em coordenadas cartesianas (XY)

---

## Arquitetura de Hardware

A eletrônica do robô foi desenvolvida de forma totalmente customizada, integrando todos os subsistemas em uma única placa de circuito impresso (PCB). O projeto prioriza robustez elétrica, redução de ruído e confiabilidade em aplicações de alta corrente e alta velocidade.

O sistema é alimentado por uma bateria Li-Po 3S (11,1 V), com estágios dedicados de proteção, filtragem e regulação para cada subsistema. A alimentação dos motores é isolada da alimentação lógica, minimizando interferências eletromagnéticas no processamento e na leitura dos sensores.

Os motores utilizados são brushless modelo **1404**, acionados por dois drivers **DRV8316**, sendo cada driver responsável por um motor. O controle é realizado por meio da técnica de *Field-Oriented Control* (FOC).

---

## Sensores de Linha – Esquemático

Conjunto de 15 sensores infravermelhos QRE-1113 com condicionamento de sinal e leitura via ADCs externos.

![Sensores IR – Esquemático](docs/images/sensores_ir_esquematico.png)

---

## Sensores de Linha – PCB

Layout da placa dedicada aos sensores infravermelhos, projetada para garantir alinhamento, simetria e redução de ruído.

![Sensores IR – PCB](docs/images/sensores_ircurvas.png)

---

## PCB Principal – Esquemático

Esquemático completo da placa principal, integrando microcontrolador, drivers de motor, sensores, memória e interfaces de comunicação.

![PCB Principal – Esquemático](docs/images/pcb_principal_esquematico.png)

---

## PCB Principal – Layout

Layout final da PCB principal, com separação entre áreas de potência e sinal, planos de terra e roteamento otimizado.

![PCB Principal – Layout](docs/images/pcb_principal_top.png)

---

## Arquitetura de Software

O software embarcado é desenvolvido de forma modular, visando escalabilidade, organização e facilidade de manutenção. Os principais módulos incluem:

- Leitura e filtragem dos sensores infravermelhos  
- Controle de velocidade e torque dos motores via FOC  
- Estimativa de pose utilizando encoders e giroscópio  
- Algoritmos de mapeamento da pista  
- Armazenamento de dados em memória não volátil  

---
---

## Status do Projeto

O projeto encontra-se em desenvolvimento ativo. O hardware está definido e validado em nível de projeto, enquanto o firmware encontra-se em implementação incremental.

---

## Trabalhos Futuros

- Implementação completa do sistema de mapeamento XY  
- Otimização dos algoritmos de controle  
- Integração e validação do sistema de sucção  
- Testes experimentais em pista de competição  

---

## Licença

Este projeto é de acesso público e destinado a fins educacionais e de pesquisa.  
A licença será definida futuramente.
