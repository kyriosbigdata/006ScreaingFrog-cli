# MAPA GENERAL DEL PROYECTO — Screaming Frog + VM + BigQuery

## FASE 1 — VM + Screaming Frog CLI
Objetivo: Tener un motor SEO automático dentro de una VM Ubuntu.

Incluye:
1. Instalar Screaming Frog en Ubuntu.
2. Crear estructura de carpetas en la VM.
3. Probar un rastreo manual con ScreamingFrogSEOSpiderCli.
4. Crear un script para ejecutar el comando automáticamente.
5. Configurar un cron en Ubuntu para correr el script en horarios fijos.
6. Guardar los archivos CSV en la VM.

---

## FASE 2 — Google Cloud Storage (GCS)
Objetivo: Sube los archivos generados por Screaming Frog a un bucket.

Incluye:
1. Crear un bucket en GCS.
2. Diseñar la estructura por fechas:
   gs://mi-bucket/screamingfrog/YYYY-MM-DD/
3. Subir los resultados desde la VM al bucket.
4. Mantener versiones históricas.
5. Opcional: Comprimir archivos grandes.

---

## FASE 3 — Tablas externas en BigQuery
Objetivo: BigQuery leerá directamente los CSV del bucket sin cargarlos manualmente.

Incluye:
1. Crear un dataset en BigQuery.
2. Crear una tabla externa apuntando al bucket.
3. Definir el esquema de columnas.
4. Probar queries para verificar lectura de datos.
5. Confirmar que los nuevos CSV se reflejan automáticamente.

---

## FASE 4 — Comparaciones históricas y análisis
Objetivo: Construir análisis SEO a lo largo del tiempo.

Incluye:
1. Comparar status codes día vs día.
2. Detectar URLs nuevas.
3. Detectar URLs que desaparecen.
4. Ver cambios en titles/descriptions.
5. Crear dashboards con Looker Studio.

---

## FASE 5 — Automatización avanzada (opcional)
Objetivo: Hacer el sistema más robusto y crear alertas automáticas.

Incluye:
1. Alertas automáticas si aparecen 404 críticos.
2. Alertas por cambios masivos en el sitio.
3. Integración con Slack o correo.
4. Migrar a Cloud Run o Cloud Functions para mayor escalabilidad.

---

# NOTA
La FASE 1 (VM + Screaming Frog CLI) será la primera que construiremos paso a paso en la siguiente conversación técnica.
