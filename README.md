## Tarea 2

**Entrega: Miércoles 22 de marzo de 2023**

*La tarea podrá realizarse en equipos de máximo 3 integrantes*

### Instrucciones

1. (2 pts.) Dada la siguiente información, define los hechos, reglas y consultas necesarias para encontrar las 3 tuplas `(Nombre, Prenda, Color, Descuento)` que resuelven el acertijo:

    Curry, Kleene y Russell fieron de compras durante el Buen Fin para aprovechar las rebajas. Cada uno compró un artículo y tuvo su debido descuento. Los artículos que compraron son una chamarra, un pantalón y una sombrilla; y encontraron descuentos del 10%, 25% y hasta 50% con meses sin intereses. Tenemos las siguientes pistas:
    
    1. La chamarra azul no la compró Curry.
    2. Russell estuvo alegre de encontrar un 25% de descuento en el producto que compró.
    3. El producto rojo tuvo un mayor descuento que la sombrilla.
    4. Los pantalones no tuvieron el descuento del 10% y no los compraron ni Curry ni Kleene.

2. (2 pts.) Define el predicado `particion(L1, L2, L3)` que se satisface cuando `L2` es la primera mitad de la lista `L1`, y `L3` es la segunda mitad de `L1`. Si el número de elementos es impar, una lista puede quedar más grande que la otra por un elemento.

    ```prolog
    ?- particion([1, 2, 3, 4, 5, 6], X, Y).
      X = [1, 2, 3], Y = [4, 5, 6].
      
    ?- particion([1, 2, 3, 4, 5], X, Y).
      X = [1, 2], Y = [3, 4, 5].
    ```

3. (2 pts.) Define el predicado `combina(L1, L2, L3)` que se satisface cuando dadas dos listas `L1` y `L2` ordenadas de forma ascendente, `L3` es la lista ordenada con los elementos de las primeras dos.

    ```prolog
    ?- combina([2, 4, 6], [1, 3, 5, 7], L).
      L = [1, 2, 3, 4, 5, 6, 7].
    ```

4. (2 pts.) Define el predicado `gcd(X, Y, Z)` que se satisface cuando `Z` es el máximo común divisor de `X` y `Y`. Además, define `coprimos(X, Y)` que decide si `X` y `Y` son primos relativos.

    ```prolog
    ?- gcd(13, 19, X).
      X = 1.

    ?- gcd(24, 18, X).
      X = 6.
    ```

5. (2 pts.) Define operadores que correspondan a los conectivos de la lógica proposicional:
   - Negación (`neg`)
   - Disyunción (`or`)
   - Conjunción (`and`)
   - Implicación (`impl`)
   
   Las definiciones deben reflejar la jerarquía y asociatividad de la lógica proposicional.
   
   ```prolog
   ?- Formula = p and neg neg q.
      Formula = p and neg neg q.

   ?- Formula = (neg (neg p)) or q.
      Formula = (neg (neg p)) or q.

   ?- Formula = neg neg p.
      Formula = neg neg p.
   ```

**Punto extra:** (1/2 punto por cada uno).
- Define un predicado `dl` que convierta una lista abierta en una lista normal, y viceversa.
- Define el predicado `ordenar(L1, L2)` que se satisface cuando `L2` es la lista `L1` ordenada (se recomienda hacer el algoritmo `merge sort`).
- Define el predicado `evaluacion(P)` que dada una fórmula `P` escrita con los operadores del ejercicio 5 y átomos `verdad` y `falso` (sin variables proposicionales) regrese `true` cuando se satisface y `false` cuando no.

### Restricciones

- La hora máxima de entrega será a las **23:59:59** de la fecha indicada al inicio de este documento.

- Para poder pedir una prórroga sobre la entrega es requisito **indispensable** que todos los equipos de estudiantes
  hagan cambios (*commit*) constantes a su repositorio a lo largo del periodo de realización de la tarea.

- **Todas las copias serán calificadas automáticamente con cero**.

### Material de consulta

- The Power of Prolog (Guía de Prolog) [https://www.metalevel.at/prolog](https://www.metalevel.at/prolog)
- Logic Puzzles [https://www.ahapuzzles.com/logic/logic-puzzles/](https://www.ahapuzzles.com/logic/logic-puzzles/)
- SWI Prolog -- Manual: Operators [https://www.swi-prolog.org/pldoc/man?section=operators](https://www.swi-prolog.org/pldoc/man?section=operators)
- Notas del Curso [https://lambdaspace.gitlab.io/cursos/unam/pd/material/](https://lambdaspace.gitlab.io/cursos/unam/pd/material/)
