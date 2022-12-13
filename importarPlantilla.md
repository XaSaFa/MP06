Extreieu la informació dels jugadors.

```
import urllib.parse
import urllib.request
import xml.etree.ElementTree as ET


def descarregaWeb():
    url = 'https://www.transfermarkt.es/cd-teruel/kader/verein/19301/saison_id/2022/plus/1'
    user_agent = 'Mozilla/5.0 (Windows NT 6.1; Win64; x64)'
    headers = {'User-Agent': user_agent}

    req = urllib.request.Request(url, None, headers)
    with urllib.request.urlopen(req) as response:
        resposta = response.read().decode("utf-8")
    
    fitxer = open("jugadors.html", "wt", encoding="utf-8")
    fitxer.write(resposta)
    fitxer.close()


def llegirFitxer():
    fitxer = open("jugadors.html", "rt", encoding="utf-8")
    html = fitxer.read()
    fitxer.close()

    inici = html.find('<table class="items">')
    final = html.find('<div class="keys"')
    taula = html[inici:final]

    taula = taula.replace('class=rn_nummer', 'class="rn_nummer"')
    taula = taula.replace('&nbsp;', '')

    fitxer = open("taula.xml", "wt", encoding="utf-8")
    fitxer.write(taula)
    fitxer.close()


def carregarXML():
    tree = ET.parse("taula.xml")
    root = tree.getroot()
    # Numeros:
    for tr in root.iter('tbody'):
        for td in tr.iter('td'):
            for div in td.iter('div'):
                print(div.text)


descarregaWeb()
llegirFitxer()
carregarXML()
```
