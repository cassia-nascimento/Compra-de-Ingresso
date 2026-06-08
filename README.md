<h1 align="center">
  🎟️ Compra de Ingressos — Oracle Next Education (ONE)
</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/Alura-ONE-Orange?style=for-the-badge" alt="Alura ONE">
</p>

Projeto prático de capacitação desenvolvido como parte da trilha de **Lógica de Programação e Manipulação do DOM com JavaScript**, integrado ao programa **Oracle Next Education (ONE)** em parceria com a **Alura**.

A aplicação simula um totem digital ou checkout de vendas para um evento corporativo/cultural (*e-ticket*). O usuário escolhe o tipo de bilhete desejado, define a quantidade e o sistema valida em tempo real se a operação respeita o teto de inventário disponível na memória local da página.

<p align="center"> <img src="assets/tela-inicial.png" alt="Tela Inicial" width="90%"> </p>

---

## 📌 Regras de Negócio & Engenharia de Lógica

O motor da aplicação (estruturado em `js/app.js`) gerencia o fluxo de checkout e o estado dos assentos adotando as seguintes diretrizes computacionais:

* **Isolamento de Escopo por Tipo de Bilhete:** A lógica lê reativamente o valor selecionado no componente `<select id="tipo-ingresso">` e roteia o fluxo para subfunções específicas dedicadas a cada setor (`comprarPista`, `comprarSuperior` ou `comprarInferior`).
* **Tratamento de Tipagem e Casting Numérico (`parseInt`):** Captura a string de texto inserida no input de quantidade e realiza a conversão explícita para o tipo primitivo de número inteiro (`parseInt`), blindando o motor analítico contra erros de concatenação de strings.
* **Mecanismo de Validação de Estoque (Inventário Local):** Antes de fechar a compra, o sistema intercepta o valor atualizado renderizado na tela e executa uma condicional estruturada. Se a quantidade solicitada for maior que o estoque do setor, o sistema bloqueia a transação e exibe um alerta de "Quantidade indisponível".
* **Atualização Reativa do DOM:** Caso a validação de estoque passe com sucesso, a aplicação calcula a subtração `estoqueDisponivel - quantidadeComprada`, injeta o novo saldo na tag HTML correspondente e limpa o campo de entrada para o próximo ciclo de venda.

---

## 📂 Organização dos Arquivos

```text
compra-de-ingresso
├── assets/             # Componentes visuais, logos estáticas e vetores estruturais
├── js/
│   └── app.js          # Camada de inteligência (regras de checkout e validação de estoque)
├── styles/
│   ├── _reset.css      # Normalização de estilos globais entre navegadores
│   └── style.css       # Layout responsivo, tipografias e tokens visuais
└── index.html          # Estrutura semântica e formulários da aplicação

```

---

## 🚀 Como Executar o Projeto

Como o ecossistema é baseado em front-end nativo puro (client-side), ele executa de forma imediata no navegador sem a necessidade de compiladores, contêineres ou prompts de servidor:

1. Realize o clone deste repositório em sua máquina:
```bash
git clone https://github.com/cassia-nascimento/compra-de-ingresso.git

```


2. Acesse a pasta do projeto:
```bash
cd compra-de-ingresso

```


3. Abra o arquivo `index.html` diretamente em seu navegador web de preferência (Chrome, Firefox, Safari ou Edge).

---

## 👩‍💻 Autora

Projeto de consolidação de condicionais e manipulação de variáveis desenvolvido por **Cássia Nascimento**.

* [GitHub Profile](https://github.com/cassia-nascimento)
* [LinkedIn](https://www.linkedin.com/in/cassia--nascimento/)
