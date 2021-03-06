Data.Set
========

O módulo [code]Data.Set[/code] nos oferece conjuntos. Conjuntos matemáticos, isso mesmo. 
Conjuntos são algo entre listas e mapas. Todos os elementos em um conjunto são únicos. E por serem 
internamente implementados por árvores (semelhantemente a mapas do [code]Data.Map[/code]), são 
ordenados. Checar existência, inserção, deleção, etc. é muito mais rápido do que com listas. As 
operações mais comuns falando-se de conjuntos é inserir, checar existência e converter para lista.

Pelos nomes do [code]Data.Set[/code] frequentemente conflitarem com membros de [code]Prelude[/code] e 
[code]Data.List[/code], fazemos uma importação qualificada.

Coloque essa linha no seu script:


E então carregue-o via GHCI.

Temos dois pedaços de um texto. Queremos descobrir quais caracteres são usados em ambos.


A função [function]fromList[/function] faz exatamente o que você imagina. Recebe uma lista e 
converte-a em um conjunto.



Como pode ver, os itens são ordenados e cada elemento são únicos. Usaremos 
[function]intersection[/function] para descobrir quais estão em ambos.



Podemos ainda usar [function]difference[/function] para ver quais letras estão no primeiro mas não 
no segundo conjunto e vice-versa.


Ou também podemos gerar um terceiro conjunto com as letras que aparecem em qualquer um dos dois 
primeiros usando [function]union[/function].



As funções [function]null[/function], [function]size[/function], [function]member[/function], 
[function]empty[/function], [function]singleton[/function], [function]insert[/function] e 
[function]delete[/function] você já deve imaginar para que servem.


Nós ainda podemos procurar por subconjuntos ou superconjuntos. O conjunto A é um subconjunto de 
B se B contém todos os elementos que A também tem. O conjunto A é um superconjunto de B se B contém 
todos os elementos de A e mais alguns.


Podemos ainda usar a [function]map[/function] e [function]filter[/function] para filtrá-los.



Conjuntos geralmente são usados para eliminar de uma lista valores duplicados transformando em 
[code]fromList[/code] e convertendo de volta para uma lista com [function]toList[/function]. 
A [code]Data.List[/code] [code]nub[/code] já faz isso, mas remover duplicados com listas grandes 
é muito mais rápido convertendo primeiro para um conjunto e depois convertendo de volta. Mas usar 
[code]nub[/code] requer que os tipos dos elementos da lista estejam na typeclass [code]Eq[/code], 
enquanto para converter a lista em um elemento, deve estar em [code]Ord[/code].



[code]setNub[/code] geralmente é mais rápido do que [code]nub[/code] em listas grandes, mas como pode 
ver, [code]nub[/code] preserva a ordem dos elementos, enquanto [code]setNub[/code] não.
