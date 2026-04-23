# Práctica: Liberación controlada de fármacos por hidrogeles
 
## Información de la estudiante
Paul A. Valle \[05211261]; paul.vt@tijuana.tecn.mx
 
Gemelos Digitales
 
Ingeniería Biomédica
 
## Docente
Dr. Paul Antonio Valle Trujillo; paul.valle@tectijuana.edu.mx
 
Departamento de Ingeniería Eléctrica y Electrónica, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana, C.P. 22454, B.C., México.
 
## Descripción de la asignatura
La asignatura de Gemelos Digitales forma parte del plan de estudios de la carrera en Ingeniería Biomédica con la siguiente competencia general del curso: Formula el gemelo digital a través de datos experimentales para el desarrollo estrategias de control mediante teorías de sistemas dinámicos no lineales y la experimentación in silico. Esta asignatura pretende aportar al perfil del Ingeniero Biomédico la capacidad de realizar investigación científica en el área de Biología de Sistemas con la finalidad de dirigir y participar en equipos de trabajo interdisciplinarios en contextos nacionales e internacionales, así como de proporcionar soluciones informáticas para resolver problemas en el campo de la Ingeniería Biomédica con ética profesional.
 
En el contexto de sistemas dinámicos que describen sistemas biológicos o fisiológicos, el modelizado in silico es una extensión lógica de la experimentación in vitro controlada, es el resultado natural del gran aumento de la potencia computacional disponible a un costo que disminuye continuamente, combinando las ventajas de la experimentación in vivo e in vitro, sin someterse a las consideraciones éticas y la falta de control asociadas con los experimentos in vivo. A diferencia de los experimentos in vitro, que existen de forma aislada, los modelos in silico permiten incluir un conjunto prácticamente ilimitado de variables y parámetros, lo que hace que los resultados sean más aplicables en problemas del mundo real.
 
## Objetivo y descripción del sistema
Determinar la tasa de liberación del hidrogel N36-2MBA3 con base en datos experimentales mediante regresión no lineal, ajustando los siguientes modelos matemáticos:
 
**Ecuación de Peppas:**
 
$$x(t) = k t^n$$
 
**Farmacocinética de primer orden:**
 
$$x(t) = \beta(1 - e^{-kt})$$
 
**Eureqa: Función del tiempo:**
 
$$x(t) = \rho_1 \sqrt{t} - \rho_2\, t$$
 
**EureqaODE: Farmacocinética de primer orden:**
 
$$\frac{\mathrm{d}x}{\mathrm{d}t} = \rho_1 - \rho_2\, x$$
 
Los datos experimentales corresponden a cuatro hidrogeles de PNVCL-PEGMA con temperatura de transición ajustable para la liberación controlada de 5-fluorouracilo: N45-2MBA12, N32, N35-VP15 y N36-2MBA3, medidos en porcentaje de liberación acumulativa de fármaco a lo largo del tiempo (minutos).
 
Palabras clave: Regresión No Lineal; Bioestadísticos; Farmacocinética; Ecuación de Peppas; Gemelos Digitales; Experimentación in silico.
 
## Actividades a realizar
1. Cargar y visualizar los datos experimentales de los cuatro hidrogeles desde el archivo `data.csv`.
2. Ajustar la **Ecuación de Peppas** ($x(t) = kt^n$) a los datos de cada hidrogel mediante regresión no lineal y reportar los bioestadísticos correspondientes (R², SSE, AICc, intervalos de confianza al 95%).
3. Ajustar la **función farmacocinética de primer orden** ($x(t) = \beta(1-e^{-kt})$) a los datos de cada hidrogel y comparar los resultados con el modelo de Peppas.
4. Ajustar la **función de Eureqa** ($x(t) = \rho_1\sqrt{t} - \rho_2 t$) obtenida por regresión simbólica y reportar los bioestadísticos.
5. Ajustar el **modelo EureqaODE** ($\mathrm{d}x/\mathrm{d}t = \rho_1 - \rho_2 x$) resuelto numéricamente mediante el método de Heun y comparar los cuatro modelos entre sí.
6. Determinar el mejor modelo para describir la tasa de liberación del hidrogel N36-2MBA3 con base en los criterios estadísticos obtenidos.
## Lista de archivos incluidos en el repositorio
1. Cuaderno computacional de MATLAB [.mlx].
2. Datos experimentales [.csv].
3. Imágenes de las simulaciones [.pdf].
4. Análisis de regresión no lineal y bioestadísticos [.pdf].
## Referencias
\[1] P. A. Valle, Syllabus para Gemelos Digitales, Tecnológico Nacional de México / Instituto Tecnológico de Tijuana, Tijuana, B.C., México, 2025. Permalink: https://biomath.xyz/course/
 
\[2] M. A. González-Ayón, J. A. Sañudo-Barajas, L. A. Picos-Corrales, & A. Licea-Claverie, "PNVCL-PEGMA nanohydrogels with tailored transition temperature for controlled delivery of 5-fluorouracil", *Journal of Polymer Science Part A: Polymer Chemistry*, vol. 53, issue 22, pp. 2662–2672, Aug 2015. DOI: https://doi.org/10.1002/pola.27766
 
\[3] Bryan, Kurt. *Differential equations: A toolbox for modeling the world*. Simiode, 2022. Permalink: https://www.simiode.org/resources/8307 non-Fickian drug release from polymers. Pharmaceutica Acta Helvetiae, 60(4), 110-111.
