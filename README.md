# Admin Suite

## Descripción general:
AdminSuite es un conjunto de scripts en Bash que automatiza tareas comunes de administración en sistemas de Linux.
Permite gestionar usuarios y grupos, realizar respaldos programados, instalar la aplicacion web WordPress con Docker, consultar logs, monitorear la red y obtener información del sistema.

## Estructura del proyecto:
```
adminsuitex/
├── scripts/
│   └── principal.sh
│   └── red.sh
│   └── usuarios_grupos.sh
│   └── respaldos.sh
│   └── ayuda.sh
│   └── logs_reportes.sh
│   └── sistema.sh
│   └── aplicacion_web.sh
│
├── backups/
│   └── app/
│   └── diario/
│
└── reportes/
    ├── usuarios_grupos/
    └── red/
```
## Entorno de pruebas:
El script fue desarrollado y testeado en CentOS 7.

## Requisitos previos:
- Distribución Linux (CentOS 7+, Rocky, Alma, u otras distribuciones basadas en Red Hat).
- Acceso administrativo (sudo).
- Dependencias: docker, nmap, tar, cron, systemctl, journalctl (algunos los instala el script).
- Carpeta /adminsuitex/ en el directorio raíz con permisos adecuados.

## Instalación:
1. Copiar la carpeta adminsuitex a /.
2. Dar permisos de ejecución:
-- chmod +x principal.sh *.sh
3. Ejecutar el menú principal:
-- bash principal.sh


## Uso básico:
- El menú principal muestra las partes principales del sistema.
- Cada submenú hace tareas específicas y guarda un registro de lo que se hizo en /var/log/adminsuite.log.

## Seguridad y buenas prácticas:
- No guardar contraseñas dentro de los scripts.
- Ejecutar siempre con permisos mínimos.
- Revisar el log /var/log/adminsuite.log para el registro de la actividad.
- Verificar la existencia de respaldos antes de restaurar.
- Usar Docker y cron de forma controlada.

## Credenciales de la VM:
- Usuario: root
- Contraseña: abc123
