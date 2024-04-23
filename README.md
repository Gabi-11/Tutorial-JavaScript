# Tutorial-JavaScript
Este guia oferece um passo a passo detalhado sobre como utilizar JavaScript. 

## O que é Java Script?
JavaScript é uma linguagem de programação usada por desenvolvedores para fazer páginas interativas da Internet. As funções de JavaScript podem melhorar a experiência do usuário durante a navegação em um site, como, por exemplo, desde a atualização do feed na página da mídia social até a exibição de animações e mapas interativos. Como uma linguagem de script do lado do cliente, ele é uma das tecnologias principais da World Wide Web. Por exemplo, ao navegar na Internet, é possível visualizar a qualquer momento um carrossel de imagens, um menu suspenso “clicar para visualizar” ou mesmo mudar dinamicamente as cores dos elementos de uma página da Web. Tudo isso graças ao JavaScript.

## Configuração do Ambiente

1. **Instalação do Node.js:** O Node.js é uma plataforma que permite executar JavaScript no servidor. Você pode baixá-lo e instalá-lo a partir do site oficial do Node.js.

2. **Editor de texto ou IDE:** Escolha um editor de texto ou uma IDE (Ambiente de Desenvolvimento Integrado) para escrever seu código JavaScript. Alguns exemplos populares são Visual Studio Code, Sublime Text e Atom.

3. **Terminal ou prompt de comando:** Você precisará de um terminal ou prompt de comando para executar comandos relacionados ao Node.js, como instalar pacotes e iniciar servidores locais.

4. **Sistema de controle de versão:** É uma boa prática usar um sistema de controle de versão como o Git para rastrear e gerenciar o código-fonte do seu projeto.

5. **Gerenciador de pacotes npm ou Yarn:** O npm (Node Package Manager) e o Yarn são gerenciadores de pacotes para o Node.js. Eles permitem instalar e gerenciar as dependências do seu projeto, como bibliotecas e frameworks.

6. **Configuração do projeto:** No seu terminal, navegue até o diretório do seu projeto e execute npm init ou yarn init para criar um arquivo package.json, que contém informações sobre o seu projeto e suas dependências.

7. **Instalação de dependências:** Use o npm ou o Yarn para instalar as dependências do seu projeto. Por exemplo, para instalar o Express (um framework para Node.js), você pode executar npm install express ou yarn add express.

8. **Configuração do ambiente de desenvolvimento:** Dependendo das necessidades do seu projeto, você pode configurar ferramentas adicionais, como transpiladores (Babel para escrever código JavaScript moderno compatível com navegadores antigos), bundlers (Webpack para agrupar e otimizar arquivos JavaScript, CSS, etc.) e linters (ESLint para ajudar a manter um código consistente e sem erros).
Essas são as etapas básicas para configurar o ambiente de desenvolvimento para JavaScript. Conforme você avança no desenvolvimento do seu projeto, pode explorar ferramentas e técnicas adicionais para otimizar o processo de desenvolvimento e a qualidade do código.


## Sintaxe Básica

JavaScript pega emprestado a maior parte de sua sintaxe do Java, mas também é influenciado por Awk, Perl e Python. No JavaScript, instruções são chamadas de declaração e são separadas por um ponto e vírgula (;). Espaços, tabulação e uma nova linha são chamados de espaços em branco. O código fonte dos scripts em JavaScript são lidos da esquerda para a direita e são convertidos em uma sequência de elementos de entrada como simbolos, caracteres de controle, terminadores de linha, comentários ou espaço em branco.

## Variáveis

Você usa variáveis como nomes simbólicos para os valores em sua aplicação. O nome das variáveis, chamados de identificadores, obedecem determinadas regras. Um identificador JavaScript deve começar com uma letra, underline (_), ou cifrão ($); os caracteres subsequentes podem também ser números (0-9). Devido JavaScript ser case-sensitive, letras incluem caracteres de "A" a "Z" (maiúsculos) e caracteres de "a" a "z" (minúsculos).

* Variável com Let: Usado para declarar uma variável mutável
```
let nome = "João";
let idade = 30;

console.log(nome); // Saída: João
console.log(idade); // Saída: 30
```
* Variável com Const: Usado para declarar constantes, ou seja, variáveis imutáveis cujo valor não pode ser alterado depois de definido.
````
const PI = 3.14;
const SITE_URL = "https://www.exemplo.com";

console.log(PI); // Saída: 3.14
console.log(SITE_URL); // Saída: https://www.exemplo.com
````



* Variáveis de Objetos: Além de armazenar valores simples, let pode ser usado para declarar variáveis que referenciam objetos complexos, como um objeto pessoa.

````
let pessoa = {
    nome: "Maria",
    idade: 25,
    cidade: "São Paulo"
};

console.log(pessoa.nome); // Saída: Maria
console.log(pessoa.idade); // Saída: 25
console.log(pessoa.cidade); // Saída: São Paulo

````

## Tipos de Dados

### Tipo Boolean
Boolean representa uma entidade lógica e pode ter dois valores: true e false.

````
let isAtivo = true;
let estaChovendo = false;

console.log(isAtivo); // Saída: true
console.log(estaChovendo); // Saída: false

````
````
let usuarioLogado = true;

if (usuarioLogado) {
    console.log("Bem-vindo! Você está logado.");
} else {
    console.log("Por favor, faça o login para continuar.");
}
````
### Tipo Null
O tipo Null tem exatamente um valor: null.

````
let variavelNula = null;

console.log(variavelNula); // Saída: null

````
````
let valor = null;

if (valor === null) {
    console.log("A variável não possui um valor válido.");
} else {
    console.log("O valor da variável é: " + valor);
}
````
### Tipo Number
O tipo Number é um valor IEEE 754 de formato binário de 64 bits de precisão dupla. É capaz de armazenar números de ponto flutuante positivos entre 2^-1074 (Number.MIN_VALUE) e 2^1024 (Number.MAX_VALUE), bem como números de ponto flutuante negativos entre -(2^-1074) e -(2^1024), mas só pode armazenar com segurança inteiros no intervalo -(2^53 − 1) (Number.MIN_SAFE_INTEGER) para 2^53 − 1 (Number.MAX_SAFE_INTEGER).

````
let numeroInteiro = 42;
let numeroDecimal = 3.14;

console.log(numeroInteiro); // Saída: 42
console.log(numeroDecimal); // Saída: 3.14

````
## Funções
Funções são blocos de construção fundamentais em JavaScript. Uma função é um procedimento de JavaScript - um conjunto de instruções que executa uma tarefa ou calcula um valor. Para usar uma função, você deve defini-la em algum lugar no escopo do qual você quiser chamá-la.

A definição da função (também chamada de declaração de função) consiste no uso da palavra chave function (en-US), seguida por:

* Nome da Função.
* Lista de argumentos para a função, entre parênteses e separados por vírgulas.
* Declarações JavaScript que definem a função, entre chaves { }.

````
function somarNumeros(numero1, numero2) {
    return numero1 + numero2;
}

// Exemplo de uso da função
let resultado = somarNumeros(5, 3);
console.log(resultado); // Saída: 8

````

## Estruturas de controle

No JavaScript, temos as seguintes estruturas condicionais:

* IF/Else: especificando um bloco de código para ser executado caso a condição seja verdadeira
```
if (condição) {
    // Bloco de código para ser executado.
}

 Exemplo:
if (x< 5) {
    mensagem = "É menor que 5";
}
```
```
if (x< 5) {
    mensagem = "É menor que 5";
} else {
    mensagem = "É maior que 5";
}
```
* Else if: especificar uma nova condição de teste caso a primeira seja falsa
````
if (condicao-1) {
    // Será executado este bloco caso a condição 1 seja verdadeira
} else if (condicao-1) {
    // Será executado este bloco caso a condição 1 seja falsa, e a 2 seja verdadeira
} else {
    // Será executado este bloco caso as condições 1 e 2 sejam falsas
}

Exemplo:
if (x< 5) {
    mensagem = "É menor que 5";
} else if (x > 5){
    mensagem = "É maior que 5";
} else {
   mensagem = "É igual a 5";
}

````
* Switch: especificar diversos blocos alternativos para serem executados
````
switch(expressao) {
    case n:
        // bloco de código
        break;
    case n:
        // bloco de código
        break;
    default:
        // bloco de block
}

No Switch, a expressão é testado uma única vez e logo após, comparado com as condições na estrutura. Quando o JavaScript interpreta a palavra break, ele simplesmente sai do bloco do switch. Isso pode salvar algum tempo de execução.
````
* For: Permite executar um bloco de código repetidamente enquanto uma condição específica for verdadeira.
```
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```
## Eventos e Manipulação do DOM

Eventos DOM (Document Object Model) são mecanismos do JavaScript que permitem aos desenvolvedores manipular e responder a eventos que ocorrem em elementos HTML. Esses eventos podem ser desde um clique do mouse até o envio de um formulário. Ao entender como os eventos DOM funcionam, os desenvolvedores podem criar interações dinâmicas e responsivas em suas páginas da web.

Como os eventos DOM funcionam?
Quando uma ação ocorre em um elemento HTML, como um botão sendo clicado, um evento é acionado. O JavaScript pode então detectar e responder a esse evento executando uma ação específica. Isso é feito através da associação de um manipulador de eventos a um elemento HTML específico.

Existem vários tipos de eventos DOM disponíveis para uso em JavaScript. Alguns dos mais comuns incluem:

* Eventos de clique: como “click”, acionados quando um elemento é clicado.
* Eventos de teclado: como “keydown” ou “keyup”, acionados quando uma tecla é pressionada ou liberada no teclado.
* Eventos de formulário: como “submit” ou “change”, acionados quando um formulário é submetido ou um campo de entrada é alterado.
* Eventos de mouse: como “mouseover” ou “mouseout”, acionados quando um mouse é movido sobre um elemento ou fora dele.

## Operadores 

### Operadores aritméticos 
Tomam valores numéricos (sejam literais ou variáveis) como seus operandos e retornam um único valor númerico. Os operadores aritméticos padrão são os de soma (+), subtração (-), multiplicação (*) e divisão (/). Estes operadores trabalham da mesma forma como na maioria das linguagens de programação quando utilizados com números de ponto flutuante (em particular, repare que divisão por zero produz um NaN (en-US)).

````
console.log(1 / 2); /* imprime 0.5 */
console.log(1 / 2 == 1.0 / 2.0); /* isto também é verdadeiro */

````
