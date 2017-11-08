# Reglas de Asociacion / Association rule learning
En minería de datos y aprendizaje automático, las reglas de asociación se utilizan para descubrir hechos que ocurren en común dentro de un determinado conjunto de datos.

Consulte wikipedia.
https://es.wikipedia.org/wiki/Reglas_de_asociaci%C3%B3n

# La aplicación
Esta es una aplicación académica cuyo fin es resolver problemas simples y arrojar todo el proceso de que ha realizado a fin de comprender el funcionamiento de esta técnica de IA. Para correr el algoritmo se requiere un **Soporte mínimo**, una **Confianza mínima** y un conjunto de transacciones. En este ejemplo colocamos el soporte en 0.3 y la confianza en 0.8 y a continuación ingresamos las siguientes transacciones:

Beef,Chicken,Milk;

Beef,Cheese;

Cheese,Boots;

Beef,Chicken,Cheese;

Beef,Chicken,Clothes,Cheese,Milk;

Chicken,Clothes,Milk;

Chicken,Milk,Clothes;

# Resultados
Corremos el aplicativo y nos devuelve el siguiente resultado:

[Cheese]->[Beef] confianza: 0.75    Descarto

[Beef]->[Cheese] confianza: 0.75    Descarto

[Chicken]->[Beef] confianza: 0.6    Descarto

[Beef]->[Chicken] confianza: 0.75    Descarto

[Clothes]->[Chicken] confianza: 1.0

[Chicken]->[Clothes] confianza: 0.6    Descarto

[Milk]->[Chicken] confianza: 1.0

[Chicken]->[Milk] confianza: 0.8

[Milk]->[Clothes] confianza: 0.75    Descarto

[Clothes]->[Milk] confianza: 1.0

[Clothes, Milk]->[Chicken] confianza: 1.0

[Chicken, Milk]->[Clothes] confianza: 0.75    Descarto

[Chicken, Clothes]->[Milk] confianza: 1.0

[Milk]->[Chicken, Clothes] confianza: 0.75    Descarto

[Chicken]->[Clothes, Milk] confianza: 0.6    Descarto

[Clothes]->[Chicken, Milk] confianza: 1.0
