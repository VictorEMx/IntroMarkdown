# RMarkdown Básico

<center style="color: green;font-size: 200%"> __Ediciones__ </center>

El tamaño del texto de los encabezados y la importancia estará definido por el número de # que coloquemos antes del texto

# 1. # Tamaño grande

### 2. ### Tamaño mediano

##### 3. ##### Tamaño menor

También es posible agregar negritas y cursivas

Negrita: Escribir el texto como ** **Negrita** ** o __ __Negrita__ __

Cursiva: Escribir el texto como * *Cursiva* * o _ _Cursiva_ _

<center style="color: green;font-size: 200%"> __Insertar imágenes__ </center>

![](tecnologico-de-monterrey-blue.png)

<center style="color: green;font-size: 200%"> __Ecuaciones__ </center>

#### Letras griegas y acentos matemáticos

Código: $\mu, \beta, \lambda, \sigma, \Sigma$

Código: $\tilde{S}, \overline{x}, \overline{X}, \hat{p}$

#### Subíndices, superíndices, comparaciones:

Código: $x_{i}$

Código: $x^{25}$

Código: $x_{i j}$

Código: $x^{2\cdot \alpha}, \tilde{S}^2,\sqrt{x}$

Código: $\mu=\mu_{0}$

Código: $3.141516\approx 3.14$

Código: $\mu\neq \mu_{0}$

Código: $\mu > \mu_{0}, \mu\geq \mu_{0}$

Código: $\mu < \mu_{0}, \mu\leq \mu_{0}$

#### Fracciones

Código: $\frac{\alpha}{2}$

Código: $z_{1-\frac{\alpha}{2}}, 8^{\frac{1}{3}}$

Código: $\frac{\tilde{S}}{\sqrt{n}}$

#### Paréntesis, corchetes y llaves:

Código: $(a,b); ]a,b[; \{a,b\}$

#### Ecuaciones complejas

Código: $f\left(k\right) = \binom{n}{k} p^k\left(1-p\right)^{n-k}$ 

<center style="color: green;font-size: 200%"> __Listas__ </center>

#### Lista 1

* Elemento
* Elemento
    + Subelemento
        - Desagregación
* Elemento

#### Lista 2

1) Elemento
2) Elemento
3) Elemento

<center style="color: green;font-size: 200%"> __Tablas__ </center>

```{r echo=FALSE}
knitr::kable(
  head(mtcars[, 1:8], 15), booktabs=TRUE,
  caption='Los primeros 15 renglones de nuestra base mtcars.')
```

<center style="color: green;font-size: 200%"> __Aplicación__ </center>

La base de datos `CARS2004` del paquete `PASWR2` recoge el número de coches por 1000 habitantes (`cars`), el número total de accidentes con víctimas mortales (`deaths`) y la población/1000 (`population`) para los 25 miembros de la Unión Europea en el año 2004.

1. Proporciona con `R` resumen de los datos. 
2. Utiliza la función `eda` del paquete `PASWR2` para realizar un análisis exploratorio de la variable `deaths`


#### Apartado 1

```{r message=FALSE, warning=FALSE, paged.print=FALSE}
library(PASWR2)
summary(CARS2004) 
```

Como puedes observar, al compilar tu documento aparecen las sentencias de `R` y el output que te da el programa.


#### Apartado 2

Ahora vamos a utilizar la función `eda` del paquete `PASWR2` para realizar un análisis exploratorio de la variable `deaths`

```{r}
eda(CARS2004$deaths)
```

En este caso, en tu documento final te aparece el código de `R`, el output numérico de la función `eda` y el output gráfico de la función `eda`.
