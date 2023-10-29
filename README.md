# Calculadora de Partidas Rankeadas

Este projeto consiste em uma função que determina o nível de um jogador com base em suas vitórias e derrotas.

## Como Funciona

1. **Definição da Função**:
```javascript
function calculadoraRankeadas(vitorias, derrotas) {
```
Aqui, definimos uma função chamada `calculadoraRankeadas` que aceita dois parâmetros: `vitorias` e `derrotas`.

2. **Cálculo do Saldo de Vitórias**:
```javascript
let saldoVitorias = vitorias - derrotas;
```
Dentro da função, calculamos o saldo de vitórias subtraindo as derrotas das vitórias e armazenamos o resultado na variável `saldoVitorias`.

3. **Determinação do Nível**:
Inicializamos uma variável chamada `nivel` para armazenar o nível do jogador.
```javascript
let nivel = "";
```

Em seguida, usamos uma série de estruturas de decisão `if-else` para determinar o nível do jogador com base no saldo de vitórias:

```javascript
if (saldoVitorias < 10) {
    nivel = "Ferro";
} else if (saldoVitorias >= 11 && saldoVitorias <= 20) {
    nivel = "Bronze";
} ...
```
Cada condição verifica um intervalo específico de saldo de vitórias e atribui o nível correspondente à variável `nivel`.

4. **Retorno da Mensagem**:
Após determinar o nível, a função retorna uma mensagem formatada com o saldo de vitórias e o nível:
```javascript
return `O Herói tem um saldo de ${saldoVitorias} e está no nível de ${nivel}`;
```
Usamos uma template string (indicada pelas crases) para inserir as variáveis `saldoVitorias` e `nivel` diretamente na mensagem.

5. **Exemplo de Uso**:
No final do código, temos um exemplo de como usar a função:
```javascript
let resultado = calculadoraRankeadas(85, 10);
console.log(resultado);
```
Neste exemplo, chamamos a função `calculadoraRankeadas` com 85 vitórias e 10 derrotas. O resultado é armazenado na variável `resultado` e, em seguida, exibido no console.
