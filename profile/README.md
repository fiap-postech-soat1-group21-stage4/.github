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

#### Pipelines Micro Services 
![image](https://github.com/fiap-postech-soat1-group21-stage4/.github/assets/83218983/dca5f82b-7df1-4fa1-b8fe-05e4a4f51586)

#### Caso de sucesso pipelines
![image](https://github.com/fiap-postech-soat1-group21-stage4/.github/assets/83218983/7aa01b7a-6542-4074-a84e-ed564f00f4a8)

#### Caso de erro pipelines
![image](https://github.com/fiap-postech-soat1-group21-stage4/.github/assets/83218983/8e944c13-08c3-4af3-9e7c-09758ff3063d)

## Estrutura do Projeto
- `order-api`: Micro Service Application referente a gestão de pedidos.
  - [![CI pipeline](https://github.com/fiap-postech-soat1-group21-stage4/order-api/actions/workflows/github-ci.yml/badge.svg)](https://github.com/fiap-postech-soat1-group21-stage4/order-api/actions/workflows/github-ci.yml) [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=fiap-postech-soat1-group21-stage4_order-api&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=fiap-postech-soat1-group21-stage4_order-api) [![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=fiap-postech-soat1-group21-stage4_order-api&metric=security_rating)](https://sonarcloud.io/summary/new_code?id=fiap-postech-soat1-group21-stage4_order-api) [![Bugs](https://sonarcloud.io/api/project_badges/measure?project=fiap-postech-soat1-group21-stage4_order-api&metric=bugs)](https://sonarcloud.io/summary/new_code?id=fiap-postech-soat1-group21-stage4_order-api) [![CD pipeline](https://github.com/fiap-postech-soat1-group21-stage4/order-api/actions/workflows/github-cd.yml/badge.svg)](https://github.com/fiap-postech-soat1-group21-stage4/order-api/actions/workflows/github-cd.yml)
- `payment-api`: MSA responsável pelo processamento de pagamentos.
  - [![CI pipeline](https://github.com/fiap-postech-soat1-group21-stage4/payment-api/actions/workflows/github-ci.yml/badge.svg)](https://github.com/fiap-postech-soat1-group21-stage4/payment-api/actions/workflows/github-ci.yml) [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=fiap-postech-soat1-group21-stage4_payment-api&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=fiap-postech-soat1-group21-stage4_payment-api) [![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=fiap-postech-soat1-group21-stage4_payment-api&metric=security_rating)](https://sonarcloud.io/summary/new_code?id=fiap-postech-soat1-group21-stage4_payment-api) [![Bugs](https://sonarcloud.io/api/project_badges/measure?project=fiap-postech-soat1-group21-stage4_payment-api&metric=bugs)](https://sonarcloud.io/summary/new_code?id=fiap-postech-soat1-group21-stage4_payment-api) [![CD pipeline](https://github.com/fiap-postech-soat1-group21-stage4/payment-api/actions/workflows/github-cd.yml/badge.svg)](https://github.com/fiap-postech-soat1-group21-stage4/payment-api/actions/workflows/github-cd.yml)
- `customer-api`: MSA referente ao cliente.
  - [![CI pipeline](https://github.com/fiap-postech-soat1-group21-stage4/customer-api/actions/workflows/github-ci.yml/badge.svg)](https://github.com/fiap-postech-soat1-group21-stage4/customer-api/actions/workflows/github-ci.yml) [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=fiap-postech-soat1-group21-stage4_customer-api&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=fiap-postech-soat1-group21-stage4_customer-api) [![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=fiap-postech-soat1-group21-stage4_customer-api&metric=security_rating)](https://sonarcloud.io/summary/new_code?id=fiap-postech-soat1-group21-stage4_customer-api) [![Bugs](https://sonarcloud.io/api/project_badges/measure?project=fiap-postech-soat1-group21-stage4_customer-api&metric=bugs)](https://sonarcloud.io/summary/new_code?id=fiap-postech-soat1-group21-stage4_customer-api) [![CD pipeline](https://github.com/fiap-postech-soat1-group21-stage4/customer-api/actions/workflows/github-cd.yml/badge.svg)](https://github.com/fiap-postech-soat1-group21-stage4/customer-api/actions/workflows/github-cd.yml)
- `product-api`: MSA referente aos produtos.
  - [![CI pipeline](https://github.com/fiap-postech-soat1-group21-stage4/product-api/actions/workflows/github-ci.yml/badge.svg)](https://github.com/fiap-postech-soat1-group21-stage4/product-api/actions/workflows/github-ci.yml) [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=fiap-postech-soat1-group21-stage4_product-api&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=fiap-postech-soat1-group21-stage4_product-api) [![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=fiap-postech-soat1-group21-stage4_product-api&metric=security_rating)](https://sonarcloud.io/summary/new_code?id=fiap-postech-soat1-group21-stage4_product-api) [![Bugs](https://sonarcloud.io/api/project_badges/measure?project=fiap-postech-soat1-group21-stage4_product-api&metric=bugs)](https://sonarcloud.io/summary/new_code?id=fiap-postech-soat1-group21-stage4_product-api) [![CD pipeline](https://github.com/fiap-postech-soat1-group21-stage4/product-api/actions/workflows/github-cd.yml/badge.svg)](https://github.com/fiap-postech-soat1-group21-stage4/product-api/actions/workflows/github-cd.yml)

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
