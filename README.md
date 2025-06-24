# 📚 Projeto de Hospedagem Local da ABP

<div align="center">

[![Status](https://img.shields.io/badge/⚙️_Status-Concluido-green?style=for-the-badge)](#-sobre-o-projeto)

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
| 🖥️ Ambiente           | Laboratório 103                                                        |
| 📊 Status              | Concluido                                                    |

</details>

---

## 🎥 Demonstração em Vídeo

<a href="https://www.youtube.com/watch?v=fNmHGEbLYmg" target="_blank">👉 Clique AQUI para assistir à apresentação</a>

---

## 🛠️ Instalação dos Programas

<details>
<summary><b>PostgreSQL</b></summary>

```bash
sudo apt update
sudo apt install postgresql postgresql-contrib
sudo systemctl status postgresql
sudo -i -u postgres
psql --version
```
</details>

<details>
<summary><b>Node.js (LTS)</b></summary>

```bash
sudo apt install nodejs
node -v
```
</details>

<details>
<summary><b>Visual Studio Code</b></summary>

```bash
https://code.visualstudio.com/

https://code.visualstudio.com/Download

https://code.visualstudio.com/docs/?dv=linux64_deb
```
</details>

---

## 🚧 Hospedagem do Projeto

<details>
<summary><b>🖥️ Hospedagem Front-end</b></summary>

1. **Clonar o repositório Front-end:**

```bash
git clone https://github.com/ErrorSquad-ABP/ErrorSquad-Front
cd ErrorSquad-Front
```

2. **Instalar dependências e iniciar:**

```bash
npm install
npm run dev
```

</details>

<details>
<summary><b>🛠️ Hospedagem Back-end</b></summary>

1. **Clonar o repositório Back-end:**

```bash
git clone https://github.com/ErrorSquad-ABP/ErrorSquad-Server
cd ErrorSquad-Server
```
2. **Instalar dependências e iniciar:**

```bash
npm install
npm run dev
```

</details>

<details>
<summary><b>🗄️ Hospedagem Banco de Dados</b></summary>

1. **Acessar serviço PostgreSQL:**

```bash
sudo systemctl start postgresql
```

2. **Criar banco de dados e usuário:**

```bash
sudo -i -u postgres
psql
CREATE DATABASE abp_local;
CREATE USER lab_user WITH PASSWORD 'senha123';
GRANT ALL PRIVILEGES ON DATABASE abp_local TO lab_user;
```

3. **Verificar se a porta 5432 está liberada:**

```bash
sudo netstat -tlnp | grep 5432
```

</details>

---

<details>
<summary><b>🔍 Verificação de portas e status</b></summary>

- **Ver status do UFW:**

```bash
sudo ufw status
```

- **Ver portas em uso:**

```bash
sudo netstat -tlnp
# ou
sudo ss -tlnp
```

</details>

<details>
<summary><b>🚫 Desativando o firewall temporariamente (apenas para testes)</b></summary>

**Ubuntu / Debian:**

```bash
sudo ufw disable
```

**CentOS / RHEL / Fedora:**

```bash
sudo systemctl stop firewalld
```

</details>

<details>
<summary><b>✅ Resumo</b></summary>

| Serviço              | Porta | Comando UFW             |
| -------------------- | ----- | ---------------------- |
| Back-end API         | 8000  | `sudo ufw allow 8000`  |
| Front-end (Vite)     | 5173  | `sudo ufw allow 5173`  |
| Banco de Dados (Postgres) | 5432 | `sudo ufw allow 5432` |

</details>

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
