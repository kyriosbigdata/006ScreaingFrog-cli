# Paso 1
# verificación de Screaming frog
screamingfrogseospider --help

# Paso2
# Crear la estructura base del proyecto CLI
mkdir -p $HOME/sf-cli/{config,crawls,exports,logs,scripts,tmp}

# Verificar que las carpetas se crearon
ls -R $HOME/sf-cli

# Paso 3 Ejecutar un crawl sencillo en CLI
screamingfrogseospider \
  --crawl "https://www.pharmacys.com.ec/" \
  --headless \
  --save-crawl \
  --output-folder "$HOME/sf-cli/crawls" \
  --timestamped-output

# Revisemos el resultado
ls $HOME/sf-cli/crawls

# Ingresemos en esa carpeta
cd $HOME/sf-cli/crawls/2025.11.19.17.43.39

# Podemos ver el contenido
ls -la

# Podemos abril la carpeta mas reciente
cd $(ls -td $HOME/sf-cli/crawls/* | head -1)

