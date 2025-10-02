# Banco API Tests

## 📌 Objetivo
Este projeto tem como finalidade realizar testes automatizados na [API Rest Banco](https://github.com/juliodelimas/banco-api), validando suas funcionalidades e contribuindo a qualidade do sistema.  

A automação cobre cenários de requisições HTTP, validações de resposta, status codes e estrutura de dados retornados.  

---

## 🛠️ Stack Utilizada
O projeto é desenvolvido em **JavaScript** com uso das seguintes bibliotecas:  

- [Mocha](https://mochajs.org/) → Framework de testes  
- [Chai](https://www.chaijs.com/) → Biblioteca de asserções  
- [Supertest](https://github.com/visionmedia/supertest) → Testes de API HTTP  
- [Mochawesome](https://github.com/adamgruber/mochawesome) → Geração de relatórios em HTML  
- Outras dependências listadas em [`package.json`](./package.json)  

---

## 📂 Estrutura de Diretórios
```bash
banco-api-tests/
│── mochawesome/        # Relatórios gerados pelo mochawesome
│── node_modules/       # Dependências instaladas
│── test/               # Testes automatizados
│   ├── login.test.js
│   └── transferencias.test.js
│── .env                # Variáveis de ambiente (não versionado)
│── .gitignore          # Arquivo para configuração de variável BASE_URL
│── package.json
│── package-lock.json
└── README.md
```

## ⚙️ Configuração do `.env`
O arquivo `.env` precisa ser criado na raiz do projeto com o seguinte conteúdo:  

```env
BASE_URL=http://localhost:3000
```

- `BASE_URL` → Define a URL base da API que será testada.  

---

## ▶️ Executando os Testes
1. Instale as dependências:  
   ```bash
   npm install
   ```

2. Execute os testes:  
   ```bash
   npm test
   ```

3. Gerar relatório com **Mochawesome**:  
   Após a execução, um relatório em HTML será gerado automaticamente no diretório `mochawesome/`.  

   Para abrir o relatório no navegador:  
   ```bash
   open mochawesome/mochawesome.html   # macOS
   start mochawesome/mochawesome.html  # Windows
   xdg-open mochawesome/mochawesome.html # Linux
   ```

---

## 📚 Documentações das Dependências
- [Mocha](https://mochajs.org/)  - Framework de execução de testes
- [Chai](https://www.chaijs.com/)  - Biblioteca de asserções
- [Supertest](https://github.com/visionmedia/supertest)   - Biblioteca para chamadas HTTP
- [Mochawesome](https://github.com/adamgruber/mochawesome)  - Geração de relatórios em HTML
- [dotenv](https://www.npmjs.com/package/dotenv)  - Gerenciamento de variáveis de ambiente
