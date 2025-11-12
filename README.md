# 🦋 Hollow Knight – Gerenciador de Personagens

## 📖 Descrição do Projeto
Este projeto é uma aplicação web desenvolvida em **PHP** com arquitetura **MVC (Model–View–Controller)** e banco de dados **MySQL**.  
O sistema tem como objetivo **gerenciar personagens do universo de Hollow Knight**, permitindo cadastrar, visualizar, editar e excluir informações sobre cada personagem, como nome, imagem e habilidades.

O projeto serve como exemplo prático de uma aplicação CRUD (*Create, Read, Update, Delete*), demonstrando a integração entre PHP, HTML e SQL em um ambiente web dinâmico.

---

## ⚙️ Configuração e Execução

### 🧩 Pré-requisitos
- Servidor local com suporte a **PHP** e **MySQL** (exemplo: [XAMPP](https://www.apachefriends.org/), [WAMP](https://www.wampserver.com/)).
- Navegador web atualizado.

---

### 🚀 Passos para Instalar e Executar

1. Extraia a pasta `Hollow Knight` para o diretório do seu servidor local:  
   ```bash
   C:\xampp\htdocs\Hollow Knight
   ```

2. Inicie o **Apache** e o **MySQL** no painel de controle do XAMPP/WAMP.

3. Acesse o **phpMyAdmin** pelo navegador:  
   ```
   http://localhost/phpmyadmin
   ```

4. Importe o arquivo SQL localizado em:  
   ```
   Hollow Knight/data/Hollow Knight.sql
   ```
   Isso criará automaticamente o banco de dados e as tabelas.

5. Verifique o arquivo de configuração do banco de dados:  
   ```
   Hollow Knight/config/database.php
   ```
   Ajuste as credenciais conforme o seu ambiente local (usuário, senha, host, etc).

6. No navegador, acesse o projeto:  
   ```
   http://localhost/Hollow Knight/
   ```

Se tudo estiver configurado corretamente, o sistema exibirá a lista de personagens e permitirá a manipulação dos dados.

---

## 🗄️ Estrutura do Banco de Dados

```sql
CREATE DATABASE IF NOT EXISTS hollow_knight;

USE hollow_knight;

CREATE TABLE IF NOT EXISTS personagens (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    arquivo_foto VARCHAR(255) NOT NULL,
    habilidades TEXT 
);

INSERT INTO personagens (nome, arquivo_foto, habilidades)
VALUES
('Hollow Knight', 'knight.png', 'Golpes com Ferrão\nDash Sombrio\nAsas do Monarca\nFúria dos Caídos'),
('Hornet', 'hornet.png', 'Arremesso de Agulha\nGiro Acrobático\nLinha da Seda\nGuardião Ágil'),
('Grimm', 'grimm.png', 'Chamas do Grimmkind\nTeleporte Sombrio\nDança Cremosa\nInvocar Servos'),
('Radiância', 'radiancia.png', 'Luz Purificadora\nSurtos de Luz\nTeletransporte Etéreo\nEspadas de Luz');
```

---

## 🧠 Tecnologias Utilizadas
- **PHP** — Lógica de aplicação (Controllers, Models, Views)  
- **MySQL** — Armazenamento e manipulação dos dados  
- **HTML/CSS** — Estrutura e estilo das páginas  
- **MVC** — Padrão de arquitetura para organização do código

---

## 💡 Autor
Projeto desenvolvido como prática de programação web, inspirado no universo de *Hollow Knight*.
