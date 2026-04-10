# 🩺 Med Control

## 📌 Descrição

O **Med Control** é um sistema web de **controle e gerenciamento médico**, desenvolvido para auxiliar clínicas e médicos no gerenciamento de pacientes, consultas e prontuários.

O sistema permite:

* Cadastro de pacientes e médicos
* Agendamento de consultas
* Registro de prontuários médicos
* Controle de usuários com autenticação

🎯 **Problema que resolve:**
Organizar e centralizar informações médicas, substituindo controles manuais e reduzindo erros no atendimento.

---

## 🛠️ Tecnologias Utilizadas

### Backend

* .NET / ASP.NET Core
* Entity Framework Core
* PostgreSQL

### Frontend

* React
* JavaScript
* Axios

---

## ⚙️ Pré-requisitos

Antes de rodar o projeto, você precisa ter instalado:

* Node.js (v16 ou superior)
* .NET SDK (6 ou superior)
* PostgreSQL
* Git

---

## 🚀 Como Executar o Projeto

### 🔹 1. Clonar o repositório

```bash
git clone https://github.com/seu-repositorio.git
cd med-control
```

---

### 🔹 2. Configurar o Banco de Dados

Crie um banco no PostgreSQL chamado:

```
MedControlDB
```

No arquivo `appsettings.json`, configure:

```json
"ConnectionStrings": {
  "DefaultConnection": "Host=localhost;Port=5432;Database=MedControlDB;Username=postgres;Password=123456"
}
```

⚠️ Ajuste usuário e senha conforme seu PostgreSQL

---

### 🔹 3. Instalar Provider do PostgreSQL

```bash
dotnet add package Npgsql.EntityFrameworkCore.PostgreSQL
```

---

### 🔹 4. Rodar as Migrations

```bash
dotnet ef migrations add InitialCreate
dotnet ef database update
```

---

### 🔹 5. Executar o Backend

```bash
dotnet run
```

A API estará disponível em:

```
https://localhost:5001
```

---

### 🔹 6. Executar o Frontend

```bash
cd frontend
npm install
npm start
```

O sistema abrirá em:

```
http://localhost:3000
```

---

## 🔌 Endpoints da API

### 👤 Pacientes

* GET /api/pacientes
* POST /api/pacientes
* PUT /api/pacientes/{id}
* DELETE /api/pacientes/{id}

### 🩺 Médicos

* GET /api/medicos
* POST /api/medicos

### 📅 Consultas

* GET /api/consultas
* POST /api/consultas

### 📋 Prontuários

* GET /api/prontuarios
* POST /api/prontuarios

📌 Swagger disponível em:

```
https://localhost:5001/swagger
```

---

## 🧩 Diagrama de Entidades (DER)

```
USUARIOS → MEDICOS → CONSULTAS ← PACIENTES
                         │
                         ▼
                   PRONTUARIOS
```

---

## 👥 Integrantes do Projeto

* Guilherme Lucas Pierri – Backend (API e banco de dados)- Frontend (React e interface)
* Tarcísio Ferreira Casagrande – Backend (API e banco de dados) - Frontend (React e interface)

---

## 📋 Divisão de Tarefas

| Integrante                   | Responsabilidades                |
| ---------------------------- | -------------------------------- |
| Guilherme Lucas Pierri       | Modelagem do banco, EF Core, API |
| Tarcísio Ferreira Casagrande | Interface React, consumo da API  |

---

## ✅ Status do Projeto

✔️ CRUD completo implementado
✔️ Relacionamentos 1:N e 1:1
✔️ Migrations funcionando
✔️ Sistema funcional

---

## 📌 Observações

* O sistema utiliza banco PostgreSQL (persistente)
* Os dados permanecem salvos após reiniciar a aplicação
* Projeto desenvolvido para fins acadêmicos

---
