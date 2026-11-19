# Instrucciones para agentes — Array

Se aplica a todo el repositorio. Codex debe leer este archivo; con Claude u otra herramienta, incluirlo explícitamente si no lo carga automáticamente.

## Antes de cambiar archivos

Lee `README.md`, `Main.java` y `Tragaperras.java` completos; son los dos únicos archivos de código.

Comprueba `git status --short` y la rama. Conserva cambios ajenos y lee las instrucciones de cualquier subdirectorio afectado. Contrasta los documentos con el código: un plan o resultado antiguo no demuestra una función actual. Limita cada cambio al encargo recibido.

## Reglas del proyecto

- No renombres `Tragaperras.java` suponiendo que su clase es pública: declara `SlotMachine` con visibilidad de paquete.
- Conserva fichas virtuales, coste y primera fila ganadora salvo encargo de cambiar reglas. El jackpot real es 100–599.
- No añadas frameworks, pagos, servicios ni una reestructuración Maven/Gradle para documentar este ejercicio.
- Trata los problemas de EOF, aleatoriedad y buffer como limitaciones; no los corrijas incidentalmente en una tarea documental.

## Validación y entrega

Con JDK: compila explícitamente ambos archivos y ejecuta `Main` con los comandos del README. Comprueba q/Q y un giro en una sesión controlada. No ejecutes el bucle con entrada cerrada para simular una prueba de salida: EOF no está gestionado. No hay comando de tests existente; no inventes `npm test` ni `mvn test`. Mantén `.class` y `.build/` fuera del commit.

En cambios solo de documentación, comprueba rutas, enlaces relativos y comandos contra los archivos reales; no hace falta repetir toda la suite si no cambia el comportamiento. No inventes pruebas ausentes ni marques como aprobado un comando que no ejecutaste. Informa comando, resultado y alcance pendiente.

Revisa el diff antes de hacer commit. No incluyas dependencias instaladas, archivos generados, datos personales, credenciales, cookies, tokens ni archivos de entorno privados. Mantén los documentos útiles existentes y actualiza el estado si cambia una decisión o una limitación. Los commits deben explicar el resultado y su validación; separa documentación y cambios funcionales.
