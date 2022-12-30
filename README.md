# ACTIVE DIRECTORY 2019 (UDEMY)
## Aaron Andal

https://www.udemy.com/course/windows-server-2019-active-directory/learn/lecture/22395454#search

https://geekland.eu/aprender-markdown-en-minutos/ 

#### ACTIVE DIRECTORY 2019 (Repaso)

1. Instalado en Virtualbox desde 0 tanto Windows Server 2019 y Windows 10 para cliente.
2. Configuradas adaptadores de red (Adaptador puente y Red Interna). 
3. Instalado el Active Directory y configurar el DNS.
4. Creación de una OU (Organizational Unit) = Unidad Organizativa.
5. Creación de OU Administración - Ventas.
6. Creación de Usuarios dentro de las respectivas OU. La contraseña debe cumplir con los requisitos de complejidad.
7. Agregar Equipos al dominio.
8. Configurar el cliente con su adaptador de red (Red Interna) para que tenga una IP dentro del rango del Servidor.
9. Prueba de conectividad Cliente - Servidor.
10. Añadir equipo Cliente al Dominio MINEGOCIO.LOCAL.
11. Iniciar como Adminstrador en el equipo Cliente.
12. Eliminar usuario admin local del Cliente desde Admin de Dominio.
13. Crear usuario temporal en la OU de Ventas.
14. Establecer contraseña con complejidad personalizada.
15. Creación de grupos.
16. Vinculación del permiso de "Contraseñas sin complejidad" al grupo recién creado.
17. Se vincularán los usuarios que pertenezcan a ese grupo.
18. Habilitación de Papelera de Reciclaje.
19. Crear usuarios a través de PowerShell. `New-ADUser -name 'Julio Inglesias' -SamAccountName julio.inglesias -UserPrincipalName julio.inglesias@minegocio.local -Path "OU=Usuarios,OU=Ventas,DC=minegocio,DC=local" -AccountPassword (ConvertTo-SecureString -AsPlainText 'Password123' -force) -Enabled $true
`
20. Crear usuarios a través de un fichero CSV. `Import-Csv -Path C:\UserAd.csv | ForEach-Object {New-ADUser -name $_.nombre -DisplayName $_.nombre -SamAccountName $_.cuenta -UserPrincipalName $_.email -Path $_.ou -AccountPassword (ConvertTo-SecureString -AsPlainText 'Password123' -force) -Enabled $true -ChangePasswordAtLogon $true}
`
21. Personalización horaria para cada usuario. Usuario puede iniciar sesión.
[]!

