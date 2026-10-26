# 🌙 PortuLua IDE

> **Uma linguagem de programação moderna baseada em Portugol, com integração nativa à Web.**

[![PortuLua IDE](https://img.shields.io/badge/PortuLua-IDE-blue?style=for-the-badge&logo=javascript)](#)
[![Status](https://img.shields.io/badge/Status-Online-success?style=for-the-badge)](#)
[![Autor](https://img.shields.io/badge/Autor-Walney%20Moreira%20Klein-orange?style=for-the-badge)](mailto:walneyk@hotmail.com)

Bem-vindo ao **PortuLua**, uma IDE (Ambiente de Desenvolvimento Integrado) completa que roda diretamente no seu navegador. Criada para facilitar o aprendizado de lógica de programação, o PortuLua expande os conceitos tradicionais do VisuAlg adicionando recursos poderosos do mundo moderno, como funções personalizadas, requisições HTTP e leitura de JSON.

---

## 🚀 Acesse o PortuLua Online

Você não precisa instalar nada. Acesse a IDE e o Manual diretamente pelo GitHub Pages:

*   💻 **[Abrir o PortuLua IDE](https://walneynf.github.io/portulua/)**
*   📘 **[Ler o Manual de Referência](https://walneynf.github.io/portulua/manual.html)**

---

## ✨ O que torna o PortuLua especial?

Diferente de outros interpretadores de Portugol, o PortuLua foi construído do zero em JavaScript puro (Vanilla JS) e possui recursos de linguagens de mercado:

*   **Lógica Clássica:** Variáveis, vetores, condicionais (`se`, `escolha`) e laços (`enquanto`, `para`, `repita`).
*   **Funções Personalizadas:** Crie as suas próprias funções com parâmetros e retorno (`funcao ... retorne ... fimfuncao`).
*   **Acesso à Internet:** Faça requisições HTTP e consuma APIs públicas (ViaCEP, JokeAPI, etc.).
*   **Leitura de JSON:** Extraia dados de APIs de forma simples usando `pega_json()`.
*   **Biblioteca Nativa:** Funções matemáticas (`raizq`, `aleatorio`) e de texto (`maiuscula`, `compr`).
*   **IDE Completa:** Editor de código (Monaco), múltiplas abas, salvamento automático no navegador e exportação de arquivos com a extensão `.wmk`.

---

## 💻 Exemplo Rápido

Aqui está um exemplo de como é fácil buscar um endereço na internet usando o PortuLua:

```pascal
algoritmo "BuscaCEP"
var
   url, logradouro, bairro: caractere
inicio
   escreval("Digite o CEP (somente numeros):")
   leia(cep)
   
   url <- "https://viacep.com.br/ws/" + cep + "/json/"
   requisicao(url)
   
   logradouro <- pega_json("logradouro")
   bairro <- pega_json("bairro")
   
   escreval("Rua: ", logradouro)
   escreval("Bairro: ", bairro)
fimalgoritmo
