# 🔄 Metodologías para proyectos de Data Science

## CRISP-DM + Scrum: cómo organizar proyectos donde no sabemos de antemano qué vamos a encontrar

> **Idea central:** CRISP-DM organiza el proceso de análisis. Scrum
> organiza el trabajo del equipo.

------------------------------------------------------------------------

## 🎯 ¿Qué tenemos que entender primero?

En un proyecto de Data Science no siempre sabemos de antemano:

-   qué vamos a encontrar en los datos;
-   qué variables serán útiles;
-   qué modelo funcionará;
-   si los datos tendrán la calidad necesaria;
-   si la solución que imaginamos inicialmente será realmente la
    adecuada.

Por eso, trabajar con una metodología pensada para un resultado
completamente definido desde el comienzo puede resultar insuficiente.

La pregunta que nos guía es:

> **¿Cómo organizamos un proyecto cuando investigar y descubrir también
> forman parte del trabajo?**

------------------------------------------------------------------------

# 1. 🏢 Desarrollo de software vs. Data Science

En un proyecto de desarrollo de software podemos tener un resultado
relativamente definido:

> "Necesitamos desarrollar esta funcionalidad."

En Data Science, en cambio, podemos recibir un objetivo como:

> "Queremos predecir qué estudiantes tienen riesgo de abandonar la
> escuela."

Y aparecen preguntas que todavía no tienen respuesta:

-   ¿Qué significa exactamente "abandono"?
-   ¿Qué datos necesitamos?
-   ¿Tenemos esos datos?
-   ¿Son confiables?
-   ¿Qué variables pueden explicar el fenómeno?
-   ¿Qué modelo podría funcionar?
-   ¿Cómo sabemos si el resultado es suficientemente bueno?

Por eso:

> **Data Science tiene una componente exploratoria e investigativa que
> debe contemplarse al organizar el proyecto.**

------------------------------------------------------------------------

# 2. 🧭 CRISP-DM

CRISP-DM es una metodología ampliamente utilizada para proyectos de
Business Analytics.

Sus etapas son:

``` text
Comprensión del negocio
          ↓
Comprensión de datos
          ↓
Preparación de datos
          ↓
Modelado
          ↓
Evaluación
          ↓
Despliegue
```

### ⚠️ Importante

CRISP-DM **no debe entenderse como un camino estrictamente lineal**.

Durante el proyecto podemos descubrir que necesitamos volver a una etapa
anterior.

Por ejemplo:

``` text
Preparación
    ↓
Modelado
    ↓
Evaluación
    ↓
🚨 Problema
    ↓
Volver a preparación
```

Esto es especialmente importante cuando el modelo, los datos o los
resultados no cumplen con los objetivos definidos.

------------------------------------------------------------------------

# 3. 🔎 Las etapas de CRISP-DM en lenguaje simple

  | Etapa | Pregunta principal |
|---|---|
| 🏢 Comprensión del negocio | **¿Qué queremos resolver?** |
| 🔎 Comprensión de datos | **¿Qué tenemos?** |
| 🧹 Preparación de datos | **¿Podemos trabajar con estos datos?** |
| 🤖 Modelado | **¿Podemos construir una solución?** |
| 🧐 Evaluación | **¿La solución sirve realmente?** |
| 🚀 Despliegue | **¿Cómo llevamos la solución a la realidad?** |

------------------------------------------------------------------------

## 3.1 🏢 Comprensión del negocio

La primera etapa busca comprender los objetivos y requisitos desde la
perspectiva del negocio.

Algunas preguntas:

-   ¿Cuál es el problema?
-   ¿Qué queremos lograr?
-   ¿Cuál es el objetivo?
-   ¿Cómo vamos a determinar si el proyecto tuvo éxito?
-   ¿Qué recursos tenemos?
-   ¿Qué restricciones existen?

### Ejemplo

**Problema:** queremos identificar estudiantes con riesgo de abandono.

Antes de entrenar un modelo debemos definir qué entendemos por
"abandono" y para qué utilizaremos la predicción.

> 💡 Podemos construir un modelo técnicamente muy bueno y, aun así,
> resolver el problema equivocado.

------------------------------------------------------------------------

## 3.2 🔎 Comprensión de datos

Comenzamos a trabajar con los datos disponibles.

Buscamos:

-   conocer las fuentes;
-   describir los datos;
-   explorar las variables;
-   detectar problemas de calidad;
-   encontrar primeras señales;
-   identificar anomalías, patrones y tendencias;
-   formular hipótesis.

### Pregunta clave

> **¿Los datos que tenemos pueden ayudarnos a responder la pregunta del
> negocio?**

------------------------------------------------------------------------

## 3.3 🧹 Preparación de datos

En esta etapa construimos el conjunto de datos que será utilizado para
el modelado.

Podemos:

-   seleccionar información;
-   limpiar datos;
-   transformar variables;
-   crear nuevas variables;
-   integrar distintas fuentes;
-   seleccionar registros y atributos;
-   dar formato a los datos.

### Resultado esperado

> **Un dataset preparado para trabajar con las herramientas de
> modelado.**

Y algo importante: esta etapa puede repetirse varias veces.

------------------------------------------------------------------------

## 3.4 🤖 Modelado

Seleccionamos y aplicamos diferentes técnicas de modelado.

Podemos:

-   probar diferentes algoritmos;
-   definir parámetros;
-   considerar supuestos;
-   entrenar modelos;
-   comparar resultados;
-   revisar el funcionamiento general.

### Pero...

Un determinado modelo puede requerir que volvamos a preparar los datos
de otra manera.

Por eso:

``` text
Preparación
      ↓
Modelado
      ↓
Evaluación
      ↓
¿Problemas?
   ↙       ↘
 Sí         No
 ↓           ↓
Volver       Continuar
```

------------------------------------------------------------------------

## 3.5 🧐 Evaluación

En esta etapa evaluamos los modelos considerando los criterios de éxito
definidos.

No alcanza con preguntar:

> **"¿Qué tan bueno es el modelo?"**

También debemos preguntar:

> **"¿El modelo sirve para el problema que queríamos resolver?"**

La evaluación permite:

-   determinar si los resultados son satisfactorios;
-   identificar problemas;
-   definir los próximos pasos;
-   tomar decisiones sobre el proyecto.

------------------------------------------------------------------------

## 3.6 🚀 Despliegue

Si la evaluación es positiva, podemos avanzar hacia la utilización de la
solución.

El despliegue puede ser:

-   un reporte;
-   un dashboard;
-   un proceso de explotación de información;
-   un modelo utilizado por una organización;
-   otra forma de poner los resultados a disposición de los usuarios.

El objetivo es que los resultados del análisis puedan convertirse en
algo útil para la organización y para quienes toman decisiones.

------------------------------------------------------------------------

# 4. 🚨 Un ejemplo que muestra la importancia de iterar

Supongamos que queremos predecir abandono escolar.

Después de preparar los datos entrenamos un modelo.

El resultado inicial muestra:

> **97% de accuracy 🎉**

¿Festejamos?

No necesariamente.

Descubrimos que el modelo presenta **overfitting**.

Entonces:

``` text
Preparación
     ↓
Modelado
     ↓
Evaluación
     ↓
🚨 Overfitting
     ↓
Nueva preparación
     ↓
Nuevo modelado
     ↓
Nueva evaluación
```

### Idea clave

> **El proyecto no avanza necesariamente en línea recta.**

Un hallazgo durante la evaluación puede obligarnos a volver a una etapa
anterior.

------------------------------------------------------------------------

# 5. 🔄 El problema de organizar este trabajo

Hasta acá tenemos una metodología para organizar el proceso analítico.

Pero todavía tenemos que responder otra pregunta:

> **¿Cómo organizamos el trabajo de un equipo que está haciendo todo
> esto?**

Ahí aparece Scrum.

------------------------------------------------------------------------

# 6. 🏃 Scrum + Business Analytics

Scrum es un framework pensado originalmente para la organización ágil
del trabajo, especialmente en contextos de desarrollo de software.

En proyectos de Business Analytics podemos aprovechar algunas de sus
prácticas, pero adaptándolas a la naturaleza exploratoria de Data
Science.

### Scrum aporta:

-   planificación;
-   priorización;
-   trabajo en Sprints;
-   objetivos;
-   entregables;
-   revisión;
-   feedback;
-   retrospectiva.

### CRISP-DM aporta:

-   comprensión del negocio;
-   comprensión de datos;
-   preparación;
-   modelado;
-   evaluación;
-   despliegue;
-   iteración del proceso analítico.

------------------------------------------------------------------------

# 7. 🧩 ¿Cómo se relacionan CRISP-DM y Scrum?

  | CRISP-DM                  | Scrum                         |
|---------------------------|-------------------------------|
| Comprensión del negocio   | Product Backlog               |
| Comprensión de datos      | Product / Sprint Backlog      |
| Preparación de datos      | Trabajo durante el Sprint     |
| Modelado                  | Trabajo durante el Sprint     |
| Despliegue                | Trabajo durante el Sprint     |
| Evaluación                | Sprint Review                 |
| Iteración                 | Nuevo Sprint / reajuste       |

### 💡 Idea central

> **CRISP-DM organiza el proceso analítico.**
>
> **Scrum organiza el trabajo del equipo.**

No son metodologías que necesariamente compiten entre sí.

Pueden complementarse.

------------------------------------------------------------------------

# 8. 📅 ¿Qué cambia cuando usamos Sprints?

Cada Sprint puede comenzar con:

-   planificación;
-   priorización;
-   definición de objetivos;
-   selección de tareas.

Durante el Sprint:

-   se exploran datos;
-   se preparan datasets;
-   se construyen variables;
-   se prueban modelos;
-   se analizan resultados.

Al finalizar:

-   se muestran avances;
-   se reciben comentarios;
-   se evalúan resultados;
-   se decide qué hacer a continuación;
-   se realiza una retrospectiva.

------------------------------------------------------------------------

# 9. 📦 Los entregables de un Sprint de Data Science

Acá aparece una diferencia importante respecto del desarrollo de
software.

### Un Sprint NO necesariamente tiene que terminar con:

> ❌ "Un modelo terminado y listo para producción."

Puede terminar con:

-   un dataset preparado;
-   un análisis exploratorio;
-   nuevas variables;
-   una hipótesis;
-   un modelo preliminar;
-   un modelo parcialmente validado;
-   resultados para revisión;
-   un informe de metadatos;
-   un problema detectado;
-   una recomendación.

### ¿Para qué?

Para que el equipo y el cliente puedan responder:

> **¿Estamos avanzando en una dirección viable?**

Y, si es necesario:

> **¿Tenemos que corregir el rumbo?**

------------------------------------------------------------------------

# 10. ⚠️ Trampas de CRISP-DM

La naturaleza iterativa de los proyectos de analítica puede generar
algunos problemas.

## 🕳️ Trampa 1 --- Quedarnos eternamente entendiendo los datos

Hay tanta información disponible que el equipo puede perder el foco
intentando hacer coincidir todo lo que encuentra con el problema de
negocio.

### Pregunta para salir:

> **¿Qué necesitamos saber para responder la pregunta que tenemos?**

------------------------------------------------------------------------

## 🕳️ Trampa 2 --- Ciclo infinito de preparación y modelado

Podemos entrar en:

``` text
Preparar
   ↓
Modelar
   ↓
No funciona
   ↓
Preparar
   ↓
Modelar
   ↓
No funciona
   ↓
...
```

No existe un modelo perfecto.

Por eso necesitamos criterios para determinar cuándo un resultado es
suficientemente bueno para el objetivo.

------------------------------------------------------------------------

## 🕳️ Trampa 3 --- Nunca llegar a implementar

Podemos iterar tantas veces que el proyecto nunca llega al momento de
utilizar los resultados.

### Pregunta clave:

> **¿Cuándo tenemos suficiente evidencia para avanzar?**

------------------------------------------------------------------------

# 11. 🧠 ¿Por qué Scrum necesita adaptarse?

## Problema 1 --- Estimar es más difícil

En Data Science muchas tareas son exploratorias.

No siempre sabemos cuánto tiempo llevará descubrir una respuesta.

------------------------------------------------------------------------

## Problema 2 --- El alcance puede cambiar

Los datos pueden contradecir lo que el negocio suponía inicialmente.

Por ejemplo:

> El negocio cree que una variable explica el abandono.

Pero los datos muestran otra cosa.

Entonces necesitamos pivotar.

------------------------------------------------------------------------

## Problema 3 --- El entregable no siempre es tangible

En software podemos mostrar:

> "Construimos esta funcionalidad."

En Data Science podemos terminar un Sprint diciendo:

> "Probamos esta hipótesis y descubrimos que no funciona."

Eso también es información valiosa.

------------------------------------------------------------------------

# 12. 🔄 La lógica completa

``` text
                 ┌───────────────────┐
                 │ Comprender negocio│
                 └─────────┬─────────┘
                           ↓
                 ┌───────────────────┐
                 │ Comprender datos  │
                 └─────────┬─────────┘
                           ↓
                 ┌───────────────────┐
                 │ Preparar datos    │
                 └─────────┬─────────┘
                           ↓
                 ┌───────────────────┐
                 │ Modelar           │
                 └─────────┬─────────┘
                           ↓
                 ┌───────────────────┐
                 │ Evaluar           │
                 └─────────┬─────────┘
                           ↓
                    ¿Funciona?
                    ↙        ↘
                  NO          SÍ
                  ↓            ↓
          Volver atrás      Desplegar
                  ↓
             Nuevo Sprint
                  ↓
                🔄
```

------------------------------------------------------------------------

# 13. 🧪 Actividad

## Caso: abandono escolar

Una organización quiere identificar estudiantes con riesgo de abandono.

Tenemos:

-   asistencia;
-   calificaciones;
-   edad;
-   materias aprobadas;
-   información socioeducativa.

### Tenemos un Sprint.

¿Cuáles priorizarías?

-   [ ] Definir qué significa "abandono".
-   [ ] Entrenar un Random Forest.
-   [ ] Revisar calidad y disponibilidad de los datos.
-   [ ] Crear el dashboard final.
-   [ ] Explorar las variables disponibles.
-   [ ] Presentar resultados.

### Dinámica

1.  Elegí **3 opciones**.
2.  Comparalas con otra persona.
3.  Justificá tu selección.
4.  ¿Qué entregable esperarías al final del Sprint?

------------------------------------------------------------------------

# 14. 🚨 Segunda parte de la actividad

El equipo entrena un modelo y obtiene:

> **97% de accuracy**

Pero durante la evaluación descubre:

> **OVERFITTING**

### ¿Qué hacemos?

-   ¿Seguimos porque el accuracy es alto?
-   ¿Volvemos a preparación?
-   ¿Probamos otra estrategia de modelado?
-   ¿Evaluamos nuevamente?
-   ¿Qué debería entregarse al final de este Sprint?

### Objetivo

Comprender que:

> **Un problema descubierto durante el Sprint también puede ser un
> resultado valioso.**

------------------------------------------------------------------------

# 15. 💬 Retrospectiva

Al finalizar un Sprint podemos preguntarnos:

### ¿Qué descubrimos?

### ¿Qué funcionó?

### ¿Qué no funcionó?

### ¿Qué necesitamos cambiar?

### ¿Qué hacemos en el próximo Sprint?

------------------------------------------------------------------------

# 16. 🏁 Para llevarnos

### CRISP-DM

> 🧭 **¿Cómo avanzamos en un proyecto analítico?**

### Scrum

> 🗂️ **¿Cómo organizamos el trabajo del equipo?**

### Juntos

> 🔄 **Iteramos, mostramos avances, recibimos feedback y corregimos el
> rumbo.**

------------------------------------------------------------------------

## ⭐ Idea final

> **Un proyecto de Data Science no es simplemente construir un modelo.**
>
> Es entender un problema, trabajar con datos, experimentar,
> equivocarnos, aprender, volver atrás y volver a probar.
>
> Por eso necesitamos una forma de organizar el trabajo sin pretender
> que conocemos el resultado desde el día uno.
>
> **CRISP-DM nos da una estructura para el proceso analítico.**
>
> **Scrum nos ayuda a organizar el trabajo en equipo.**
>
> Y la combinación de ambos permite trabajar de manera iterativa,
> mostrando avances y corrigiendo el rumbo cuando los datos nos dicen
> que estábamos mirando para otro lado.

### 💡 Para recordar

> **En Data Science, que un Sprint no nos dé la respuesta que
> esperábamos... también puede ser un resultado.**

    
