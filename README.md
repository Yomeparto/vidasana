# Calorías y menús para bajar peso

Aplicación web gratuita, en un único archivo HTML, para **bajar de peso de forma ordenada**: calcula tus calorías diarias según tu edad, altura y peso, registra lo que comes, te propone menús y un plan semanal con los gramos de cada ingrediente, genera la lista de la compra y crea un **plan de entrenamiento en casa adaptado a tus limitaciones**.

Inspirada en apps como Fitia. Funciona sin instalación, sin registro y sin servidor.

## Características

### Calorías y diario
- Cálculo de tu **objetivo diario de calorías** con la fórmula Mifflin-St Jeor, según sexo, edad, altura, peso, nivel de actividad y ritmo de pérdida (0,25, 0,5 o 0,75 kg por semana).
- Estimación de las semanas necesarias para llegar a tu peso objetivo.
- Diario de comidas (desayuno, almuerzo, merienda y cena) con un anillo que muestra las calorías que te quedan y una barra de proteína.
- Buscador con **más de 220 alimentos** (carnes, pescados, lácteos, cereales, verduras, frutas, platos hechos, dulces y bebidas).

### Menús y compra
- **Menú diario** con 8 opciones por comida y los **gramos de cada ingrediente**, ajustados a tu objetivo de calorías.
- **Plan semanal** de lunes a domingo sin repetir platos, también con gramos.
- **Lista de la compra** automática con los 7 días sumados, agrupada por secciones, con casillas para ir tachando y botón para copiarla. Carnes, pescados, arroz, pasta y legumbres se muestran en crudo, tal como se compran.

### Entrenamiento personal en casa
- **73 ejercicios** explicados paso a paso, con consejo y series o tiempo.
- Tres niveles: **principiante, intermedio y profesional**.
- De 2 a 6 días por semana, sesiones de 15, 30, 45 o 60 minutos, con o sin material (botellas o mancuernas).
- Adaptación a limitaciones: rodillas, espalda baja, muñecas u hombros, saltos o impacto, dificultad para tumbarse o levantarse del suelo y problemas de equilibrio. Los ejercicios que no encajan nunca aparecen en el plan.
- Cada sesión incluye calentamiento, circuito principal y estiramientos, y se puede marcar como hecha.

### Diseño
- Interfaz responsive pensada para móvil, con cabecera ilustrada en SVG y fondo con motivos de comida.
- Sin imágenes externas ni dependencias.

## Cómo usarla

1. Descarga el archivo HTML y, si quieres publicarlo con GitHub Pages, renómbralo a `index.html`.
2. Ábrelo en el navegador (doble clic).
3. Ve a **Mis datos**, rellena el formulario y pulsa **Calcular mi objetivo**.
4. Usa las pestañas **Hoy**, **Menú**, **Semana** y **Entreno**.

### Publicar con GitHub Pages
1. Sube `index.html` al repositorio.
2. En **Settings → Pages**, elige la rama `main` y la carpeta `/ (root)`.
3. En unos minutos tendrás la web en `https://tu-usuario.github.io/nombre-del-repositorio/`.

### Usarla en WordPress
Pega el código en un bloque **HTML personalizado**. Se recomienda una versión con los estilos limitados a un contenedor para no chocar con el tema.

## Privacidad

Todo se guarda en el **navegador** de cada persona (`localStorage`). No hay servidor, cuentas ni envío de datos. Si se borran los datos del navegador, se pierde el diario.

## Cómo se calcula

- **Metabolismo basal:** Mifflin-St Jeor.
- **Gasto diario:** metabolismo basal por el factor de actividad (1,2 a 1,725).
- **Objetivo:** gasto diario menos el déficit (ritmo × 7700 kcal ÷ 7 días), con un mínimo de **1.500 kcal en hombres y 1.200 en mujeres**.
- **Proteína sugerida:** 1,6 g por kg de peso.
- **Reparto de calorías:** 25 % desayuno, 35 % almuerzo, 10 % merienda y 30 % cena.
- Solo para adultos (18 a 90 años). No admite pesos objetivo por debajo de un IMC de 18,5.

## Tecnologías

HTML, CSS y JavaScript puros (sin frameworks ni librerías). Solo usa las tipografías Bricolage Grotesque y Figtree de Google Fonts, con tipografías del sistema como alternativa.

## Personalización

Los datos están al principio del `<script>`, en constantes fáciles de editar:

| Constante | Contenido |
|-----------|-----------|
| `FOODS` | Alimentos del buscador: nombre, ración, kcal y proteína |
| `ING` | Ingredientes de los menús, por cada 100 g |
| `PLAN` | Platos de cada comida y sus gramos |
| `CAT`, `RAW` | Sección de la lista de la compra y conversión de cocinado a crudo |
| `EX` | Ejercicios: nivel, material, limitaciones, explicación y consejo |
| `LIM` | Limitaciones que se pueden marcar |

## Aviso importante

Esta herramienta es **orientativa** y no sustituye el consejo de un médico, dietista o fisioterapeuta. Si tienes una enfermedad, una lesión, estás embarazada o das el pecho, consulta con un profesional antes de cambiar tu dieta o empezar a entrenar. Si sientes dolor, mareo o falta de aire durante un ejercicio, detente.

## Licencia

Elige la licencia que prefieras (por ejemplo, MIT) y añade aquí el archivo `LICENSE`.
