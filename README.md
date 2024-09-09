# Guía para Usar Nikto en Kali Linux

Nikto es una herramienta de escaneo de seguridad para servidores web que ayuda a identificar vulnerabilidades y problemas de configuración. A continuación, te presento una guía detallada para instalar y usar Nikto en Kali Linux.

## Instalación de Nikto

Nikto suele estar preinstalado en Kali Linux. Para verificar si está instalado y ver la versión, usa el siguiente comando:
```bash
nikto -Version
```

Si Nikto no está instalado, puedes instalarlo utilizando `apt`:
```bash
sudo apt update sudo apt install nikto
```


## Uso Básico de Nikto

Para realizar un escaneo básico en un servidor web, usa el siguiente comando:
```bash
nikto -h http://example.com
```
Reemplaza `http://example.com` con la URL del servidor web que deseas escanear.

## Opciones Comunes

Nikto ofrece varias opciones que puedes utilizar para personalizar tus escaneos:

- `-h`: Especifica el objetivo del escaneo. Debe incluir el protocolo (http o https).
- `-p`: Permite especificar un puerto. Por ejemplo, `-p 8080` para el puerto 8080.
- `-Tuning`: Ajusta el nivel de escaneo. Los valores varían desde 1 (escaneo rápido) hasta 6 (escaneo exhaustivo).
- `-o`: Especifica el archivo de salida para guardar los resultados del escaneo.

### Ejemplo con Opciones

Para escanear un servidor en el puerto 8080 y guardar los resultados en un archivo:
```bash
nikto -h http://example.com -p 8080 -o resultados.txt
```

## Mensaje de Deslinde de Responsabilidad

**Nota:** Usa Nikto de manera ética y solo en servidores para los cuales tengas permiso explícito para realizar auditorías. El uso no autorizado de herramientas de escaneo puede ser ilegal y tener consecuencias graves.

