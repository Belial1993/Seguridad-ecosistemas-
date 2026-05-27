# 🤝 Guía de Contribución

¡Gracias por tu interés en contribuir a **Seguridad-ecosistemas-**! 

Este documento te guía a través del proceso de contribución, desde reportar problemas hasta enviar cambios.

---

## 📋 Tabla de Contenidos

1. [Código de Conducta](#código-de-conducta)
2. [Antes de Empezar](#antes-de-empezar)
3. [Reportar Vulnerabilidades](#reportar-vulnerabilidades)
4. [Reportar Bugs](#reportar-bugs)
5. [Sugerir Mejoras](#sugerir-mejoras)
6. [Proceso de Pull Request](#proceso-de-pull-request)
7. [Guía de Estilo](#guía-de-estilo)
8. [Estructura de Commits](#estructura-de-commits)

---

## 📜 Código de Conducta

### Nuestro Compromiso

Nos comprometemos a proporcionar un ambiente acogedor y respetuoso para todos.

### Comportamiento Esperado

- Usa lenguaje inclusivo y respetuoso
- Acepta crítica constructiva
- Enfócate en lo mejor para la comunidad
- Muestra empatía hacia otros miembros

### Comportamiento Inaceptable

- Acoso, intimidación o discriminación
- Contenido sexual o violento
- Spam o autopromoción
- Ataques personales

---

## 🔍 Antes de Empezar

### Verifica que tu contribución sea necesaria

- [ ] Consulta [Issues existentes](../../issues)
- [ ] Revisa [Pull Requests abiertos](../../pulls)
- [ ] Lee la [documentación actual](docs/)
- [ ] Verifica el [Roadmap](README.md#-roadmap)

### Configura tu entorno local

```bash
# 1. Fork el repositorio
git clone https://github.com/TU_USUARIO/Seguridad-ecosistemas-
cd Seguridad-ecosistemas-

# 2. Añade el repositorio original como remote
git remote add upstream https://github.com/Belial1993/Seguridad-ecosistemas-

# 3. Crea una rama para tu trabajo
git checkout -b feature/descripcion-tu-cambio
```

---

## 🔐 Reportar Vulnerabilidades

### ⚠️ IMPORTANTE: No reportes vulnerabilidades públicamente

Las vulnerabilidades de seguridad son **críticas**. No abras un issue público.

### Reportar Vulnerabilidad Responsablemente

1. Envía un correo a: `[email por definir]`
2. Incluye:
   - Descripción detallada del problema
   - Pasos para reproducir
   - Impacto de seguridad
   - Posible solución (opcional)

3. Espera confirmación dentro de **48 horas**
4. Trabajaremos contigo en un fix antes de publicar

---

## 🐛 Reportar Bugs

### Verificación Previa

Antes de reportar, confirma:

- [ ] Estás usando la versión más reciente
- [ ] El bug no se reportó antes
- [ ] Incluyes pasos claros para reproducir

### Crear un Reporte de Bug

Haz clic en [New Issue](../../issues/new) y selecciona **Bug Report**:

```markdown
## Descripción
[Descripción clara del bug]

## Pasos para Reproducir
1. Paso 1
2. Paso 2
3. Paso 3

## Comportamiento Esperado
[Lo que debería suceder]

## Comportamiento Actual
[Lo que sucede realmente]

## Entorno
- OS: [ej. Ubuntu 22.04]
- Versión: [ej. v1.0]
- Rama: [ej. main]

## Contexto Adicional
[Screenshots, logs, archivos relevantes]
```

---

## 💡 Sugerir Mejoras

### Crear una Sugerencia

Haz clic en [New Issue](../../issues/new) y selecciona **Feature Request**:

```markdown
## Descripción de la Mejora
[Descripción clara de la mejora propuesta]

## Problema que Resuelve
[¿Qué problema soluciona?]

## Solución Propuesta
[Tu idea de solución]

## Alternativas Consideradas
[Otras opciones evaluadas]

## Contexto Adicional
[Información relevante]
```

---

## 📤 Proceso de Pull Request

### Paso 1: Fork y Crea una Rama

```bash
# Actualiza tu fork
git fetch upstream
git checkout main
git merge upstream/main

# Crea una rama descriptiva
git checkout -b fix/issue-123-descripcion
# o
git checkout -b docs/agregar-documentacion-api
```

### Paso 2: Realiza tus Cambios

```bash
# Edita archivos
vim docs/ejemplo.md

# Verifica cambios
git status
git diff
```

### Paso 3: Commit Siguiendo Convención

```bash
git commit -m "type(scope): descripción clara"
```

Ver [Estructura de Commits](#estructura-de-commits)

### Paso 4: Push a tu Fork

```bash
git push origin fix/issue-123-descripcion
```

### Paso 5: Abre un Pull Request

1. Ve a [Pull Requests](../../pulls)
2. Haz clic en **New Pull Request**
3. Selecciona:
   - **Base**: `Belial1993/Seguridad-ecosistemas- main`
   - **Compare**: `TU_USUARIO/Seguridad-ecosistemas- tu-rama`
4. Completa el template de PR

---

## 📝 Template de Pull Request

```markdown
## Descripción
[Qué cambios incluye este PR y por qué]

## Tipo de Cambio
- [ ] 📚 Documentación
- [ ] ✨ Nueva característica
- [ ] 🐛 Bug fix
- [ ] 🚀 Performance
- [ ] 🔒 Seguridad
- [ ] ♻️ Refactoring

## Relacionado con Issue
Cierra #123

## Cambios Principales
- [ ] Cambio 1
- [ ] Cambio 2
- [ ] Cambio 3

## Checklist
- [ ] Mi código sigue el estilo del proyecto
- [ ] He actualizado la documentación
- [ ] He añadido tests relevantes
- [ ] Los tests pasan localmente
- [ ] No hay conflictos con main

## Testing
[Describe cómo testear los cambios]

## Screenshots (si aplica)
[Adjunta evidencia visual]

## Notas Adicionales
[Información relevante]
```

---

## 🎨 Guía de Estilo

### Markdown

```markdown
# Título Principal (H1)
## Subtítulo (H2)
### Sección (H3)

**Negrita** para énfasis
*Cursiva* para énfasis sutil
`código inline`

- Listas con bullets
- Dos espacios antes
- Legible

1. Listas numeradas
2. Información secuencial
3. Clara estructura
```

### Code

```python
# Python - PEP 8
def function_name(param1, param2):
    """Docstring describing function."""
    return result

class ClassName:
    """Docstring describing class."""
    def __init__(self):
        pass
```

```rust
// Rust - rustfmt
pub fn function_name(param1: Type1) -> Result<T, E> {
    /// Documentation
    Ok(value)
}
```

```go
// Go - gofmt
func functionName(param1 string) error {
    // Comment explaining logic
    return nil
}
```

### Directorios y Archivos

```
lowercase/
├── with-hyphens.md
├── not_underscores.md
├── CamelCaseForCode/
│   ├── Main.rs
│   └── Utils.go
└── README.md (siempre presente)
```

---

## 📌 Estructura de Commits

### Formato Convencional

```
type(scope): subject

body

footer
```

### Tipos Válidos

| Tipo | Descripción |
|------|------------|
| `feat` | Nueva característica |
| `fix` | Bug fix |
| `docs` | Cambios en documentación |
| `style` | Formato, sin cambios de código |
| `refactor` | Refactoring de código |
| `perf` | Mejora de performance |
| `test` | Agregar o actualizar tests |
| `chore` | Cambios en build, deps, etc. |
| `security` | Parches de seguridad |

### Ejemplos

```bash
# Característica
git commit -m "feat(auth): agregar autenticación multifactor"

# Bug fix
git commit -m "fix(gateway): corregir validación de tokens"

# Documentación
git commit -m "docs(api): actualizar especificación OpenAPI"

# Refactoring
git commit -m "refactor(core): mejorar estructura de módulos"

# Seguridad
git commit -m "security(crypto): actualizar a AES-256-GCM"
```

### Body y Footer (Opcional pero Recomendado)

```bash
git commit -m "feat(sandbox): implementar WASM runtime

- Integración completa de WebAssembly
- Validación de permisos previo a ejecución
- Aislamiento de memoria

Closes #456
BREAKING CHANGE: Cambios en API de ejecución"
```

---

## ✅ Checklist Pre-Commit

Antes de hacer push:

```bash
# 1. Actualiza con los cambios del upstream
git fetch upstream
git rebase upstream/main

# 2. Verifica tu código
git diff

# 3. Valida formato markdown
# - Sin líneas muy largas
# - Código indentado correctamente
# - Links funcionando

# 4. Commits limpios
git log --oneline origin/main..HEAD

# 5. Push
git push origin tu-rama
```

---

## 🔄 Revisión de PR

### Qué Esperamos

- Cambios claros y bien documentados
- Tests (si aplica)
- Commits bien estructurados
- Cumplimiento de estilo

### Qué Haremos

- Revisar código
- Solicitar cambios si es necesario
- Validar seguridad
- Mergear cuando esté listo

### Tiempos de Respuesta

- Documentación: **24-48 horas**
- Código: **2-5 días**
- Seguridad: **inmediata**

---

## 🚀 Tipos de Contribución

### 📚 Documentación

```
docs/
├── nuevas-secciones.md
├── mejoras-existentes.md
└── ejemplos/
    └── caso-de-uso.md
```

**Cómo empezar:**
- Identifica gaps en la documentación
- Crea un issue antes de escribir mucho
- Sigue el estilo Markdown definido
- Incluye ejemplos claros

### 💻 Código

```
reference-implementations/
├── core-kernel/
├── secure-gateway/
└── [nuevo-modulo]/
```

**Requisitos:**
- Código comentado
- Tests unitarios
- Compatibilidad con stack definido
- Seguridad como prioridad

### 🔍 Auditoría de Seguridad

```
security/
├── audits/
│   └── audit-2026-05-27.md
└── findings/
    └── issue-cve-2026-xxxxx.md
```

**Cómo reportar:**
- Usa el proceso de vulnerabilidades
- Documenta hallazgos
- Propone soluciones

### 🚀 Optimizaciones

```
performance/
├── benchmarks/
└── improvements/
```

---

## 📞 Comunidad y Soporte

- **Preguntas**: Abre una [Discussion](../../discussions)
- **Bugs**: Abre un [Issue](../../issues)
- **Seguridad**: Envía email (confidencial)
- **Reuniones**: [Próximas a definir]

---

## 📖 Recursos Útiles

- [Guía Git Flow](https://guides.github.com/introduction/flow/)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Semantic Versioning](https://semver.org/)
- [Principios de Código Limpio](https://cleancode.dev/)

---

## ⭐ Reconocimiento

Todos los contribuidores serán reconocidos en:
- Lista de contributors (README)
- Release notes
- Documentación

---

## ❓ Preguntas Frecuentes

### ¿Necesito permiso para empezar?
No, solo abre un issue o PR directamente.

### ¿Cuál es el tiempo de respuesta?
Documentación: 24-48h | Código: 2-5 días | Seguridad: inmediata

### ¿Puedo trabajar en múltiples cambios?
Sí, pero en ramas separadas. Un PR por cambio lógico.

### ¿Qué si mi PR es rechazado?
Solicita feedback y ajusta. La comunidad quiere ayudar.

---

## 🎉 Gracias

**¡Tu contribución cuenta!** Desde pequeñas correcciones hasta grandes características, todo suma.

Juntos construimos un ecosistema más seguro.

---

**Última actualización**: 2026-05-27  
**Versión**: 1.0  
**Mantenedor**: Belial1993
