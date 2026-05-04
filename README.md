<img width="1536" height="1024" alt="diagrama geral" src="https://github.com/user-attachments/assets/1e8cb5b1-f911-4872-bd49-23654961bf13" />

# 🎟️ Sistema de Gestão e Venda de Ingressos

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)
![Bootstrap](https://img.shields.io/badge/bootstrap-%238511FA.svg?style=for-the-badge&logo=bootstrap&logoColor=white)

## 📌 Sobre o Projeto
Este é um sistema completo de gestão de venda de ingressos desenvolvido como parte acadêmica do bacharelado em Sistemas de Informação da Universidade Mogi das Cruzes (UMC). O foco principal da aplicação é a implementação de conceitos avançados de **Programação Orientada a Objetos (Herança e Polimorfismo)**, **Arquitetura MVC**, e **Segurança da Informação** utilizando o ecossistema Spring.

O projeto vai além do CRUD básico, implementando regras de negócio reais para cálculo de valores, cancelamento e políticas de devolução baseadas em datas, além de um módulo de autenticação protegido por tokens JWT.

## 🚀 Funcionalidades e Regras de Negócio

### Módulo de Ingressos
*   **Venda Dinâmica (Polimorfismo):** O sistema lida com diferentes instâncias de ingressos (Normal, VIP e Meia-Entrada), calculando taxas e descontos de forma dinâmica na camada de serviço.
*   **Persistência Inteligente (NoSQL):** Utilização do MongoDB para salvar diferentes tipos de ingressos na mesma collection, utilizando o atributo `_class` gerenciado pelo Spring Data.
*   **Gestão de Estado:** Controle do ciclo de vida do ingresso (Disponível ➡️ Pago ➡️ Cancelado / Devolvido).
*   **Política de Devolução:** Regra de negócio que calcula a diferença entre a data atual e a data do evento, permitindo reembolso apenas com antecedência superior a 7 dias.

### Módulo de Segurança (Auth)
*   **Autenticação JWT:** Geração de JSON Web Tokens válidos por 1 hora e armazenados em Cookies seguros (HTTPOnly).
*   **Proteção de Rotas:** Implementação de um `HandlerInterceptor` que bloqueia o acesso não autenticado às rotas sensíveis da aplicação.
*   **Prevenção contra Força Bruta:** Bloqueio automático da conta do usuário no banco de dados após 3 tentativas falhas de login.

## 🛠️ Tecnologias Utilizadas
*   **Backend:** Java 17, Spring Boot 3 (Web, Thymeleaf, Data MongoDB)
*   **Banco de Dados:** MongoDB
*   **Segurança:** JSON Web Token (jjwt)
*   **Frontend:** HTML5, CSS3, Bootstrap 5 (via CDN)

## 📊 Arquitetura e Modelagem
*(Dica: Adicione aqui as imagens dos seus diagramas UML! Faça o upload das imagens na pasta do projeto e use a tag abaixo para exibi-las)*

`![Diagramas do Sistema](caminho/para/sua/imagem.png)`

## ⚙️ Como executar o projeto localmente

**Pré-requisitos:**
*   Java 17+ instalado
*   Maven instalado
*   MongoDB rodando localmente na porta padrão (`localhost:27017`)

**Passo a passo:**
1. baixe o arquivo sistema-ingressos.zip:
   ```bash
   git clone [https://github.com/SEU-USUARIO/sistema-ingressos.git](https://github.com/SEU-USUARIO/sistema-ingressos.git)

2. Acesse a pasta do projeto: sistema-ingressos

3. Instale as dependências e rode a aplicação: mvn spring-boot:run

4. Acesse no navegador: http://localhost:8080/


Desenvolvido por Jonathas Eduardo Santos Ramos
