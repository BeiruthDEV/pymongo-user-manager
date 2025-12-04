<p align="center">
  <img src="assets/logo-vassouras.png" alt="Universidade de Vassouras" width="400"/>
</p>

<h3 align="center">
  Universidade de Vassouras  
</h3>

---

### 📚 Curso: **Engenharia de Software**  
### 🖥️ Disciplina: **Banco de Dados Não Relacionais**  
### 👨‍🎓 Autor: **Matheus Beiruth**

---

## 🍃 PyMongo User Manager

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![Status](https://img.shields.io/badge/Status-Funcional-green?style=for-the-badge)

> Um módulo de interface de base de dados para gestão de utilizadores, implementando o ciclo completo de operações CRUD (Create, Read, Update, Delete) com persistência NoSQL.

## ⚙️ Funcionalidades

Este projeto abstrai a complexidade das queries do MongoDB em funções Python reutilizáveis:

* **Criação (Create):** Inserção de documentos JSON com validação implícita de tipos.
* **Leitura (Read):** Consultas flexíveis para recuperação de perfis.
* **Atualização (Update):** Modificação atómica de campos específicos (ex: atualizar apenas a idade sem reescrever o documento inteiro).
* **Remoção (Delete):** Exclusão segura de registos por identificadores.

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python 3
* **Driver de Banco de Dados:** `pymongo` (Driver oficial do MongoDB para Python)
* **Banco de Dados:** MongoDB (Community Edition)

## 🚀 Como Executar

### Pré-requisitos
1. Ter o **MongoDB** instalado e rodando localmente na porta padrão (`27017`).
2. Python 3.x instalado.

### Instalação

1. **Clone o repositório:
   ```bash
   git clone [https://github.com/BeiruthDEV/pymongo-user-manager.git](https://github.com/BeiruthDEV/pymongo-user-manager.git)
   cd pymongo-user-manager
   ```

2. **Crie um ambiente virtual (recomendado) e instale as dependências:

```bash

python -m venv venv
# Windows
.\venv\Scripts\activate
# Linux/Mac
source venv/bin/activate

pip install pymongo
```

3. **Execute o módulo:

```bash
python crud.py
```

## 💻 Exemplo de Uso (Snippet)
```bash

from crud import criar_usuario, ler_usuarios

# Inserindo um novo utilizador no sistema
criar_usuario("Matheus Beiruth", 25)

# Recuperando dados
usuarios = ler_usuarios()
for user in usuarios:
    print(f"ID: {user['_id']} | Nome: {user['nome']}")
```
## 🗄️ Estrutura do Banco de Dados
O sistema cria automaticamente a seguinte estrutura se ela não existir:
```bash
Database: meu_banco

Collection: usuarios

Document Schema:

JSON

{
  "_id": ObjectId("..."),
  "nome": "String",
  "idade": "Int"
}
```
## Autor
Matheus Beiruth
