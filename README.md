Proyecto de Automatización E2E - SauceDemo (NTT DATA)
Este proyecto contiene pruebas automatizadas para el portal SauceDemo, utilizando el framework Serenity BDD con Cucumber y el patrón de diseño Screenplay.

Requisitos Previos
Java JDK 17 o superior.

Apache Maven 3.8+.

Google Chrome (Actualizado).

Pasos para la Ejecución
Para ejecutar las pruebas y asegurar que las librerías se carguen correctamente, sigue estas instrucciones desde tu IDE (IntelliJ) o terminal:

Limpiar el proyecto: Ejecuta el comando clean para eliminar reportes previos y carpetas temporales.

Bash
mvn clean
Ejecutar las pruebas: Usa el comando verify. Esto abrirá el navegador, ejecutará los escenarios de login.feature y realizará las validaciones correspondientes.

Bash
mvn verify
Nota: Si prefieres usar la interfaz de IntelliJ, ve al panel de Maven > Lifecycle y haz doble clic en verify.

Generar el reporte consolidado: Una vez finalizada la ejecución, genera el reporte visual de Serenity con el siguiente comando:

Bash
mvn serenity:aggregate

Ubicación de los Reportes
Tras ejecutar el comando aggregate, los resultados detallados (incluyendo pasos y capturas de pantalla) se encuentran en la siguiente ruta local:

target/site/serenity/index.html

Cómo ver el reporte:
Navega hasta la carpeta target/site/serenity/ en el explorador de archivos.

Haz clic derecho sobre el archivo index.html.

Selecciona "Open in Browser" (Chrome/Edge).

Estructura del Proyecto
src/test/resources/features: Contiene los archivos .feature (Gherkin).

src/test/java/co/com/nttdata/ui/runners: Contiene la clase CucumberTestSuite para disparar las pruebas.

src/test/java/co/com/nttdata/ui/stepdefinitions: Contiene la implementación de los pasos de Cucumber.

src/test/resources/serenity.conf: Archivo de configuración del WebDriver y Serenity.
