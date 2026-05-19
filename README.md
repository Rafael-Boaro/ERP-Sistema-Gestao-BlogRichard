# 🚀 Case Study: Sistema de Gestão ERP Full-Stack com Painel Administrativo

Este repositório documenta a engenharia de software, o modelo de banco de dados relacional e as decisões arquiteturais aplicadas no desenvolvimento de um **Sistema de Gestão Empresarial (ERP) Full-Stack**. O sistema foi projetado de ponta a ponta para centralizar dados operacionais, automatizar processos manuais e servir como ferramenta de suporte à tomada de decisão gerencial.

> 🔒 **Nota de Privacidade e Compliance:** Por motivos de direitos acadêmicos e segurança institucional, o código-fonte original deste projeto é mantido em um repositório privado. Este ambiente serve como um *Showcase Técnico* detalhado e documentação de arquitetura.

---

## 📸 Demonstração Visual (Interface do Sistema)

Abaixo estão evidenciadas as quatro principais camadas operacionais do sistema rodando em ambiente de homologação. 
*(Para visualizar as imagens, substitua os caminhos pelos seus arquivos correspondentes ou faça o upload na pasta do repositório)*

### 1. Camada de Autenticação (Segurança de Borda)
A primeira linha de defesa do ecossistema. Implementa rotas protegidas e tratamento rigoroso de sessões para impedir acessos não autorizados.

![Tela de Login](login.jpg)

### 2. O Cérebro do Sistema (Dashboard Analítico)
Painel consolidado que consome consultas complexas do banco de dados em tempo real, transformando linhas de registros em totalizadores estratégicos para os gestores.

![Dashboard Principal](dashboard.jpg)

### 3. Controle de Acesso Baseado em Perfis (RBAC - Role-Based Access Control)
Módulo avançado de gerenciamento de usuários. Permite atribuir papéis específicos (Admin, Operador, Auditor) mitigando riscos de segurança e vazamento de dados de acordo com as diretrizes de governança.

![Gerenciar Usuários](gerenciar.jpg)

### 4. Orquestração de Regras de Negócio (Módulo CRUD)
Interface de manipulação de dados estruturada com validação pesada no back-end. Impede a inserção de dados corrompidos e lida com dados complexos como controle de inventário e códigos de barras.

![Adicionar Produto](crud.jpg)

---

## 🛠️ Stack Tecnológica & Engenharia

O ecossistema foi estruturado visando alta disponibilidade, manutenibilidade e baixo acoplamento entre as camadas.

- **Camada de Apresentação (Front-end):** Interface responsiva estruturada para garantir usabilidade ágil na linha de frente operacional, priorizando performance no carregamento de tabelas e renderização de dados dinâmicos.
- **Camada de Negócio (Back-end):** Arquitetura baseada em APIs RESTful, responsável pelo tratamento de exceções, roteamento protegido, sanitização de inputs e execução de controllers complexos.
- **Camada de Persistência (Banco de Dados):** Banco de Dados Relacional estruturado de forma estritamente normalizada para garantir integridade referencial absoluta, eliminação de redundâncias e alta velocidade em consultas indexadas.

---

## ⚙️ Principais Desafios Técnicos Solucionados

### 🧩 1. Implementação do Modelo RBAC (Role-Based Access Control)
Em vez de uma autenticação simples, o sistema valida dinamicamente o nível de permissão do usuário a cada requisição ao servidor. Se um usuário com nível operacional tentar acessar o endpoint de exclusão ou gerenciamento de usuários, o back-end intercepta a requisição e retorna um erro de segurança antes mesmo de tocar na camada de dados.

### 📊 2. Performance em Consultas de Agregação (Dashboard)
Para evitar o gargalo clássico de lentidão no painel administrativo, o banco de dados utiliza queries otimizadas com funções de agregação estruturadas. Isso garante que a contagem de inventário e os totalizadores gerenciais sejam processados no servidor de banco de dados de forma extremamente veloz, entregando a informação limpa para o front-end.

### 🛡️ 3. Validação e Higienização de Dados (Sanitização)
Nenhum dado inserido pelo usuário é considerado confiável. Todos os formulários (como o cadastro de novos itens) passam por um pipeline de validação que verifica tipos de dados, tamanhos de strings e impede vulnerabilidades como injeções maliciosas na persistência de dados.

---

## 📬 Contato Técnico
Estou totalmente disponível para detalhar as decisões de arquitetura, diagramas de entidade-relacionamento (DER) e lógicas de código aplicadas neste projeto.

- **LinkedIn:** [rafael-paolielo-boaro-1414b135a](https://www.linkedin.com/in/rafael-paolielo-boaro-1414b135a)
- **E-mail:** [rafaelboaro7@gmail.com](mailto:rafaelboaro7@gmail.com)
