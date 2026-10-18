# Mini RPG: Batalla de Calabozos (CLI)

## Descripción y Mecánica del Juego
**Mini RPG: Batalla de Calabozos** es un juego de rol táctico por turnos operado completamente desde la consola. El objetivo del juego es que el equipo de jugadores sobreviva a una serie de encuentros contra monstruos en un calabozo cada vez más desafiante hasta derrotar al jefe final.

### Roles de los Participantes (Equipos de 2 a 3 jugadores)
Cada integrante del grupo elige un rol único con características y habilidades especiales:
1. **El Guerrero (Tanque / Daño Físico):** 
   - *Poderes y Habilidades:* Posee alta vida y defensa. Su ataque especial es el **"Golpe Crítico"** (hace el doble de daño ignorando parte de la armadura del enemigo) y puede usar la habilidad **"Escudo Protector"** para reducir el daño recibido en el siguiente turno.
2. **El Mago (Daño Mágico / Control):**
   - *Poderes y Habilidades:* Tiene baja vida pero un ataque devastador. Su poder principal es la **"Bola de Fuego"** (daño mágico directo) y el hechizo **"Curación Arcana"** para sanar puntos de vida a sí mismo o a un compañero.
3. **El Arquero o Pícaro (Daño Ágil / Apoyo - Opcional para 3 jugadores):**
   - *Poderes y Habilidades:* Alta velocidad y probabilidad de evasión. Su habilidad es el **"Ataque Veloz"** (permite atacar dos veces en un turno) y **"Flecha Venenosa"** (aplica daño por sangrado durante los turnos siguientes).

### El Enemigo y la Inteligencia del Sistema
El sistema genera de forma automática a los enemigos según el nivel del calabozo:
- **Enemigos Comunes (Goblins, Esqueletos, Orcos):** Tienen ataques básicos y patrones de asalto aleatorios.
- **El Jefe Final (El Señor del Calabozo):** Aparece en la última fase. Tiene una barra de vida masiva y cuenta con un poder especial llamado **"Golpe Oscuro"** que se activa cada 3 turnos, obligando a los jugadores a coordinar quién absorbe el daño o quién cura.

---

## Estructura del Proyecto
   text
MiniRPG/
│
├── src/
│   ├── __init__.py
│   ├── characters.py    # Clases POO para Héroes (Guerrero, Mago) y Enemigos.
│   ├── combat.py        # Motor de turnos, cálculo de daño, críticos y aplicación de estados.
│   └── dungeon.py       # Generador de encuentros, progresión de niveles y gestión de turnos.
│
├── tests/
│   ├── __init__.pygit status
│   └── test_combat.py   # Pruebas unitarias para validar fórmulas de daño y límites de vida.
│
└── main.py              # Interfaz de consola interactiva que coordina la aventura.