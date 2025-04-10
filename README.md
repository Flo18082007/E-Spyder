
# **📧E-Spyder : Votre Détective d'Emails OSINT 🕵**
👋Bonjour ! Pour toute demande professionnelle ou collaboration, veuillez me contacter à l'adresse suivante :
gggy068@protonmail.com

![E-SPIDER logo](src/img/spider.png)


![PyPI](https://img.shields.io/pypi/v/holehe) ![PyPI - Week](https://img.shields.io/pypi/dw/holehe) ![PyPI - Downloads](https://static.pepy.tech/badge/holehe) ![PyPI - License](https://img.shields.io/pypi/l/holehe)

# [E-Spyder Online Version](https://osint.industries/)

## **Sommaire**

*Trouver efficacement les comptes enregistrés à partir d'e-mails*

E-Spyder vérifie si un e-mail est associé à un compte sur tous les sites web prometteur.

+ Récupère des informations en utilisant la fonction de mot de passe oublié..
+ **[Obfuscation de requete cible .](https://github.com/megadose/holehe/issues/12)**
+ **Utilisation : [Python 3](https://www.python.org/downloads/release/python-370/).**
+ 
## 🛠️ Installation

### 🔵 PyPI

```pip3 install E-Spyder```

### 🔵  Github

```bash
git clone
cd E-Spider/
python3 config.py install
```

### 🔵 Docker

```bash
docker build . -t E-Spyder-image
docker run E-Spyder-image E-Spyder test@gmail.com
```

## Rapidité d'execution 

E-Spider peut se lancer directement depuis le shell ou integré 
dans un autre script .

### 📚 CLI Exemple

```bash
E-Spider test@gmail.com
```
### 📈 Python Exemple

```python
import trio
import httpx

from E-spider.modules.social_media.snapchat import snapchat


async def main():
    email = "test@gmail.com"
    out = []
    client = httpx.AsyncClient()

    await snapchat(email, client, out)

    print(out)
    await client.aclose()

trio.run(main)
```
## Module De Sortie 

Pour chaque module en sortie , il est directemnt classé sous format json comme si dessous : 
```json
{
  "name": "example",
  "rateLimit": false,
  "exists": true,
  "emailrecovery": "ex****e@gmail.com",
  "phoneNumber": "0*******78",
  "others": null
}
```

- Spider Web : Cela siginie que vous avez été limité par le service.
- Spider : Spider trouvé .
- Ghost Spider : Les spiders peuvents etres hasher ou invalide.
- Phone Spider  :  Parfois, des numéros de téléphone de récupération partiellement masqués sont retournés.
- Craezy Spider : information subtiles 


Spider Web = Altération IP

