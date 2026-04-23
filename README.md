# Practica3GD
## Docente
Dr. Paul Antonio Valle Trujillo; paul.valle@tectijuana.edu.mx

Departamento de Ingeniería Eléctrica y Electrónica, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana, C.P. 22454, B.C., México.

## Descripción de la asignatura
La asignatura de Gemelos Digitales forma parte del plan de estudios de la carrera en Ingeniería Biomédica con la siguiente competencia general del curso: Formula el gemelo digital a través de datos experimentales para el desarrollo estrategias de control mediante teorías de sistemas dinámicos no lineales y la experimentación in silico. Esta asignatura pretende aportar al perfil del Ingeniero Biomédico la capacidad de realizar investigación científica en el área de Biología de Sistemas con la finalidad de dirigir y participar en equipos de trabajo interdisciplinarios en contextos nacionales e internacionales, así como de proporcionar soluciones informáticas para resolver problemas en el campo de la Ingeniería Biomédica con ética profesional.

En el contexto de sistemas dinámicos que describen sistemas biológicos o fisiológicos, el modelizado in silico es una extensión lógica de la experimentación in vitro controlada, es el resultado natural del gran aumento de la potencia computacional disponible a un costo que disminuye continuamente, combinando las ventajas de la experimentación in vivo e in vitro, sin someterse a las consideraciones éticas y la falta de control asociadas con los experimentos in vivo. A diferencia de los experimentos in vitro, que existen de forma aislada, los modelos in silico permiten incluir un conjunto prácticamente ilimitado de variables y parámetros, lo que hace que los resultados sean más aplicables en problemas del mundo real. La experimentación in silico ha dado lugar al paradigma denominado como "gemelos digitales" (en inglés digital twins); en esencia, los gemelos digitales son una réplica o representación digital de un proceso o sistema del mundo real, donde por replica se refiere a un modelo computacional desarrollado con base en datos experimentales y características especiales que le permiten conectar lo físico con lo virtual con el propósito de mejorar el rendimiento de un sistema, detectar y prevenir fallas, y realizar predicciones sobre su respuesta ante diferentes estímulos o escenarios de operación; una definición más formal establece que: un gemelo digital es un conjunto de modelos adaptativos que emulan el comportamiento de un sistema físico en un sistema virtual obteniendo datos en tiempo real para actualizarse a lo largo de su ciclo de vida; replica al sistema físico para predecir fallas y oportunidades de cambio, prescribir acciones en tiempo real para optimizar y/o mitigar eventos inesperados observando y evaluando el perfil operativo del sistema. En el campo particular de la Biología de Sistemas, un gemelo digital se presenta como un algoritmo o conjunto de algoritmos computacionales desarrollados con base en modelos mecanicistas de un organismo vivo, esto con el objetivo de emular su fisiología para ilustrar su dinámica en el corto y en el largo plazo, así como predecir su respuesta a diferentes estímulos endógenos y exógenos.

## Objetivo y descripción del sistema
Determinar la tasa de liberación del hidrogel N36 2MBA3 (y las demás formulaciones como N32, N35-VP15 y N45-2MBA12) con base en los datos experimentales de concentración liberada a lo largo del tiempo.

La liberación de fármacos desde matrices poliméricas (como los hidrogeles) es un proceso dinámico de transporte de masa que puede ser analizado y caracterizado mediante diversos modelos matemáticos. En esta práctica, se utilizan técnicas de regresión no lineal y experimentación in silico para ajustar perfiles experimentales de liberación acumulada de fármaco (%) en función del tiempo (min) evaluando los siguientes modelos:

1. **Modelo de Korsmeyer-Peppas**: $x(t) = k \cdot t^n$
2. **Farmacocinética de primer orden**: $x(t) = \beta(1 - e^{-kt})$
3. **Modelo de ecuaciones empíricas (Eureqa)**: $x(t) = \rho_1 \sqrt{t} - \rho_2 t$
4. **Modelo mecanicista basado en Ecuaciones Diferenciales Ordinarias (EDO)**: $\frac{dx_1}{dt} = \rho_1  - \rho_2 x_1$

Para la resolución del sistema basado en EDOs se utilizan métodos de integración numérica, como el Método de Heun, acoplados al algoritmo de estimación de parámetros para encontrar los valores óptimos. Finalmente, se extraen bioestadísticos de bondad de ajuste, tales como intervalos de confianza, Criterio de Información de Akaike ajustado (AICc) y R-cuadrada.

Palabras clave: Liberación Controlada; Hidrogeles; Regresión No Lineal; Farmacocinética; Ecuaciones Diferenciales Ordinarias; Bioestadística.

## Actividades a realizar
1. Importar y procesar datos experimentales de liberación de fármacos estructurados en tablas de datos.
2. Desarrollar rutinas en MATLAB para ajustar modelos farmacocinéticos empíricos mediante regresión no lineal.
3. Integrar numéricamente Ecuaciones Diferenciales Ordinarias utilizando el Método de Heun acoplado a funciones de minimización de error.
4. Evaluar la certidumbre estadística de cada modelo calculando valores t-student, margen de error e intervalos de confianza (CI95).
5. Graficar y exportar de forma vectorial las curvas predichas contra los datos experimentales en múltiples paneles.

## Lista de archivos incluidos en el repositorio
1. Cuaderno computacional de MATLAB (Script principal) [.mlx].
2. Funciones integradas para modelado (e.g. `peppas.m`, `farmacocinetica.m`, `biostats.m`) [.m].
3. Base de datos con resultados experimentales de hidrogeles (`data.csv`).
4. Imágenes exportadas de los modelos paramétricos y estadísticos [.pdf].

## Referencias
\[1] P. A. Valle, Syllabus para Gemelos Digitales, Tecnológico Nacional de México / Instituto Tecnológico de Tijuana, Tijuana, B.C., México, 2025. Permalink: https://biomath.xyz/course/

\[2] Peppas, N. A. (1985). Analysis of Fickian and non-Fickian drug release from polymers. Pharmaceutica Acta Helvetiae, 60(4), 110-111.
