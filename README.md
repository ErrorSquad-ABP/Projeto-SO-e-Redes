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

Link para o vídeo de apresentação (será adicionado após upload):

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
sudo -i -u postgres psql -c "GRANT ALL PRIVILEGES ON DATABASE abp_local TO lab_user;"
```

</details>

<details>
<summary><b>Node.js (LTS)</b></summary>

```bash
sudo apt install -y curl
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt install -y nodejs
node -v && npm -v
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

Para hospedar localmente o sistema ABP no laboratório 103, siga os passos:

1. **Clonar repositório:**

   ```bash
   ```

git clone [https://github.com/ErrorSquad-ABP/ErrorSquad-Front](https://github.com/ErrorSquad-ABP/ErrorSquad-Front)
cd ErrorSquad-Front

````
2. **Configurar variáveis de ambiente:**
Crie um arquivo `.env` com:
```env
DB_HOST=localhost
DB_USER=lab_user
DB_PASS=senha123
DB_NAME=abp_local
PORT=3000
````

3. **Instalar dependências Node.js:**

   ```bash
   ```

npm install

````
4. **Executar migrações e seeders (se aplicável):**
```bash
npm run db:migrate
npm run db:seed
````

5. **Iniciar servidor:**

   ```bash
   ```

6. **Acessar aplicação:**
Navegue até `http://localhost:3000` em qualquer máquina do grupo.

**Observações de Rede:**
- Certifique-se de que todas as máquinas estejam na mesma sub-rede do laboratório (ex: 192.168.1.0/24).
- Configure regras de firewall locais para liberar porta 3000.
- Utilize SSH ou VNC para acesso remoto entre as máquinas, se necessário.

---

## 👥 Nossa Equipe

<div align="center">
 <table>
     <tr>
         <td align="center"><b>Gestão</b></td>
         <td align="center"><b>Desenvolvimento</b></td>
     </tr>
     <tr>
         <td align="center">
             <b>Felipe Ferreira Pacheco</b><br>
             <i>Documentador</i><br>
             <a href="https://github.com/FelipePacheco30"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
             <a href="https://www.linkedin.com/in/felipe-ferreira-pacheco-621443347/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/></a>
         </td>
         <td align="center">
             <b>Arthur Facchinetti Peixoto</b><br>
             <a href="https://github.com/ArthurFacchinetti"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
             <b>João Victor Lopes Rosa</b><br>
             <a href="https://github.com/JV-L0pes"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
             <b>Tiago Jardel Costa</b><br>
             <a href="https://github.com/Tiago199516"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
             <b>Alícia Silva Dias</b><br>
             <a href="https://github.com/TIALICIA"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
             <b>Leonardo da Silva Irineu</b><br>
             <a href="https://github.com/Leo-Slv"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
             <b>Carlos Eduardo Espirito Santo</b><br>
             <a href="https://github.com/PromptdComando"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
             <b>Caio Araujo</b><br>
             <a href="https://github.com/Caiuuutecnologico"><img src="https://img.shields.io/badge/GitHub-333?style=flat-square&logo=github"/></a>
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
