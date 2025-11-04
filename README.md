# 🚀 Projeto de Engenharia de Dados – NovaDrive Motors

[![AWS](https://img.shields.io/badge/AWS-EC2-orange?style=for-the-badge&logo=amazon-aws)](#)
[![Docker](https://img.shields.io/badge/Docker-Container-blue?style=for-the-badge&logo=docker)](#)
[![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-Orquestra%C3%A7%C3%A3o-017CEE?style=for-the-badge&logo=apache-airflow)](#)
[![Snowflake](https://img.shields.io/badge/Snowflake-Data%20Warehouse-29B5E8?style=for-the-badge&logo=snowflake)](#)
[![DBT](https://img.shields.io/badge/DBT-Transforma%C3%A7%C3%A3o-FD3A5C?style=for-the-badge&logo=dbt)](#)
[![PostgreSQL](https://img.shields.io/badge/Postgres-Fonte%20de%20Dados-336791?style=for-the-badge&logo=postgresql)](#)
[![Python](https://img.shields.io/badge/Python-Script%20ETL-yellow?style=for-the-badge&logo=python)](#)
[![Power BI](https://img.shields.io/badge/Power%20BI-Visualiza%C3%A7%C3%A3o-FFC300?style=for-the-badge&logo=power-bi)](#)

---

## 💡 Contexto do Projeto

O projeto foi inspirado em um **bootcamp de Engenharia de Dados**, simulando o ambiente de uma empresa fictícia: **NovaDrive Motors**, fabricante de veículos.

> 🎯 **Objetivo:** criar um **pipeline de dados completo** para integrar informações do ERP (Postgres) a um Data Warehouse (Snowflake), com orquestração via Airflow e transformação via DBT.

O resultado final é um **Data Warehouse analítico** pronto para consumo em ferramentas de **Business Intelligence (Power BI / Looker Studio)**.

---

## 🧱 Arquitetura da Solução

```text
        +-------------+
        |   Postgres  |
        | (ERP Fonte) |
        +-------------+
               |
               v
        +-------------+
        |   Airflow   |  ->  Executado em EC2 (Ubuntu + Docker)
        | Orquestrador|
        +-------------+
               |
               v
        +-------------+
        |  Snowflake  |
        | Data Staging|
        +-------------+
               |
               v
        +-------------+
        |     DBT     |
        |Transformação|
        +-------------+
               |
               v
        +-------------+
        | BI Tool (Power BI / Looker) |
        +-------------+
