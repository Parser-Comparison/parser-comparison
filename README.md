## Грамматика
Для сравнения наших генераторов мы воспользовались следующей неоднозначной грамматикой:
```
S -> SSS | SS | a    # это a+
```
При таком описании во время парсинга возникает очень много неоднозначностей, на которые было интересно посмотреть и сравнить производительность парсеров


Ту же грамматику можно записать так:
```
S -> aS | a
```
Так неоднозначностей возникать не будет и выражение разбирается за ![equation](https://latex.codecogs.com/png.latex?%5Cbg_white%20%5Csmall%20%5Cmathcal%7BO%7D%28n%29)

## Используемые генераторы и их реализации
* [antlr4](https://github.com/alexbuyan/fl-2021-hse-win/tree/proj/antlr4) (Adaptive LL(*))
* [lark](https://github.com/alexbuyan/fl-2021-hse-win/tree/proj/lark) (Earley)
* [parglare](https://github.com/alexbuyan/fl-2021-hse-win/tree/proj/parglare) (GLR)
* [yacc](https://github.com/alexbuyan/fl-2021-hse-win/blob/proj/yacc/) (LALR(1))

Подробнее про работу каждого из генераторов можно почитать по соответствующей ссылке.

Для написания генераторов мы использовали Python3, но также понадобилась Java (для визуализации деревьев в ANTLR)

## Основные выводы
TODO