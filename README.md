# 🐷 Piggy Slot

![Status](https://img.shields.io/badge/status-in%20development-yellow)
![License](https://img.shields.io/badge/license-MIT-blue)

**Piggy Slot** es un juego de tragaperras educativo/recreativo desarrollado como proyecto de portfolio. La mecánica principal se centra en una **hucha progresiva con forma de cerdito** que se llena a medida que aparecen monedas durante el juego base. Al explotar, da paso a un **bonus principal** con varias mecánicas divertidas y visualmente atractivas.

> ⚠️ **Nota importante**: Este es un proyecto educativo/demostrativo. No involucra dinero real ni apuestas reales. Todos los créditos son virtuales.

---

## 🎮 Concepto del Juego

- Slot moderna con temática de **dinero, ahorro y riqueza**.  
- El jugador llena una hucha virtual mediante **monedas que aparecen aleatoriamente en posiciones especiales** del tablero.  
- Cuando la hucha explota, se activa un **bonus tipo Hold & Win** con tablero de **3x4**, **3 vidas**, y diferentes tipos de mecánica:
  - Multiplicadores
  - Vidas extra
  - Tablero duplicado  
- En el bonus, las monedas tienen **valores numéricos visibles**, que representan el dinero ganado.  
- La mecánica busca generar **tensión visual y UX clara**, fácil de explicar en portfolio o entrevistas.

---

## ✨ Características Principales

- 🎰 **5 rodillos × 3 filas** con líneas de pago estándar (10 líneas).  
- 🐷 **Sistema de hucha progresiva** con posiciones especiales que alimentan la hucha.  
- 💰 **4 tipos de monedas scatter**: Bronce, Plata, Oro y Diamante.  
- 🎁 **Bonus Hold & Win** con mecánica de 3 vidas, respins, multiplicadores, tablero duplicado.  
- 💎 **4 niveles de Jackpot**: Mini, Minor, Major y Grand (Grand solo si se completa todo el tablero).  
- 📊 **Sistema de apuestas escalable** (0,10€ - 2,00€ demo).  
- 🎨 **Diseño cartoon minimalista** moderno y limpio.  
- 🔄 **Auto-spin** que se detiene al entrar al bonus.  

---

## 🎨 Diseño Visual

### Estilo
- Cartoon minimalista, limpio y colorido.  
- Inspiración: estilo educativo, tipo Duolingo/Crossy Road.  

### Paleta de Colores
- **Fondo:** Morado oscuro con degradados  
- **Hucha:** Rosa neón con detalles dorados  
- **Acentos:** Dorado para premios, verde para acciones positivas  
- **Monedas:** Bronce, Plata, Oro y Diamante con efectos brillantes  

### Indicadores visuales de “cerca de explotar”
- Temblor progresivo del cerdito: suave → medio → fuerte  
- Cambio de expresión del cerdito: normal → tenso → “a punto de explotar”  
- Grietas o brillo interno  
> No mostrar porcentajes exactos; solo sensación visual para UX

---

## 🎰 Mecánicas de Juego

### Símbolos Regulares
- Billetes, lingotes, cofres y bolsas de dinero  
- Solo acompañan a las monedas, sin valor visible, mantienen coherencia temática  

### Símbolos Especiales
- **Wild:** Hucha dorada (sustituye símbolos regulares)  
- **Scatter:** Monedas (Bronce/Plata/Oro/Diamante) que alimentan la hucha  

### Sistema de Hucha
- Solo posiciones especiales alimentan la hucha  
- Cada moneda incrementa internamente la probabilidad de que la hucha explote  
- La explosión es **aleatoria** y depende de:  
  - Monedas en pantalla  
  - Número aleatorio por tirada (1-100) comparado con umbral dinámico  

---

## 🎁 Bonus: Hold & Win

### Cómo funciona
1. La hucha explota y se activa el bonus  
2. Tablero de **3x4**, jugador con **3 vidas**  
3. Desde arriba caen monedas  
4. Cada moneda puede:
   - Colocarse en casilla → resetea las 3 vidas  
   - Pasar de largo → pierdes 1 vida  
5. Bonus termina cuando se acaban las vidas  
6. Se suman todos los valores de las monedas  

### Tipos de bonus al explotar la hucha (ruleta)
- **Multiplicadores:** caen sobre monedas existentes, si no hay → pasan de largo  
- **Vidas extra:** alarga bonus, aumenta margen de error  
- **Tablero duplicado:** dos tableros independientes, se suman al final  

> Siempre sale mínimo 1 tipo. 2 o 3 tipos juntos son raros para no saturar UX  

### Valores de las monedas en el bonus (multiplicadores × BET)
- 🥉 Bronce: x1, x2  
- 🥈 Plata: x5, x10  
- 🥇 Oro: x25, x50  
- 💎 Diamante: x100  

---

## 💎 Jackpots Especiales
- ⭐ MINI: x15  
- ⭐ MINOR: x30  
- ⭐ MAJOR: x100  
- ⭐ GRAND: x1000 (**solo si se completa todo el tablero del bonus**)  

---

## 💰 Sistema de Apuestas
- Créditos iniciales: 1,000€ virtuales  
- Apuesta por defecto: 1€  
- Rango de apuestas: 0,10€ - 2,00€  
- Todos los premios son **multiplicadores del BET**  

---

## 🛠️ Stack Tecnológico
- **Frontend:** Vue 3 + TypeScript  
- **Styling:** Tailwind CSS  
- **Animaciones:** GSAP + CSS Animations  
- **Estado:** Pinia  
- **Hosting:** Firebase Hosting  
- **CI/CD:** GitHub Actions  
- **Control de versiones:** Git + GitHub  

> Proyecto **100% frontend/demo**, sin backend ni dinero real.  

---

## 📂 Estructura del Proyecto
- Carpeta de componentes  
- Carpeta de assets (sprites, sonidos)  
- Carpeta de animaciones  
- Carpeta de store (Pinia)  
- Carpeta de utilidades (RNG, cálculo de bonus)  

---

## 🗓️ Roadmap de Desarrollo

### Fase 1: MVP - Juego Base
- Setup de proyecto (Vue 3 + Tailwind)  
- Diseño de UI básica  
- Sistema de rodillos y spin básico  
- Símbolos y líneas de pago  
- Sistema de apuestas y balance  

### Fase 2: Sistema de Hucha
- Implementar hucha visual  
- Posiciones especiales aleatorias  
- Animaciones de monedas volando a la hucha  
- Indicadores visuales de proximidad (temblor, grietas, expresión)  
- Explosión animada  

### Fase 3: Bonus Hold & Win
- Transición a modo bonus  
- Tablero 3x4, 3 vidas  
- Monedas con valores visibles  
- Tipos de bonus (multiplicador, vidas extra, tablero duplicado)  
- Ruleta al explotar cerdito  
- Suma final de premios y jackpots  

### Fase 4: Polish & UX
- Sonidos y música  
- Animaciones mejoradas  
- Efectos de partículas  
- Feedback visual completo  
- Modo responsive (móvil)  
- Tutorial / ayuda integrada  

### Fase 5: Optimización & Deploy
- Optimización de rendimiento  
- Testing completo  
- Deploy a Firebase Hosting  
- Configurar dominio personalizado  
- Analytics opcional  

---

## 🎯 Objetivos del Proyecto
- Practicar Vue 3 y TypeScript  
- Implementar animaciones complejas  
- Gestión de estado con Pinia  
- Arquitectura escalable de componentes  
- Crear un proyecto destacado para portfolio  

---

## 🤝 Contribuciones
Este es un proyecto personal de aprendizaje. Si tienes sugerencias o mejoras, siéntete libre de abrir un issue.

---

## 📄 Licencia
MIT License - Proyecto de código abierto para referencia educativa.

---

## 👤 Autor
**Alvaro Delgado**  
- GitHub: [@AlvaroS19](https://github.com/AlvaroS19)  
- LinkedIn: [Alvaro Delgado](https://www.linkedin.com/in/alvarodelgado-dev/)
