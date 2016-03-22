# Cálculos

Estos son los calculos que se utilizan en el sketch para convertir los valores analógicos de los sensores.


### Alcohol

![Alcohol](alcohol.png)

**Puntos de la curva**

Rs/Ro | mg/L
------------ | -------------
0,1333 | 10
0,16666 | 8
0,17 | 6
0,18 | 4
0,19 | 2,5
0,2 | 1,8
0,23 | 1,4
0,6 | 0,9
0,7 | 0,7
0,8 | 0,6
0,9 | 0,5
1 | 0,4
1,66666 | 0,21
1,24 | 0,1

**Ecuación potencial**

- Expresión:
```
y = 0,337x-1,45 
```
- Código:
```arduino
double Alcohol = 0.337*pow(mq3_resistencia/5463, -1.45);
```


### Gases Licuados del Petróleo (GLP)

![Alcohol](glp.png)

**Puntos de la curva**

Rs/Ro | ppm
------------ | -------------
0,75 | 10000
0,9 | 5000
1,7 | 1000
2,7 | 200


**Ecuación potencial**

- Expresión:
```
y = 4102x-2,95 
```
- Código:
```arduino
double glp = 4102*pow(mq2_resistencia/5463, -2,95);
```


### Metano

### Propano

### Monóxido de Carbono

### Hidrógeno

### Dióxido de Carbono

### Óxidos de Nitrógeno

### Amoniaco