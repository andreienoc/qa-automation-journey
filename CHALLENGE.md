# 🎯 Prueba Técnica: API Data Checker

**Rol:** QA Automation Engineer (Junior)
**Duración:** 2 semanas
**Nivel:** Fundamentos (Python + APIs + Testing)

---

## 📋 Contexto del challenge

Imaginá que acabás de entrar como QA Automation Junior a una empresa que consume datos de APIs externas dentro de su producto. Tu líder de equipo te asigna tu primera tarea real:

> "Necesitamos un script que se conecte a nuestros endpoints, valide que las respuestas sean correctas, y nos avise automáticamente si algo se rompe. No hace falta que sea perfecto, pero tiene que ser confiable y fácil de leer para cualquiera del equipo."

Esto es exactamente lo que hace un QA Automation Engineer en su día a día: no espera a que un humano pruebe todo a mano, construye un sistema que lo prueba por él.

---

## 🎮 Cómo lo vas a jugar

Este challenge está dividido en **4 niveles**. Cada nivel desbloquea el siguiente. No pases al nivel N+1 sin haber terminado y probado el nivel N — así se trabaja en equipos reales, con entregas incrementales.

Llevá un diario corto de avance (podés usarlo después para tus posts de LinkedIn): qué hiciste, qué se rompió, cómo lo arreglaste.

---

## 🥉 Nivel 1 — Conexión (días 1-3)

**Objetivo:** Conectarte a una API pública y traer datos reales.

**Tareas:**
- [ ] Elegí una API pública gratuita: [reqres.in](https://reqres.in) o [jsonplaceholder.typicode.com](https://jsonplaceholder.typicode.com)
- [ ] Escribí una función en Python que haga un `GET` a un endpoint de usuarios/posts
- [ ] Imprimí el código de estado de la respuesta (`200`, `404`, etc.)
- [ ] Imprimí el JSON completo de la respuesta, formateado y legible

**Criterio de éxito:** corrés el script y ves en consola una lista de datos reales traídos desde internet, sin errores.

---

## 🥈 Nivel 2 — Verificación (días 4-7)

**Objetivo:** Dejar de solo "mirar" los datos y empezar a **verificarlos automáticamente**.

**Tareas:**
- [ ] Verificá que el código de estado sea `200` (si no lo es, el script debe decir claramente qué falló)
- [ ] Verificá que cada elemento de la respuesta tenga los campos obligatorios (ej: `id`, `email`, `name`) — si falta alguno, repórtalo
- [ ] Verificá que ningún campo esperado venga vacío o en `null`
- [ ] Contá cuántas verificaciones pasaron y cuántas fallaron

**Criterio de éxito:** el script te dice, sin que vos revises nada a mano, si los datos están "sanos" o no.

> 💡 Este es el corazón del testing: no confiar en que "seguro está bien", sino demostrarlo con código.

---

## 🥇 Nivel 3 — Reporte (días 8-11)

**Objetivo:** Que cualquier persona del equipo (no solo vos) entienda el resultado en 5 segundos.

**Tareas:**
- [ ] Generá un reporte final tipo:
  ```
  ✅ 8/10 verificaciones pasaron
  ❌ Usuario id=3 no tiene campo 'email'
  ❌ Usuario id=7 tiene 'name' vacío
  ```
- [ ] Guardá ese reporte en un archivo `.txt` o `.json` con fecha y hora de ejecución
- [ ] (Opcional, sumá puntos) Coloreá la salida en consola: verde para OK, rojo para fallos (librería `colorama`)

**Criterio de éxito:** alguien que nunca vio tu código puede correr el script y entender el resultado sin preguntarte nada.

---

## 🏆 Nivel 4 — Automatización real (días 12-14)

**Objetivo:** Que el script se ejecute solo, como en una empresa de verdad.

**Tareas:**
- [ ] Subí el proyecto a GitHub con estructura clara (ver abajo)
- [ ] Configurá un **GitHub Action** simple que corra tu script automáticamente cada vez que hacés push
- [ ] Escribí el `README.md` del repo explicando qué hace el proyecto, cómo correrlo localmente, y qué aprendiste

**Criterio de éxito:** hacés push a GitHub y ves en la pestaña "Actions" que tu script corrió solo, sin que vos lo ejecutes a mano.

---

## 📁 Estructura esperada del repo

```
api-data-checker/
├── README.md              # qué es, cómo correrlo, qué aprendiste
├── CHALLENGE.md            # este archivo
├── checker.py               # script principal
├── requirements.txt         # librerías usadas
├── reports/                 # reportes generados (.txt/.json)
└── .github/
    └── workflows/
        └── run-checks.yml   # GitHub Action del Nivel 4
```

---

## 🚫 Qué NO hace falta para este challenge

- No hace falta usar frameworks de testing todavía (Pytest viene en el próximo proyecto)
- No hace falta manejar autenticación compleja
- No hace falta que sea "bonito" visualmente — que sea claro y funcional

---

## 📱 Para tu LinkedIn

Cada nivel completado es un post potencial:

- **Nivel 1:** "Día 3: conecté mi primer script a una API real 🎉 [captura]"
- **Nivel 2:** "Día 7: mi script ahora detecta automáticamente cuando faltan datos — así empieza el testing de verdad"
- **Nivel 3:** "Día 11: generé mi primer reporte automático, legible para cualquiera del equipo"
- **Nivel 4:** "Día 14: mi primer pipeline de CI corriendo solo en GitHub Actions ✅ Repo: [link]"

---

## ✅ Entrega final

Al terminar los 4 niveles vas a tener:
1. Un repo público en GitHub, con historial de commits mostrando tu progreso real
2. Un script funcional que simula el trabajo diario de un QA Automation Engineer
3. Material concreto para 4 posts de LinkedIn documentando tu proceso
4. Tu primera pieza de portfolio para mostrar en entrevistas

**Buena suerte. Empezá cuando quieras — el reloj corre desde tu primer commit.** ⏱️
