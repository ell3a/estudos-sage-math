# Códigos do Capítulo 2

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

* `03-variaveis-simbolicas.ipynb`: