# ActiveDierectory-Lab# Active Directory Lab: Vynilics

Laboratorio de Active Directory para una empresa ficticia, Vynilics.
El foco no es la instalación sino las decisiones de diseño, los scripts
de administración y los problemas que aparecieron en el camino.

## Por qué un dominio

En una empresa sin dominio, cada carpeta compartida se protege con una
contraseña que conocen todos los que la usan. Cuando alguien se va, hay
que cambiarla y volver a repartirla. Si se filtra, no hay forma de saber
quién entró. No hay un dueño claro de los archivos, cualquiera con
acceso puede borrar, y nada impide probar contraseñas sin límite porque
no hay política de bloqueo.

El dominio separa quién es cada persona de qué puede hacer, y centraliza
las reglas en un solo lugar.

## Entorno

- Hyper-V sobre Windows 11 Pro
- DC01: Windows Server, controlador de `ad.vynilics.com`
- CLI01: Windows 11 unido al dominio

## Estado

- [x] Nombre del dominio
- [x] Red del laboratorio
- [ ] Promoción del controlador
- [ ] Unidades organizativas y delegación
- [ ] Usuarios por script y grupos (AGDLP)
- [ ] Directivas de grupo
- [ ] Cliente unido al dominio
- [ ] Rearmado desde cero en menos de una hora

## Estructura

- `diseno/`: decisiones de diseño y su justificación
- `bitacora/`: registro de cada sesión, incluidos los errores