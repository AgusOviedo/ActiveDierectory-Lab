# Red del laboratorio

Hyper-V con un switch interno propio (`LabNAT`) y NAT en el host.
Red 192.168.50.0/24.

- No uso el switch externo: conecta las VMs a la red de casa, y el
  controlador terminaría respondiendo DNS en la misma red que el resto
  de los dispositivos.
- No uso la Default Switch: su subred puede cambiar al reiniciar el
  host, lo que rompe las IPs fijas.
- Switch interno más NAT: red aislada de la casa y con salida a internet.

| Equipo         | IP             | DNS            |
|----------------|----------------|----------------|
| Host (gateway) | 192.168.50.1   | n/a            |
| DC01           | 192.168.50.10  | sí mismo       |
| CLI01          | 192.168.50.20  | 192.168.50.10  |

Sin DNS alternativo en ningún equipo: un equipo de dominio debe resolver
solo contra el controlador. Un DNS público como secundario provoca
fallas intermitentes al buscar el dominio.