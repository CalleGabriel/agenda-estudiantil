# Agenda Estudiantil

## Problema
Problema concreto: Los estudiantes anotan tareas y horarios en chats, cuadernos y notas sueltas, y por eso olvidan entregas.
Personas beneficiarias: Estudiantes de mi curso que tienen varias materias.
Evidencia inicial: Lo veo en mi curso: se pregunta seguido "¿para cuándo era la tarea?". Preguntaré a algunos compañeros si les pasa.

## Solución
Descripción de la solución: Agenda Estudiantil ayudará a los estudiantes a organizarse y a no olvidar entregas: es una app para Android que guarda sus tareas con fecha y las muestra ordenadas, de la más cercana a la más lejana.
Funcionalidades principales: 1. Registro de tareas — Agregar y borrar tareas con materia y fecha de entrega.
2. Lista de pendientes — Ver las tareas ordenadas por fecha y marcarlas como hechas.
3. Horario semanal — Ver las clases de cada día.
Recorrido de uso: 1. Abre la app y ve sus pendientes. 2. Agrega una tarea con materia y fecha. 3. La marca como hecha al terminar. 4. Revisa su horario.
Pantallas previstas: Pendientes (inicio): Ver tareas y marcarlas como hechas.
Nueva tarea: Agregar una tarea.
Horario: Ver las clases de la semana.
Diferenciación: Es más simple que Google Calendar o Notion: está pensada para estudiantes y solo tiene lo necesario.
Comprobaciones: Cuando el usuario agrega una tarea con fecha, entonces la app debe mostrarla en la lista ordenada por fecha.
Cuando el usuario marca una tarea como hecha, entonces la app debe quitarla de los pendientes.
Resumen: Quiero resolver el olvido de entregas mediante una app que reúne tareas y horario, para que los estudiantes se organicen mejor. La primera versión permitirá agregar tareas con fecha, verlas ordenadas y marcarlas como hechas.
Mejora posterior: Se completará después de recibir la retroalimentación de Mentor.

## Objetivos
- Agregar una tarea en máximo 3 pasos (abrir Nueva tarea, llenar materia y fecha, tocar Guardar); evidencia: video corto del flujo.
- Ordenar 5 tareas de prueba (2 con la misma fecha y 1 sin fecha) con la más cercana arriba y la sin fecha al final; evidencia: captura de la lista.
- Elegir la fecha con un selector de calendario para evitar formatos incorrectos; evidencia: captura del selector.
- Guardar con AsyncStorage: crear 3 tareas, cerrar y reabrir la app, y que sigan en la lista; evidencia: video de la prueba.
- Marcar una tarea como hecha y que no vuelva a pendientes al reabrir la app; evidencia: captura antes y después.
- Probar con 3 compañeros: es éxito si agrega una tarea sin ayuda al primer intento y responde "sí" a "¿te ayudaría a recordar tus entregas?"; meta: 2 de 3; evidencia: tabla de resultados.

## Habilidades
- React Native con Expo y TypeScript
- Componentes reutilizables y props tipadas
- Estado local y hooks (useState / custom hooks)
- Navegación entre pantallas (Expo Router)
- Estilos, temas y diseño adaptable
- Persistencia local con AsyncStorage

## Alcance inicial
Sí incluiré en el MVP: Agregar y eliminar tareas con materia y fecha.
Lista de pendientes ordenada por fecha.
Marcar tareas como hechas.
Horario semanal con las clases.
Datos guardados en el teléfono con AsyncStorage: la lista de tareas se guarda en formato JSON y se lee al abrir la app.
No incluiré todavía: No tendrá cuentas, internet ni nube.
No tendrá notificaciones ni copias de seguridad.

## Restricciones
- Riesgo y plan: Ya hice una app con Expo, Expo Router y TypeScript (calculadora Retro) con componentes reutilizables.
- Paso 1: proyecto con Expo Router, 3 pestañas y formulario de Nueva tarea con useState.
- Paso 2: guardar y leer la lista con AsyncStorage (setItem y getItem) en un hook useTareas.
- Paso 3: ordenar por fecha con sort() y probarlo con 5 tareas.
- Paso 4: marcar como hecha, armar el horario y probar con 3 compañeros.
- Riesgo: manejar fechas; probaré primero con una sola tarea y la documentación de Expo.
- Si se borra la app, se pierden los datos; es un límite de la primera versión.
