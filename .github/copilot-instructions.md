# Copilot Workspace Instructions

## Objetivo del proyecto

Soc Ops es una app de Bingo Social en Blazor WebAssembly (.NET 10). Prioriza cambios pequenos, claros y alineados con la experiencia de juego.

## Flujo rapido

Comandos base:

```bash
dotnet --version
dotnet build SocOps/SocOps.csproj
dotnet run --project SocOps/SocOps.csproj
```

Usa la URL que indique Kestrel (normalmente `http://localhost:5166`).

## Checklist de desarrollo

Antes de abrir PR o cerrar tarea:

- [ ] Verificar .NET 10 SDK disponible
- [ ] Ejecutar `dotnet build SocOps/SocOps.csproj` sin errores
- [ ] Ejecutar `dotnet run --project SocOps/SocOps.csproj` y validar arranque
- [ ] Probar flujo impactado en UI
- [ ] Limitar cambios al requerimiento
- [ ] Evitar dependencias nuevas salvo necesidad real

## Mapa del proyecto

- `SocOps/Components/`: UI
- `SocOps/Services/`: logica y estado
- `SocOps/Models/`: modelos de dominio
- `SocOps/Data/Questions.cs`: preguntas
- `SocOps/wwwroot/css/app.css`: utilidades CSS

## Reglas de implementacion

- Preferir nombres claros en C# y mantener convenciones de .NET (PascalCase para miembros publicos).
- En Razor, mantener markup simple y mover logica a `Services`.
- Reutilizar utilidades CSS existentes antes de crear nuevas clases.
- Mantener accesibilidad basica: botones con texto claro y estados visibles.

## UI y seguridad de cambios

- Seguir `.github/instructions/frontend-design.instructions.md` y `.github/instructions/css-utilities.instructions.md`.
- No eliminar funcionalidades existentes sin solicitud explicita.
- Si hay conflicto de puerto, identificar proceso activo y proponer puerto alterno simple.