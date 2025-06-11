# ControlExcel – Registro de Visitas a Clientes

Aplicación de escritorio desarrollada en Java Swing con estructura MVC, diseñada para registrar visitas a clientes, calcular pagos automáticamente y exportar la información a Excel. Ideal como MVP para escalar posteriormente a una versión web.

---

## 🛠️ Características

- Registro de visitas con:
  - Fecha con selector de calendario
  - Horas de salida/llegada (empresa y cliente)
  - Referencia alfanumérica
- Cálculo automático de:
  - Minutos trabajados (pagos)
  - Minutos con cliente
  - Total a pagar (minutos trabajados / 60 × 9500)
- Visualización en tabla (`JTable`)
- Validación de entradas (solo números en horas, letras/números en referencia)
- Exportación a Excel con celdas bordeadas (Apache POI)
- Búsqueda por fecha
- Prevención de duplicados

---

## 🧱 Tecnologías utilizadas

- Java 17+
- Java Swing
- Apache POI
- SQLite
- Maven

---

## 📦 Estructura del proyecto (MVC)

src
└── main
    ├── java
    │   └── com.miempresa.controlexcel
    │       ├── model
    │       │   ├── VisitRecord.java         ← Modelo con los campos de cada visita
    │       │   ├── VisitService.java        ← Lógica de negocio: cálculo de tiempo y pago
    │       │   └── ExcelExporter.java       ← Clase que exporta a Excel
    │       │
    │       ├── view
    │       │   └── MainView.java            ← Interfaz Swing (ya la tienes)
    │       │
    │       ├── controller
    │       │   └── MainController.java      ← Controla acciones de botones, conecta vista y modelo
    │       │
    │       └── App.java                     ← Clase con el método main que lanza la app
    │
    └── resources                            ← Espacio para íconos, fuentes, archivos de configuración

    ## 🚀 Instalación y ejecución

1. Clona el repositorio:

git clone https://github.com/tuusuario/controlexcel.git
cd controlexcel

2. Ejecuta el proyecto desde tu IDE favorito (IntelliJ, Eclipse, NetBeans) o por línea de comandos con Maven:
   mvn clean install
   
3. Ejecuta la clase App.java.

📝 Cómo usar
Inicia la app.
1. Llena los campos con la información requerida.
2. Pulsa Guardar para registrar una nueva visita.
3. Usa Buscar para filtrar por fecha.
4. Exporta a Excel con el botón correspondiente.

💡 Futuras mejoras
Versión web con Spring Boot y frontend moderno.
Generación de PDF.
Autenticación de usuarios.
Dashboard de reportes.

🤝 Contribuciones
¡Contribuciones son bienvenidas! Si deseas colaborar, crea un fork, haz tus cambios y abre un Pull Request.
   
