# Enunciat:

Crea una petita aplicació que genera un directori al home de l’usuari actual anomenat URLDownloader*, on * és el teu cognom.

El programa té les següents opcions:

- Sortir: Surt del programa.

- Descarregar URL: Pregunta per una URL a l’usuari/a i la descarrega dins d’un directori de URLDownloader* anomenat com el domini de la URL.

Per exemple si l’usuari “Manel” descarrega la URL: “https://www.filmaffinity.com/es/film826914.html”, el programa crearà un fitxer anomenat:

“/home/Manel/URLDownloader*/www.filmaffinity.com/film826914.html”

Si el fitxer JA EXISTEIX, crea una copia del fitxer actual (versió vella) i descarrega el fitxer com s’ha explicat abans:

“/home/Manel/URLDownloader*/www.filmaffinity.com/film826914-OLD-1.html” és la copia vella del fitxer.

Cada vegada que es crei una còpia del fitxer s’actualitzarà el sufix OLD-1, OLD-2, OLD-3…

- Actualitzar URL: Pregunta una URL i si no està descarregada avisa a l’usuari/a, en cas d’estar descarregada sobreescriu la versió principal i esborra les versions.
