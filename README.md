 Piensa: ¿por qué no le pasamos al servicio web la contraseña de root de la base de datos
(env_file: .env)?
Porque la aplicación PHP solo necesita leer y escribir en la 
base de datos arcade mediante el usuario jugador y pasar la contraseña de root al contenedor web
expondría permisos de administración y control si el contenedor web se llega a ver comprometido.


MariaDB [arcade]> SHOW GRANTS;
+--------------------------------------------------------------------------------------------------------+
| Grants for jugador@%                                                                                   |
+--------------------------------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO `jugador`@`%` IDENTIFIED BY PASSWORD '*77D0467C6FCC8FA6D6E3B9D9A7564F3F12BDED14' |
| GRANT ALL PRIVILEGES ON `arcade`.* TO `jugador`@`%`                                                    |
+--------------------------------------------------------------------------------------------------------+
2 rows in set (0.000 sec)

9 | MONEDA-1: ARC-7X3K | secreto        |      0 

🪙 MONEDA 2: ARC-Q9M2
