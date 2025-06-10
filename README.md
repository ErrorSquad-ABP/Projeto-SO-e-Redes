# Projeto de Gerenciamento Acadêmico com Grade de Horários e Mapa Interativo

## 📌 Resumo do Projeto

Este repositório contém o sistema de **gerenciamento acadêmico**, desenvolvido como parte da disciplina de Sistemas Operacionais e Redes. O objetivo principal é **pegar nosso projeto da ABP** (Aprendizagem Baseada em Projetos) e **hospedá-lo localmente** nas máquinas do laboratório 103, simulando um ambiente real de rede e servidor.

Principais funcionalidades:

* **Mapa interativo** das salas de aula, mostrando professor, disciplina e horários.
* **Grade de horários** dinâmica, filtrável por turma e professor.
* **Banco de dados** PostgreSQL integrado.
* **Hospedagem local** em servidor Node.js, com acesso via rede interna.
* **Interface responsiva** para diferentes tamanhos de tela.

<details>
<summary>🛠 Processo</summary>

1. **Clonar o repositório** na máquina do laboratório 103.
2. **Instalar dependências** e ferramentas necessárias (PostgreSQL, Node.js, VS Code).
3. **Configurar o banco de dados** local e executar o script de criação de esquema e dados iniciais.
4. **Instalar dependências Node.js** do projeto.
5. **Iniciar o servidor** e acessar via navegador em `http://localhost:3000`.
6. **Validar o funcionamento** do mapa interativo e da grade de horários.

</details>

<details>
<summary>💻 Instalação no Linux Mint (Laboratório 103)</summary>

### 1. PostgreSQL

```bash
# Atualizar lista de pacotes
sudo apt update

# Instalar PostgreSQL e cliente
sudo apt install -y postgresql postgresql-client

# Iniciar e habilitar o serviço
sudo systemctl start postgresql
sudo systemctl enable postgresql

# Acessar o usuário postgres para criar banco/usuário
sudo -i -u postgres
psql
-- Dentro do psql:
CREATE DATABASE academia;
CREATE USER lab_user WITH ENCRYPTED PASSWORD 'senha123';
GRANT ALL PRIVILEGES ON DATABASE academia TO lab_user;
\q
exit
```

### 2. Node.js (versão LTS)

```bash
# Instalar dependências para adicionar repositório
sudo apt install -y curl

# Baixar e executar o script de instalação do NodeSource para LTS
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -

# Instalar Node.js
sudo apt install -y nodejs

# Verificar versões
node -v
npm -v
```

### 3. Visual Studio Code

```bash
# Importar a chave do repositório Microsoft
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
sudo install -o root -g root -m 644 microsoft.gpg /etc/apt/trusted.gpg.d/

# Adicionar o repositório do VS Code
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'

# Atualizar e instalar
sudo apt update
sudo apt install -y code

# Remover arquivo temporário
rm microsoft.gpg
```

</details>

## 🎥 Demonstração em Vídeo

Confira o funcionamento completo do sistema no vídeo a seguir (link será adicionado em breve):

👉 [Assista no YouTube](https://www.youtube.com/SEU-LINK-AQUI)

---

*Laboratório 103 – Sistemas Operacionais e Redes*
