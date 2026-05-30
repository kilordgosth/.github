# .github — Shared Security Workflows

Workflows de seguridad reutilizables.

## 🛡️ security-scan.yml

### Herramientas incluidas
| Herramienta | Función | Lenguajes |
|---|---|---|
| Gitleaks | Secretos hardcodeados | Todos |
| Bandit | SAST profundo | Python |
| Semgrep | SAST multi-lenguaje | 40+ lenguajes |
| Trivy | CVEs en dependencias | Todos |
| CodeQL | Flujo de datos (público) | Python, JS, Java, PHP |
| License Check | Verificar LICENSE | Todos |

### Cómo usarlo en otro repositorio

```yaml
jobs:
  security:
    uses: kilordgosth/.github/.github/workflows/security-scan.yml@main
    with:
      lenguaje: 'todos'
      debug: false
    secrets: inherit
```

### Disparadores
- ⏰ Diario a las 9am Colombia
- 🔀 En cada push a main/master
- 🖱️ Manual con selector de lenguaje y debug
- 📞 Llamado desde otros workflows