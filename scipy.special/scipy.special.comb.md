# scipy.special.comb

### `scipy.special.comb(N, k, exact=False, repetition=False)`

O número de combinações de N coisas, sendo elas consideradas um número k por vez

Essa fórmula é comumente expressa pela frase "N k a k"

#### Parâmetros

**N: *int, ndarray***

Número de coisas sendo combinadas

**k: *int, ndarray***

Número de elementos selecionados

**exact: *bool, opcional***

Se o parâmetro *exact* for Falso, o resultado é retornado com precisão de ponto flutuante, caso contrário um inteiro longo é computado

**repetition: *bool, opcional***

Se o parâmetro repetition for Verdadeiro, então o número de combinações com repetições é considerado no cálculo da função

#### Retornos

**val: *int, float, ndarray***

O número total de combinações

### Observações

---

- Vetores (arrays) só podem ser usados como argumentos na função se o parâmetro `exact=False`.

- Se N < 0 ou k < 0, o retorno será 0.

- Se k > N e o parâmetro `repetition=False`, o retorno será 0.

### Exemplos

---

```python
>>> from scipy.special import comb

>>> k = np.array([3, 4])

>>> n = np.array([10, 10])

>>> comb(n, k, exact=False)

array([120., 210.])

>>> comb(10, 3, exact=True)

120

>>> comb(10, 3, exact=True, repetition=True)

220
```


