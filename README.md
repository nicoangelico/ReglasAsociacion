# Reglas de Asociacion
Aplicación académica de Reglas de Asociación (UTN FRRe).


Consulte wikipedia para saber que es y como funciona esta tecnica de inteligencia artifical.
https://es.wikipedia.org/wiki/Reglas_de_asociaci%C3%B3n

# La aplicación
Para correr el algoritmo se requiere un **Soporte mínimo**, una **Confianza mínima** y un conjunto de transacciones. En este ejemplo colocamos el soporte en 0.3 y la confianza en 0.7 y a continuación ingresamos las siguientes transacciones:

B,I,M;

B,C;

C,O;

B,I,C,O;

B,I,L,C,M;

I,L,M;

I,M,L;

C,M,I,L,O;

M,L,B;

B,O,M;


# Resultados
Corremos el aplicativo y nos devuelve el siguiente resultado:

[C]->[B] confianza: 0.6    Descarto

[B]->[C] confianza: 0.5    Descarto

[I]->[B] confianza: 0.5    Descarto

[B]->[I] confianza: 0.5    Descarto

[M]->[B] confianza: 0.57    Descarto

[B]->[M] confianza: 0.67    Descarto

[I]->[C] confianza: 0.5    Descarto

[C]->[I] confianza: 0.6    Descarto

[O]->[C] confianza: 0.75

[C]->[O] confianza: 0.6    Descarto

[L]->[I] confianza: 0.8

[I]->[L] confianza: 0.67    Descarto

[M]->[I] confianza: 0.71

[I]->[M] confianza: 0.83

[M]->[L] confianza: 0.71

[L]->[M] confianza: 1.0

[L, M]->[I] confianza: 0.8

[I, M]->[L] confianza: 0.8

[I, L]->[M] confianza: 1.0

[M]->[I, L] confianza: 0.57    Descarto

[I]->[L, M] confianza: 0.67    Descarto

[L]->[I, M] confianza: 0.8

