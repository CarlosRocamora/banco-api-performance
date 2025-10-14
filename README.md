# banco-api-performance

## Introdução
Este repositório contém testes de performance para uma API bancária, utilizando JavaScript e a ferramenta K6. O objetivo é validar a performance dos principais fluxos do sistema, garantindo estabilidade e eficiência sob carga.

## Tecnologias Utilizadas
- [K6](https://k6.io/) — Ferramenta de teste de carga e performance
- JavaScript — Linguagem utilizada para os scripts de teste

## Estrutura do Repositório
```
aula.test.js
html-report.html
README.md
config/
	config.local.json
fixtures/
	postLogin.json
helpers/
	autenticacao.js
tests/
	login.test.js
	transferencias.test.js
utils/
	variaveis.js
```

### Objetivo de cada grupo de arquivos
- **aula.test.js**: Exemplo ou script de teste geral.
- **html-report.html**: Relatório de performance exportado pelo K6.
- **config/**: Arquivos de configuração do projeto, como variáveis de ambiente e endpoints.
- **fixtures/**: Dados estáticos utilizados nos testes, como payloads de requisições.
- **helpers/**: Funções auxiliares para autenticação e outras rotinas comuns.
- **tests/**: Scripts de teste organizados por fluxo (ex: login, transferências).
- **utils/**: Utilitários e variáveis globais usadas nos scripts.

## Modo de Instalação
1. Clone o repositório:
	 ```sh
	 git clone https://github.com/CarlosRocamora/banco-api-performance.git
	 cd banco-api-performance
	 ```
2. Instale o K6 seguindo as instruções oficiais: https://k6.io/docs/getting-started/installation/

## Modo de Execução do Projeto
1. Defina a variável de ambiente `BASE_URL` com a URL da API a ser testada. Exemplo:
	 ```sh
	 export BASE_URL=https://sua-api.com
	 ```
	 No Windows PowerShell:
	 ```powershell
	 $env:BASE_URL="https://sua-api.com"
	 ```
2. Execute um teste com o K6:
	 ```sh
	 k6 run tests/login.test.js
	 ```
3. Para acompanhar o relatório em tempo real e exportar o resultado em HTML, utilize as variáveis de ambiente do K6:
	 ```sh
	 K6_WEB_DASHBOARD=true K6_WEB_DASHBOARD_EXPORT=html-report.html k6 run tests/login.test.js
	 ```
	 No Windows PowerShell:
	 ```powershell
	 $env:K6_WEB_DASHBOARD="true"; $env:K6_WEB_DASHBOARD_EXPORT="html-report.html"; k6 run tests/login.test.js
	 ```

O relatório será salvo no arquivo `html-report.html` na raiz do projeto.

---

Repositório: [github.com/CarlosRocamora/banco-api-performance](https://github.com/CarlosRocamora/banco-api-performance)