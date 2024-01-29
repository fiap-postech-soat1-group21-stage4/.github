# FIAP SOAT1 Group 21 - Stage 4
## Sobre
Este repositório contém o código-fonte e os recursos relacionados à implementação da Fase 4 do curso de Software Archicture 1.

O projeto é focado na construção de uma aplicação utilizando arquitetura de microsserviços, qualidade de software e CI/CD automatizada.

## Sumário Executivo
- [x] Projeto Monolito reestruturado em micro serviço;
- [x] Testes Unitários e BBD;
- [x] Workflow CI/CD
  - [x] Pull Requests com execução dos testes e qualidade; 
  - [x] CI executa Testes e SonarQube
      - Em caso de falha nos testes ou recusa do QualityGate do Sonar, a pipeline irá falhar 
        - [Resultados SonarQube Cloud Fiap-Postech-SOAT1-Group21-Stage4 Projects](https://sonarcloud.io/organizations/fiap-postech-soat1-group21-stage4/projects)
  - [x] em caso de sucesso na etapa de CI, executará CD com build e deploy da imagem em DockerHub
      - [DockerHub - Repositório das Imagens 'buildadas'](https://hub.docker.com/u/dchagas)
- [x] Branches e repositórios protegidos

![image](https://github.com/fiap-postech-soat1-group21-stage4/.github/assets/83218983/57f8a3e1-35cf-4fb2-819c-d7e83afd78fc)

![image](https://github.com/fiap-postech-soat1-group21-stage4/.github/assets/83218983/e7054ab7-1772-4049-a11b-1219352bee1f)
![image](https://github.com/fiap-postech-soat1-group21-stage4/.github/assets/83218983/8d724a7a-c534-4023-8e8f-e4389050504f)


![image](https://github.com/fiap-postech-soat1-group21-stage4/.github/assets/83218983/050a6999-eac8-4f8a-863f-9089d30ce52a)

## Estrutura do Projeto
- `order-api`: Micro Service Application referente a gestão de pedidos.
- `payment-api`: MSA responsável pelo processamento de pagamentos.
- `customer-api`: MSA referente ao cliente.
- `product-api`: MSA referente aos produtos. 

## Tecnologias Utilizadas

- Github Actions
- SonarQube Cloud
- Golang
- Docker & Docker Hub
- PostgreSQL

## Instruções de Execução

### Pré-requisitos

- Docker instalado
- Go instalado (para desenvolvimento)

### Passos para Execução

1. Siga as instruções específicas de cada microsserviço para construir e executar.
