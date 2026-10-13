# investment-competition-coach

Skill de Claude que hace de coach y sparring para equipos de estudiantes en competiciones de inversión: Wharton Global High School Investment Competition, CFA Research Challenge, ligas de bolsa escolares y cualquier concurso en el que haya que diseñar una estrategia o una cartera para un cliente a partir de un caso.

## Qué hace

- Pide en el chat el caso del cliente, las reglas, los entregables y la política de IA de la competición. No depende de ninguna edición concreta, así que sirve año tras año.
- Construye con el equipo una ficha del cliente donde cada dato va etiquetado como dato del caso, inferencia o pendiente.
- Acompaña por fases: entender al cliente, Investment Policy Statement (IPS), asset allocation, selección de valores, gestión durante la competición e informe final.
- Trabaja con preguntas socráticas, escenarios de estrés y simulacros de jurado.
- No redacta texto para los entregables. Al cerrar cada sesión genera el registro de uso de IA para los Works Cited y un punto de guardado para seguir en otro chat.

## Instalación

### Claude (web y escritorio)

1. Descarga `investment-competition-coach.zip` desde la sección **Releases** de este repositorio.
2. En Claude, abre la sección de Skills, pulsa **+**, luego **Create skill** y **Upload a skill**, y sube el ZIP.
3. Comprueba que la ejecución de código está activada en la configuración.

### Claude Code

```bash
git clone https://github.com/Josefbenbunan/investment-competition-coach.git
cp -r investment-competition-coach/skills/investment-competition-coach ~/.claude/skills/
```

### Con el CLI de skills

```bash
npx skills add Josefbenbunan/investment-competition-coach
```

## Cómo se usa

Basta con escribir algo como *"Estamos en la competición de inversión de Wharton y queremos empezar a trabajar el caso"*. La skill pedirá lo que necesita.

Consejo: para cada competición, cread un Proyecto en Claude y subid el caso como archivo. Así no hay que pegarlo en cada chat.

## Estructura

```
skills/investment-competition-coach/
├── SKILL.md                      # instrucciones principales
├── references/
│   ├── ips-framework.md          # marco conceptual del IPS
│   ├── sparring-questions.md     # preguntas por fase, modo jurado, escenarios de estrés
│   └── ai-use-log.md             # formato del registro de IA y punto de guardado
└── assets/
    └── case-intake.md            # plantilla de la ficha del cliente
```

## Aviso

Herramienta educativa. No constituye asesoramiento financiero. Cada equipo es responsable de cumplir las normas de su competición y de declarar el uso de IA tal como se exija.
