# Connectar Python amb MariaDB:

Després de seguir el tutorial d'instal·lació de MariaDB provarem a crear un programa que permeti:

1. Inserir a la bbdd equips de futbol amb l'estructura de taula:

![image](https://user-images.githubusercontent.com/110727546/204524608-4f06986f-3e9a-41ec-b61f-5636faa5dddb.png)

2. Inserir a la bbdd jugadors amb l'estructura de taula:

![image](https://user-images.githubusercontent.com/110727546/204526899-659956c8-3fa5-4214-b8d8-95305638a571.png)

On la posició serà un tipus de dades [ENUM de MariaDB](https://mariadb.com/kb/en/enum/) que podrà tenir els valors:

- Portero.
- Defensa central.
- Lateral izquierdo.
- Lateral derecho.
- Pivote.
- Mediocentro.
- Extremo izquierdo.
- Extremo derecho.
- Delantero centro.

Podeu consultar dades de jugadors [aquí](https://www.transfermarkt.es/cd-teruel/startseite/verein/19301).

Cada jugador haurà de ser d'un equip de la BBDD seguint les restriccions:

![image](https://user-images.githubusercontent.com/110727546/204527160-6b1186f2-eef1-4b18-aee0-f0014f856dd6.png)


