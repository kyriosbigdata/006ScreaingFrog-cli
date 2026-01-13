# CONCEPTO GENERAL: Screaming Frog en una VM de Google Cloud

1. ¿Qué significa usar Screaming Frog en una VM?

- Una VM es una computadora en la nube que siempre está encendida.
- Screaming Frog se puede usar en “modo terminal” (CLI), sin interfaz gráfica.
- En una VM solo necesitamos el modo CLI para automatizar procesos SEO.

2. ¿Qué hace Screaming Frog desde terminal (CLI)?

- Rastrea un sitio web completo.
- Exporta archivos CSV con información SEO (internal, status codes, redirects, titles, etc.).
- Guarda automáticamente los resultados en carpetas.
- Funciona sin abrir ninguna ventana.

3. Estructura general dentro de la VM

/home/ubuntu/screamingfrog/
    ├── config/        → Configuraciones (opcional)
    ├── lists/         → Listas de URLs (opcional)
    ├── results/       → CSV generados por cada rastreo
    └── scripts/       → Scripts que luego usaremos para automatizar

(Esto es solo conceptual, todavía no se crea.)

4. ¿Cómo se ejecuta un rastreo (concepto general)?

Ejemplo de comando:

ScreamingFrogSEOSpiderCli --crawl https://www.sitio.com --headless --output-folder ./results

Este comando:
- Inicia el rastreo sin abrir interfaz gráfica.
- Exporta automáticamente los reportes en CSV.
- Guarda todo en la carpeta indicada.

5. ¿Qué genera un rastreo?

Archivos CSV como:
- Internal_All.csv
- Response_Codes.csv
- Redirects.csv
- Page_Titles.csv
- Entre otros

Estos son los que después se pueden conectar con BigQuery.

6. ¿Por qué es útil hacerlo en una VM?

- La VM está siempre activa.
- No depende de tu laptop.
- Puede ejecutar rastreos programados.
- Puede manejar cargas grandes.
- Permite automatización total (cron, scripts, BigQuery, etc.)

FIN — Esto es solo la explicación general. No se ha instalado nada todavía.
