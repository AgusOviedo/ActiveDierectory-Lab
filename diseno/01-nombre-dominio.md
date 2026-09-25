# Nombre del dominio

`ad.Vynilics.com`

Empezamos poniendo un subdominio y no el dominio público directo. Si el dominio interno
se llamara igual que el público, el controlador pasaría a ser la
autoridad de ese nombre para toda la red, y lo que la empresa publique
afuera (web, correo, sistemas de terceros) dejaría de resolver desde
adentro salvo que se cargue a mano y tenga un mantenimiento recurrente.

Tampoco uso `.local`: no existe en internet, nadie puede demostrar que
le pertenece, y eso complica la integración con servicios en la nube.

Con el subdominio, el nombre de inicio de sesión puede coincidir con la
dirección de correo cuando se integre con Microsoft 365.
