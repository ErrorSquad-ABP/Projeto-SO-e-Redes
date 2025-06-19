# 📚 Projeto de Hospedagem Local da ABP

<div align="center">

[![Status](https://img.shields.io/badge/⚙️_Status-Desenvolvimento-yellow?style=for-the-badge)](#-sobre-o-projeto)

</div>

---

## 📋 Sobre o Projeto

Projeto com foco na **hospedagem local** da ABP do primeiro semestre em máquinas Linux Mint (laboratório 103), evidenciando conhecimento de Redes e Sistemas Operacionais.

<details>
<summary><b>ℹ️ Informações do Projeto</b></summary>

| Categoria              | Detalhes                                                              |
| ---------------------- | --------------------------------------------------------------------- |
| 📍 Instituição         | FATEC Jacareí                                                          |
| 📚 Curso               | DSM - 1º Semestre 2025                                                |
| 🔄 Metodologia         | Aprendizagem Baseada em Projetos (ABP)                                |
| 👤 Focal Point         | Prof. Antonio Egydio Graça                                            |
| 📧 Contato             | [antonio.graca@fatec.sp.gov.br](mailto:antonio.graca@fatec.sp.gov.br) |
| 📅 Período             | 02/06/2025 – 23/06/2025                                               |
| ⚙️ Ferramentas         | PostgreSQL, Node.js, Visual Studio Code                               |
| 🖥️ Ambiente           | laboratório 103                                                        |
| 📊 Status              | Em desenvolvimento                                                    |

</details>

---

## 🎥 Demonstração em Vídeo

Link para o vídeo de apresentação:

`https://www.youtube.com/SEU-LINK-AQUI`

---

## 🛠️ Instalação dos Programas

Instruções de instalação no Linux Mint para as ferramentas necessárias:

<details>
<summary><b>PostgreSQL</b></summary>

```bash
sudo apt update
sudo apt install -y postgresql postgresql-client
sudo systemctl enable --now postgresql
sudo -i -u postgres psql -c "CREATE DATABASE abp_local;"
sudo -i -u postgres psql -c "CREATE USER lab_user WITH PASSWORD 'senha123';"
```

</details>

<details>
<summary><b>Node.js (LTS)</b></summary>

```bash
sudo apt install -y curl
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt install -y nodejs
node -v
```

</details>

<details>
<summary><b>Visual Studio Code</b></summary>

```bash
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
sudo install -o root -g root -m 644 microsoft.gpg /etc/apt/trusted.gpg.d/
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
sudo apt update
sudo apt install -y code
rm microsoft.gpg
```

</details>

---

## 🚧 Hospedagem do Projeto

### 🖥️ Hospedagem Front-end

1. **Clonar repositório Front-end:**

   ```bash
   git clone https://github.com/ErrorSquad-ABP/ErrorSquad-Front
   cd ErrorSquad-Front
   ```
2. **Instalar dependências e iniciar:**

   ```bash
   npm install
   npm run dev
   ```

### 🛠️ Hospedagem Back-end

1. **Clonar repositório Back-end:**

   ```bash
   git clone https://github.com/ErrorSquad-ABP/ErrorSquad-Server
   cd ErrorSquad-Server
   ```
2. **Instalar dependências e iniciar:**

   ```bash
   npm install
   npm run dev
   ```

### 🗄️ Hospedagem Banco de Dados

1. **Acessar serviço PostgreSQL:**

   ```bash
   sudo -i -u postgres psql
   ```
2. **Criar banco e usuário:**

   ```sql
   CREATE DATABASE abp_local;
   CREATE USER lab_user WITH PASSWORD 'senha123';
   GRANT ALL PRIVILEGES ON DATABASE abp_local TO lab_user;
   ```
3. **Executar migrações e seeders:**

   ````bash
   cd /caminho/para/ErrorSquad-Back
   npm run db:migrate
   npm run db:seed
   ```
---

## 👥 Nossa Equipe

### 🏢 Gestão
<div align="center">
<table>
 <tr>
   <td align="center">
     <b>Felipe Ferreira Pacheco</b><br>
     <i>Documentador</i><br>
     <a href="https://github.com/FelipePacheco30"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
     &nbsp;
     <a href="https://www.linkedin.com/in/felipe-ferreira-pacheco-621443347/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/></a>
   </td>
 </tr>
</table>
</div>

### 🖥️ Hospedagem
<div align="center">
<table>
 <tr>
   <th align="center">Front-end</th>
   <th align="center">Back-end</th>
   <th align="center">Banco de Dados</th>
 </tr>
 <tr>
   <td align="center">
     <b>João Victor Lopes Rosa</b><br>
     <i>Front-end</i><br>
     <a href="https://github.com/JV-L0pes"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
   </td>
   <td align="center">
     <b>Leonardo da Silva Irineu</b><br>
     <i>Back-end</i><br>
     <a href="https://github.com/Leo-Slv"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
   </td>
   <td align="center">
     <b>Tiago Jardel Costa</b><br>
     <i>Banco de Dados</i><br>
     <a href="https://github.com/Tiago199516"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
   </td>
 </tr>
</table>
</div>

### 💻 Desenvolvimento
<div align="center">
<table>
 <tr>
   <td align="center">
     <b>Arthur Facchinetti Peixoto</b><br>
     <a href="https://github.com/ArthurFacchinetti"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
     <a href="https://www.linkedin.com/in/arthur-facchinetti-669a6a2a7/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/></a>
   </td>
   <td align="center">
     <b>Alícia Silva Dias</b><br>
     <a href="https://github.com/TIALICIA"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
   </td>
   <td align="center">
     <b>Carlos Eduardo Espirito Santo</b><br>
     <a href="https://github.com/PromptdComando"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
     <a href="https://www.linkedin.com/in/carlos-eduardo-espirito-santo/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/></a>
   </td>
   <td align="center">
     <b>Caio Araujo</b><br>
     <a href="https://github.com/Caiuuutecnologico"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
     <a href="https://www.linkedin.com/in/caio-arauj/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/></a>
   </td>
 </tr>
</table>
</div>

---

## 👨‍🏫 Coordenação e Orientação

<div align="center">
 <table>
     <tr><td align="center"><b>Professor</b></td></tr>
     <tr>
         <td align="center">
             <b>Prof. Antonio Egydio Graça</b><br>
             <i>Professor Instrutor</i><br>
             <a href="https://github.com/antonioegydio"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
             <a href="https://www.linkedin.com/in/antonio-egydio/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/></a>
         </td>
     </tr>
 </table>
</div>

---

<div align="center">
 <img src="https://capsule-render.vercel.app/api?type=waving&color=4a90e2&height=100&section=footer" width="100%"/>
</div>

```
