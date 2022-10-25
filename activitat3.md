# Podcast addiction

## Antecedents:

A dia d'avui tothom té un podcast i vosaltres voleu estar "al loro" de les últimes novetats en el món del podcasting, per això heu decidit **CREAR UN PORTAL** on es vegin les últimes novetats dels vostres podcasts favorits.

Aquest programa està dividit en dues parts:

### Com funciona un RSS:

Un [RSS]((https://en.wikipedia.org/wiki/RSS) és un format de creació de metainformació i difusió de contingut en format XML.

Quan analitzem el feed d'una RSS veiem que es tracta d'informació sobre QUI genera el contingut i informació del contingut.

**Exemple de feed:** [MSDOS.CLUB](https://msdos.club/podfeed/feed.xml).

Podem observar que la metainformació de qui crea el contingut està al principi del fitxer:

```
<title>MS-DOS CLUB</title>
<link>https://msdos.club</link>
<description> MS-DOS CLUB - El Club de los obsoletos pero orgullosos. </description>
<language>es</language>
<lastBuildDate>Mon, 10 Oct 2022 08:20:00 +0200</lastBuildDate>
<itunes:subtitle> MS-DOS, Aplicaciones, Videojuegos, Virus, Hardware, entrevistas. </itunes:subtitle>
<itunes:author>A.C.H.U.S.</itunes:author>
<itunes:summary> Este es el club de los usuarios antiguos y nuevos de un sistema operativo que ya no es comercial, pero sigue estando entre nosotros. El MS-DOS Club acepta a miembros de cualquier sexo, raza, religión y credo, siempre que tengan una unidad de 3 y medio donde meter el diskette del programa. </itunes:summary>
<itunes:explicit>no</itunes:explicit>
<itunes:type>episodic</itunes:type>
<itunes:category text="Technology"/>
<itunes:image href="https://msdos.club/wp-content/uploads/2021/03/DOSCLBLOGO.jpg"/>
<itunes:owner>
<itunes:email>hola@msdos.club</itunes:email>
</itunes:owner>
<itunes:keywords> MS-DOS, Aplicaciones, Videojuegos, Virus, Hardware </itunes:keywords>
```

Mentre que cada podcast està dintre d'un tag <item>:
  
```
<item>
<title>Floppy 40 – Programando en DIV Games Studio con Tizo.</title>
<link>https://msdos.club/floppy-40-programando-en-div-games-studio-con-tizo/</link>
<description>
Floppy 40 – Programando en DIV Games Studio con Tizo.
Si te gusta nuestro contenido recuerda apoyarnos con una recomendación o echando una mano con los gastos del server 😉

En el podcast anterior hablamos con el creador del engine de desarrollo de videojuegos para DOS DIV Games Studio, Dani Navarro.

Vamos a seguir hablando de este engine con una de las personas que participó en el proyecto de Dani Navarro y Digital Dreams Multimedia, Tizo.

Tizo se encargó de programar juegos de ejemplo y por encargo para clientes en la plataforma, además de escribir artículos en la revista oficial de DIV y participar en el libro de programación Programación avanzada en DIV.

Además nos contará cómo estuvo en uno de los trabajos del mundo BETATESTER para los Hermanos Ruiz en FX Interactive.

¡Esperamos que os guste!

Agradecimientos:

Tizo (@tiotizo): Página web de Tizo. Por concedernos la entrevista. 

Javier Sancho (@kalzakath1): Por grabar y editar la entrevista.
</description>
<pubDate>Tue, 18 Oct 2022 10:00:00 +0200</pubDate>
<guid>https://msdos.club/floppy-40-programando-en-div-games-studio-con-tizo/</guid>
<enclosure length="48775000" type="audio/mpeg" url="https://msdos.club/episodios/floppy40.mp3"/>
<itunes:summary>
Floppy 40 – Programando en DIV Games Studio con Tizo.
Si te gusta nuestro contenido recuerda apoyarnos con una recomendación o echando una mano con los gastos del server 😉

En el podcast anterior hablamos con el creador del engine de desarrollo de videojuegos para DOS DIV Games Studio, Dani Navarro.

Vamos a seguir hablando de este engine con una de las personas que participó en el proyecto de Dani Navarro y Digital Dreams Multimedia, Tizo.

Tizo se encargó de programar juegos de ejemplo y por encargo para clientes en la plataforma, además de escribir artículos en la revista oficial de DIV y participar en el libro de programación Programación avanzada en DIV.

Además nos contará cómo estuvo en uno de los trabajos del mundo BETATESTER para los Hermanos Ruiz en FX Interactive.

¡Esperamos que os guste!

Agradecimientos:

Tizo (@tiotizo): Página web de Tizo. Por concedernos la entrevista. 

Javier Sancho (@kalzakath1): Por grabar y editar la entrevista.
</itunes:summary>
<itunes:explicit>yes</itunes:explicit>
<itunes:episodeType>full</itunes:episodeType>
<itunes:image href="https://msdos.club/wp-content/uploads/floppy40.jpg"/>
<itunes:duration>00:52:01</itunes:duration>
</item>
```

## Enunciat:

Aquesta pràctica es divideix en dues parts:

### Part 1 - Gestió de feeds:

En aquesta part creareu un programa que simplement ens deixa editar un fitxer anomenat feeds.txt.

En aquest fitxer guardarem a cada línia un feed d'un podcast que ens agradi:

Si no sabeu per on començar busqueu els feeds de:

- Programar es una mierda.
- La Ruina.
- Podcast República Web.

El programa us deixarà:

- Afegir un feed.
- Eliminar un feed.
- Llistar els feeds.

### Part 2 - Generació de Web de podcasts nous:

Per fer aquesta part necessitareu almenys 10 feeds al fitxer de l'apartat anterior.

Fareu un programa que crearà una pàgina web amb els últims n capítols de tots els podcasts ordenats per data de publicació dels capítols, on n serà un paràmetre subministrat per l'usuari/a.

Aquesta web mostrarà informació rellevant de cada podcast:

- Nom del Creador del podcast amb link a la seva web ```<title>``` i ```<link>```.
- Logo del podcast ```<itunes:image>```.

- Nom de l'episodi ```<title>``` amb link a la web del capítol ```<guid>``` o ```<link>```.
- Duració ```<itunes:duration>```.
- Portada de l'episodi ```<itunes:image>```.
- Descripció ```<description>``` o ```<itunes:summary>```.
- Opció de descarregar el fitxer del podcast ```<enclosure url>```.
