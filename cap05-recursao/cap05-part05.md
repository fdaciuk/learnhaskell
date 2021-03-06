Pensando recursivamente
=======================

Já fizemos alguma coisa de recursão até agora e, como você provavelmente já notou, existe um padrão 
aqui. Normalmente você define uma condição limite e então você define uma função que faz alguma coisa 
com o primeiro elemento e reaplica no resto. Não importa se é uma lista, uma árvore ou qualquer outra 
estrutura de dados. Uma soma é o primeiro elemento de uma lista mais a soma do resto da lista. O produto 
de uma lista é o primeiro elemento da lista multiplicado pelo produto do resto da lista. O tamanho de 
uma lista é primeiro elemento mais o tamanho do resto da lista. E por ai vai.

E claro, falamos também das condições limite. Normalmente o caso limite é um cenário onde uma aplicação 
recursiva não faz sentido. Quando se trata de listas, a condição limite é na maioria das vezes uma 
lista vazia. Se você está lidando com árvores, o caso limite é normalmente um nodo que não tem filho algum. 
Coitado...

Não é diferente quando estamos lidando com números recursivamente. Um número faz algum cálculo com 
alguma modificação dele. Quando fizemos a função de fatorial, era o número multiplicado pelo fatorial (dele - 1). 
Nesse caso, tal aplicação recursiva não fazia sentido com zero, já que fatoriais estão definidos somente 
para inteiros positivos. Frequentemente os valores das condições limite acabam sendo sua identidade. 
A identidade da multiplicação é 1 porque se você multiplicar algum número por 1, você recebe de volta 
ele mesmo. Também ao fazer somas de listas, definimos a soma de uma lista vazia como 0 e 0 é a identidade 
da adição. No quicksort, o caso limite é a lista vazia e a identidade é também a lista vazia, porque se 
você adicionar uma lista vazia a uma lista, você apenas recebe de volta a lista original.

Então quando você tentar pensar de forma recursiva para resolver um problema, tente pensar em quando 
a solução recursiva não se aplica e tente ver se você pode usar isso como uma condição limite. Pense sobre 
identidades, se você vai dividir em partes os parâmetros da função (por exemplo, listas são normalmente 
divididas em primeiro elemento e resto, através de pattern matching) e em que parte você usará 
chamadas recursivas.
