# Pooled testing of subsamples identified by tuples

L. Mutesa et at., A strategy for finding people infected with
SARS-CoV-2: optimizing pooled testing at low prevalence,
<https://doi.org/10.1101/2020.05.02.20087924>, 2020-08-03.

## Task

To test samples from *n* individuals, at a low prevalence *p*, in the
shortest possible time without extra test equipment.

## Strategy

1.  <span class="english"> <span class="underline">Group testing
    phase</span> </span>
    
    Divide the *n* samples into *g* groups of size *N*, with *N* chosen
    as the power of 3 (value for which the number of tests per person is
    minimum) closest to <sup>0.35</sup>⁄<sub>*p*</sub>. Test each group:
    perform *g* tests, each with a pool of *N* subsamples.
    
    A new estimate of the prevalence can be made once the fraction *f*
    of groups that tested negative is known: *p* = 1 −
    *f*<sup>1/*N*</sup>. If the new estimate differs significantly from
    the original one, another value for *N* may then be chosen for the
    next phase.

2.  <span class="english"> <span class="underline">Slicing tests phase -
    First round</span> </span>
    
    Perform a first round of slicing tests on the groups that tested
    positive in the first phase.
    
    For each group of *N* individuals, take *D* subsamples from each
    individual sample, and pool (or combine)
    <sup>*N*</sup>⁄<sub>*L*</sub> subsamples for each of *T* = *D* \*
    *L* tests. Assign individuals to tests in a way that allows
    associating an individual with a certain set of tests.
    
    To associate an individual with a certain set of tests, a *D*-tuple
    of digits is assigned to each individual, each digit taking a value
    from a number *L* of values. Each *D*-tuple corresponds to the
    coordinate of a point in a hypercube of *D* dimensions, with *L*
    points on each side. Each test corresponds to a slice of the
    hypercube, composed of those individuals that have the same
    coordinate in a given direction.
    
    The *D*-tuple that identifies an individual may be also treated as a
    *D*-digit number in a base-*L* numeral system. Each of the *L*
    values of each of the *D* digits corresponds to a test; from this it
    follows that *D* \* *L* is the number of tests to perform for the
    *N* individuals.
    
    Now, a simple example, using *L* = 10 (not the optimum value).
    Assume there are *N* = 100 individuals to test, because it is
    estimated that *p* = 0.0035. We number the individuals from 0 to 99.
    *D* = 2, because 10<sup>2</sup> = 100. We then have to perform *D*
    \* *L* = 2 \* 10 = 20 tests, each with <sup>*N*</sup>⁄<sub>*L*</sub>
    = <sup>*100*</sup>⁄<sub>*10*</sub> = 10 subsamples. We assign each
    test to a digit: one test corresponds to 0 in ones place, another
    test to 0 in tens place, etc. For the test that corresponds to 0 in
    ones place, we pool the 10 subsamples from those individuals
    identified with numbers ending in 0, i.e. 0, 10, 20,…, 90. For the
    test that corresponds to 3 in tens place, we pool the 10 subsamples
    from those individuals identified with numbers having a 3 in tens
    place: 30, 31,…, 39. And similarly for the other eighteen tests. If
    an individual is infected, the positive tests will be those
    corresponding to the identification number; for example, if only the
    tests that correspond to 5 in ones place and 1 in tens place are
    positive, we know that the individual with number 15 (and only him
    or her) is infected. All 20 tests can be performed simultaneously.
    We save the cost of 80 tests. By using *L* = 3 —the optimum value—
    the savings are greater still: only 15 tests are needed to identify
    the infected individual.

3.  <span class="english"> <span class="underline">Slicing tests phase -
    Steps to take after the first round</span> </span>
    
    If there is only one positive slice in each direction, there is only
    one infected individual, that is immediately identified.
    
    If there is only one direction in which several slices are positive,
    all infected individuals are immediately identified.
    
    If there are several directions in which several slices are
    positive, those individuals identified with slices that tested
    positive are included in a second round of slicing tests. In the
    example above, if the positive tests correspond to 2 and 7 in ones
    place and 4, 6 and 9 in tens place —a very low probability case
    given the estimated prevalence— between three and six individuals
    are infected among those identified with numbers 42, 47, 62, 67, 92
    and 97.

## This file

<span class="english"> </span>

This page was written to help prepare slicing tests and interpret their
results, numbering both tests and individuals with positive integers in
the decimal system.

The user can enter, below, either the value of *p*, letting the system
determine the optimum values for *N*, *D* and *L*, or the value of one
(or two) of these variables, obtaining the other(s).

The *Preparation* tabs show, for the values entered, which subsamples
are to be combined for a given test, and which tests must contain a
subsample from a given individual.

The *Results* tab shows, given the results from the tests, which
individuals are infected (if any) or which individuals should be
included in an additional round of testing.
# Análisis con mezcla de submuestras identificadas por tuplas

L. Mutesa et at., A strategy for finding people infected with
SARS-CoV-2: optimizing pooled testing at low prevalence,
<https://doi.org/10.1101/2020.05.02.20087924>, 2020-08-03.

## Tarea

Analizar muestras de *n* individuos, cuando la prevalencia *p* es baja,
en el menor tiempo posible sin recurrir a instrumentos de diagnóstico
adicionales.

## Estrategia

1.  <span class="spanish"> <span class="underline">Fase de análisis por
    grupos</span> </span>
    
    Dividir las *n* muestras en *g* grupos de *N* muestras cada uno, con
    *N* igual a la potencia de 3 (valor de *L* que minimiza la cantidad
    de análisis por individuo) más cercana a
    <sup>0.35</sup>⁄<sub>*p*</sub>. Hacer un análisis por cada grupo,
    es decir *g* análisis con *N* submuestras mezcladas en cada uno.
    
    Se puede además, ya que se conoce la fracción *f* de grupos
    negativos, mejorar la estimación de la prevalencia: *p* = 1 −
    *f*<sup>1/*N*</sup>. Si el valor de *p* así estimado es muy distinto
    de la estimación inicial, se puede elegir otro valor de *N* para la
    siguiente fase.

2.  <span class="spanish"> <span class="underline">Fase de análisis por
    tajadas - Primera ronda</span> </span>
    
    Pasar los grupos que en la primera fase resultaron positivos, a una
    primera ronda de análisis por tajadas.
    
    Para cada grupo de *N* individuos, tomar *D* submuestras de cada
    muestra correspondiente a un individuo, y mezclar
    <sup>*N*</sup>⁄<sub>*L*</sub> submuestras en cada uno de *T* = *D*
    \* *L* análisis. Asignar los individuos a los análisis de modo que a
    cada individuo le corresponda un conjunto de análisis distinto.
    
    Esto último se hace asignando a cada individuo una *D*-tupla de
    dígitos, cada uno de un valor tomado de entre *L* valores. La
    *D*-tupla corresponde a la coordenada de un punto en un hipercubo de
    *D* dimensiones, con *L* puntos en cada dirección. En cada análisis
    va una tajada del hipercubo, formada por los individuos que
    comparten una misma coordenada en determinada dirección.
    
    La *D*-tupla que identifica a un individuo se puede intrepretar
    también como un número en un sistema de numeración en base *L*. Cada
    uno de los *L* valores de cada uno de los *D* dígitos, corresponde a
    un análisis; de ahí que haya *D* \* *L* análisis para los *N*
    individuos.
    
    Ahora, un ejemplo sencillo usando *L* = 10 (valor no óptimo).
    Supongamos que hay que analizar *N* = 100 individuos ya que se
    estima *p* = 0.0035. Numeramos los individuos del 0 al 99. *D* = 2
    ya que 10<sup>2</sup> = 100. Luego hacemos *D* \* *L* = 2 \* 10 = 20
    análisis,cada uno con <sup>*N*</sup>⁄<sub>*L*</sub> =
    <sup>*100*</sup>⁄<sub>*10*</sub> = 10 submuestras. Hacemos
    corresponder cada análisis a un dígito: un análisis para el 0 de las
    unidades, otro para el 0 de las decenas, etc. En el análisis
    correspondiente al dígito 0 de las unidades, mezclamos las 10
    submuestras de los individuos identificados con números terminados
    en 0, es decir 0, 10, 20,…, 90. En el análisis correspondiente al
    dígito 3 de las decenas, mezclamos las 10 submuestras de los
    individuos identificados con números que tienen 3 en esa posición:
    30, 31,…, 39. Y así para los restantes dieciocho análisis. Si hay un
    individuo infectado, resultarán positivos los análisis que lo
    identifican; por ejemplo, si solamente resultan positivos los
    análisis correspondientes al 5 de las unidades y al 1 de las
    decenas, sabemos que el individuo identificado con el número 15 (y
    sólo él) está infectado. Los 20 análisis se pueden hacer a la vez.
    Ahorramos 80 anñalisis. Usando *L* = 3 —valor óptimo—, el ahorro es
    todavía mayor: bastan 15 análisis para identificar el individuo
    infectado.

3.  <span class="spanish"> <span class="underline">Fase de análisis por
    tajadas - Pasos a seguir luego de la primera ronda</span> </span>
    
    Si sólo hay una tajada positiva en cada dirección, hay sólo un
    individuo infectado, que se identifica inmediatamente.
    
    Si sólo en una dirección hay más de una tajada positiva, se
    identifica inmediatamente a los individuos infectados.
    
    Si hay más de una dirección con más de una tajada positiva, se pasan
    a una segunda ronda de análisis los individuos identificados por
    tajadas que resultaron positivas. En el ejemplo de arriba, si los
    análisis correspondientes a los dígitos 2 y 7 de las unidades y 4,
    6 y 9 de las decenas resultaron positivos —caso muy poco probable
    para la prevalencia estimada—, pueden estar infectados entre tres y
    seis de los individuos identificados con los números 42, 47, 62, 67,
    92 y 97.

## Este archivo

<span class="spanish"> </span>

Esta página se hizo para poder preparar análisis por tajadas, e
interpretar sus resultados, cuando se usan números naturales en el
sistema decimal tanto para los análisis como para los individuos.

Más abajo el usuario puede ingresar el valor de *p* y obtener los
valores óptimos de *N*, *D* y *L*, o bien ingresar el valor de una (o
dos) de estas variables y obtener el resto.

En las pestañas de *Preparación* de análisis, se informa, para los
valores ingresados, cuáles submuestras debe contener un análisis
determinado, y en cuáles análisis deben ir submuestras de determinado
individuo.

En la pestaña de *Resultados*, se informa, dados los resultados de los
análisis, cuáles individuos están infectados o cuáles individuos pasan a
una ronda adicional de análisis.
