# sgrequisicoes-ce
Sistema Gerenciador de Requisições de Compras

# 🚀 SGRequisicoes

Sistema de **Gestão de Compras** desenvolvido em **CodeIgniter 3** com **PHP 8**, **MariaDB** e **Bulma.io**.  
Uma aplicação moderna, leve e eficiente para o controle de requisições de compras, consumo e relatórios de desempenho.

---

## 🧩 Tecnologias Utilizadas

- ⚙️ [CodeIgniter 3](https://codeigniter.com/)
- 💻 [PHP 8+](https://www.php.net/)
- 🗄️ [MariaDB](https://mariadb.org/)
- 🎨 [Bulma.io](https://bulma.io/) (framework CSS)
- 🌐 Servidor Web: **Apache 2.4+**

---

## 📦 Requisitos do Sistema

Antes de iniciar a instalação, verifique se o ambiente atende aos seguintes requisitos:

| Requisito | Versão mínima |
|------------|----------------|
| PHP | 8.0 |
| Apache | 2.4 |
| MariaDB | 10.4 |
| Composer | 2.x (opcional, se quiser gerenciar dependências) |

---

## ⚙️ Instalação

### 1️⃣ Clone o repositório

```bash
git clone https://github.com/SEU_USUARIO/sgrequisicoes.git


Entre na pasta do projeto:
cd sgrequisicoes

2️⃣ Configure o ambiente

Crie o arquivo .env (ou use o application/config/config.php) e ajuste as configurações básicas:
cp .env.example .env

Em seguida, configure as variáveis de conexão com o banco de dados:

DB_HOST=localhost
DB_USER=root
DB_PASS=sua_senha
DB_NAME=sgrequisicoes

💡 Caso o .env não seja usado, configure diretamente no arquivo
application/config/database.php

3️⃣ Crie o banco de dados

No terminal do MariaDB:
CREATE DATABASE sgrequisicoes CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

Em seguida, importe o arquivo SQL com a estrutura inicial:
mysql -u root -p sgrequisicoes < database/sgrequisicoes.sql

4️⃣ Configure o servidor Apache

Adicione um virtual host (em /etc/apache2/sites-available/sgrequisicoes.conf):

<VirtualHost *:80>
    ServerName sgrequisicoes.local
    DocumentRoot /var/www/html/sgrequisicoes

    <Directory /var/www/html/sgrequisicoes>
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>

Ative o site e o módulo de reescrita:
sudo a2enmod rewrite
sudo a2ensite sgrequisicoes.conf
sudo systemctl reload apache2

5️⃣ Teste o sistema

Abra no navegador:
http://sgrequisicoes.local

Se tudo estiver certo, o painel inicial do SGRequisicoes será exibido 🎉

🎨 Estilo e Layout

O frontend utiliza Bulma.io
, garantindo um design moderno, responsivo e leve.
Você pode personalizar o tema em:

assets/css/custom.css

🧰 Estrutura do Projeto

sgrequisicoes/
├── application/
│   ├── config/
│   ├── controllers/
│   ├── models/
│   ├── views/
│   └── ...
├── assets/
│   ├── css/
│   ├── js/
│   └── images/
├── system/               # Núcleo do CodeIgniter
├── database/
│   └── sgrequisicoes.sql
└── index.php

