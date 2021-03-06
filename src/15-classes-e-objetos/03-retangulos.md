## 15.3 - Retângulos

Às vezes, é óbvio quais deveriam ser os atributos de um objeto, mas outras é preciso decidir entre as possibilidades. Por exemplo, vamos supor que você esteja criando uma [classe](08-glossario.md#classe) para representar retângulos. Que atributos usaria para especificar a posição e o tamanho de um retângulo? Você pode ignorar ângulo; para manter as coisas simples, suponha que o retângulo seja vertical ou horizontal.

Há duas possibilidades, no mínimo:

* Você pode especificar um canto do retângulo (ou o centro), a largura e a altura.

* Você pode especificar dois cantos opostos.

Nesse ponto é difícil dizer qual opção é melhor, então implementaremos a primeira, como exemplo.

Aqui está a definição de classe:

```python
class Rectangle:
    """Represents a rectangle.
    attributes: width, height, corner.
    """
```

A docstring lista os atributos: width e height são números; corner é um objeto `Point` que especifica o canto inferior esquerdo.

Para representar um retângulo, você tem que [instanciar](08-glossario.md#instanciar) um objeto `Rectangle` e atribuir valores aos atributos:

```python
box = Rectangle()
box.width = 100.0
box.height = 200.0
box.corner = Point()
box.corner.x = 0.0
box.corner.y = 0.0
```

A expressão `box.corner.x` significa “Vá ao objeto ao qual `box` se refere e pegue o [atributo](08-glossario.md#atributo) denominado `corner`; então vá a este objeto e pegue o atributo denominado `x`”.

A Figura 15.2 mostra o estado deste objeto. Um objeto que é um atributo de outro objeto é integrado.

A Figura 10.1 mostra o diagrama de estado para cheeses, numbers e empty.

![Figura 15.2 – Diagrama de um objeto Rectangle](/fig/tnkp_1502.png).
<br>_Figura 15.2 – Diagrama de um objeto_ `Rectangle`.

