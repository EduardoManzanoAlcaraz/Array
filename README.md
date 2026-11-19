# Array — máquina de fichas en consola

Ejercicio Java con una cuadrícula 3×3 de símbolos aleatorios. Empieza con 100 fichas virtuales, cada giro cuesta 10 y se premia la primera fila coincidente; no hay pagos ni persistencia. El nombre del repositorio no describe toda su función.

## Código y ejecución

`Main.java` contiene el bucle de consola. `Tragaperras.java` declara la clase no pública `SlotMachine`, con generación, impresión y premios. Usa solo la biblioteca estándar; no hay Maven/Gradle ni dependencias externas. El código utiliza APIs disponibles en Java 8; necesitas un **JDK con `javac`**, no solo un JRE.

Desde la raíz, en PowerShell:

```powershell
New-Item -ItemType Directory -Force .build
javac -encoding UTF-8 -d .build Main.java Tragaperras.java
java -cp .build Main
```

ENTER gira; `q` o `Q` sale. No añadas `.build/` ni `.class` a los commits.

## Estado y siguientes pasos

Revisión del 2026-11-19 sobre `77fbe906102dc0e4f203856e31ab6cd2d31925ff`. Las observaciones del código se distinguen de las pruebas ejecutadas y de los informes históricos. Esta revisión solo modifica documentación.

Se leyeron ambos archivos; no hay suite de pruebas, CI ni manifiesto de compilación. No se compiló ni ejecutó: el entorno revisado dispone de JRE 8 pero no de `javac` localizado. Los comandos anteriores se deducen del código, no se declaran ejecutados.

El jackpot usa `nextInt(500)+100`: devuelve **100–599**, aunque un comentario del código diga 600. El generador no ofrece semilla configurable y el bucle no trata explícitamente EOF; la entrada usa `System.in.read/available`. Próximos pasos propuestos: compilar con un JDK, comprobar salida y giro manualmente, y después abordar entrada/EOF y pruebas deterministas en un cambio funcional aparte.

[Instrucciones para agentes](AGENTS.md).
