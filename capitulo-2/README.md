# Capítulo 2

## Sumario
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Capítulo 2](#capítulo-2)
  - [Sumario](#sumario)
  - [Lista de Arquivos no Diretório](#lista-de-arquivos-no-diretório)
  - [Biblioteca de Funções Sage](#biblioteca-de-funções-sage)
    - [Funções Básicas](#funções-básicas)
    - [Funções Aritméticas](#funções-aritméticas)

<!-- /code_chunk_output -->


O primeiro capítulo do livro [Elementos de Computação Matemática com SageMath](https://sagectu.com.br/) apresenta orintações sobre o software e seu uso. A codifição sendo iniciada no capítulo 2: __SageMath: Primeiros Passos__.

__Obs.:__ A execução dos códigos foi feita com sage 8.6, usando o debian 10.

---

## Lista de Arquivos no Diretório

* `01-inserindo-comandos.ipynb`: com o básico do uso do software, sintaxe de chamada à metodos, declaração de variáveis, operações básicas, etc.

    __Tabela de métodos Sage mencionados__

    Método   | Descrição          | Exemplo de Uso
    ---------|--------------------|---------------
    `matrix` | criação de Matrizes| `M = matrix([[1,2],[0,-1]])`
    `det`    | Determinante       | `det(M)`  ou `M.det()`
    `transpose`| Transposição de matriz | `transpose(M)`  ou `M.transpose()` ou `M.T`
    `solve`  | Solução de equações| `solve(x^2-5*x + 3,x)`  ou `(x^2-5*x + 3).solve(x)`
    `_`      | Chamada do resultado anterior | `_^2`
    `?`      | Descrição do método | `det?`

* `02-aproximacoes-numericas.ipynb`: com exemplos de constantes em Sage, aproximações numéricas e declaração de variáveis.

    Método   | Descrição          | Exemplo de Uso
    ---------|--------------------|---------------
    `n()`    | Aproximação numérica| `n(pi, digits=10)`
    `reset`  | Apaga as variáveis da memória| `reset()` 

* `03-variaveis-simbolicas.ipynb`: definições e usos de variáveis simbolícas.
    Método   | Descrição          | Exemplo de Uso
    ---------|--------------------|---------------
    `var`    | Criação de Variáveis Simbólicas | `y = var('y')`
    `assume` | Cria um intervalo de restrição para uma variável simbólica | `assume(x>-1, x<1, 'RR')`
    `assumptions` | Verifica as restrições assumides no uso de `assume` | `assumptions()`
    `forget` | Apaga os valores assumidos em restrições | `forget()`

* `04-funcoes-disponiveis.ipynb`: uso das funções matemáticas disponibilizadas junto com o Sage.

---

## Biblioteca de Funções Sage

O sage contém várias funções matemáticas predefinidas. A seguir é apresentado algumas lista de algumas delas: 

---

### Funções Básicas

Função      | Descrição                        | Sintaxe
------------|----------------------------------|---------------
<img src="https://latex.codecogs.com/svg.latex?\Large&space;\mid x \mid">| valor Absoluto de <img src="https://latex.codecogs.com/svg.latex?\Large&space;x">| `abs(x)`
<img src="https://latex.codecogs.com/svg.latex?\Large&space;\sqrt{x}"> | Raiz quadrada de <img src="https://latex.codecogs.com/svg.latex?\Large&space;x">| `sqrt(x)`
<img src="https://latex.codecogs.com/svg.latex?\Large&space;\sqrt[n]{x}"/> | Rai n-ésima de <img src="https://latex.codecogs.com/svg.latex?\Large&space;x"/> | `x^(1\n)`
<img src="https://latex.codecogs.com/svg.latex?\Large&space;\log_bx"/> | Logaritmo de <img src="https://latex.codecogs.com/svg.latex?\Large&space;x"/> na base <img src="https://latex.codecogs.com/svg.latex?\Large&space;b"/> | `log(x,b)`
<img src="https://latex.codecogs.com/svg.latex?\Large&space;e^x"/> | Exponencial de <img src="https://latex.codecogs.com/svg.latex?\Large&space;x"/> | `exp(x)` e `e^x`
<img src="https://latex.codecogs.com/svg.latex?\Large&space;\lceil x \rceil"/> | Menor inteiro maior ou igual a <img src="https://latex.codecogs.com/svg.latex?\Large&space; x"/> | `ceil(x)`
<img src="https://latex.codecogs.com/svg.latex?\Large&space;\lfloor x \rfloor"/> | Maior inteiro menor ou igual a <img src="https://latex.codecogs.com/svg.latex?\Large&space; x"/> | `floor(x)`
<img src="https://latex.codecogs.com/svg.latex?\Large&space;\max(x,y,\ldots)"/> | Valor máximo do conjunto <img src="https://latex.codecogs.com/svg.latex?\Large&space;\{x,y,\ldots\}"/> | `max(x,y,...)`
<img src="https://latex.codecogs.com/svg.latex?\Large&space;\min(x,y,\ldots)"/> | Valor mínimo do conjunto <img src="https://latex.codecogs.com/svg.latex?\Large&space;\{x,y,\ldots\}"/> | `min(x,y,...)`
<img src="https://latex.codecogs.com/svg.latex?\Large&space;\mbox{round}(x)"/> | Inteiro mais próximo ou igual a <img src="https://latex.codecogs.com/svg.latex?\Large&space; x"/> | `round(x)`
<img src="https://latex.codecogs.com/svg.latex?\Large&space;\mbox{int}(x)"/> | Parte inteira de <img src="https://latex.codecogs.com/svg.latex?\Large&space; x"/> | `int(x)`

---

### Funções Aritméticas

Sintaxe            | Descrição          
-------------------|-----------------------------------
`factorial(n)`     | Fatorial de n
`binomial(n,r)`    | Binomial de n sobre r
`factor(n)`        | Fatoração de n em primos
`is_prime(n)`      | Verifica se n é primo
`prime_range(i,j)` | Todos os primos entre i e j-1
`next_prime(n)`    | Primeiro primo depois de n
`gcd(i,j)`         | M.M.C de i e j
`lcm(i,j)`         | M.D.C de i e j
`randit(i,j)`      | Número aleatório entre i e j