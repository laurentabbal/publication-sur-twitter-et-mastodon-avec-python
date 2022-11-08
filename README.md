# Publication sur Twitter et Mastodon avec Python

`pytwidon.py` permet de publier simultanément sur Twitter et Mastodon du texte et des images. Avantage: plus besoin de passer par http://crossposter.masto.donte.com.br (ou équivalent) et donc plus besoin de partager des paramètres de connexion avec des sites tiers.

Code : https://github.com/laurentabbal/publication-sur-twitter-et-mastodon-avec-python/blob/main/pytwidon.py

Pour pouvoir utiliser `pytwidon.py`, il faut tout d'abord installer les bibliothèques et créer les clés Twitter et Mastodon. C'est un peu long mais c'est à faire qu'une fois.

## A. INSTALLATION DES BIBLIOTHÈQUES

### 1. BIBLIOTHÈQUE TWEEPY
Exécuter:
```
pip install tweepy --upgrade
```

### 2. BIBLIOTHÈQUE MASTODON.PY
Exécuter:
```
pip install mastodon.py
```

## B. CLÉS

### 1. TWITTER (à ne faire qu'une fois)
* se connecter à son compte Twitter
* ouvrir : https://developer.twitter.com/en/portal/petition/essential/basic-info
* remplir le formulaire et valider
* cocher "Accept Terms & Conditions" puis cliquer sur "Submit"
* suivre la procédure pour vérifier l'adresse courriel
* donner un nom à l'application et cliquer sur "Get keys"
* inutile de sauvegarder les clés (il faudra les générer à nouveau plus tard), cliquer directement sur "Dashboard" puis sur "Yes, I saved them" (même si vous ne l'avez pas fait)
* cliquer sur l'icone "App settings" de l'application
* dans la rubrique "User authentication settings", cliquer sur "Set up"
* sélectionner "Read and write" dans "App permissions", "WebApp, Automated App or Bot" dans "Type of App" puis, dans "App info", saisir l'adresse d'un site pour "Callback URI / Redirect URL" et "Website URL" (vous pouvez mettre n'importe quel site, même un site qui n'existe pas) 
* cliquer sur "Save" puis sur "Yes" puis sur "Done" (inutile de sauvegarder les données car elles ne serviront pas) et enfin sur "Yes, I saved it" (même si vous ne l'avez pas fait)
* cliquer sur l'onglet "Keys and token"
* pour "API Key and Secret", cliquer sur "Regenerate"
* sauvegarder les clés car elles ne seront plus accessibles ensuite (dans `pytwidon.py`, `api_key` sera votre "API Key" et `api_key_secret` sera votre "API Key Secret")
* pour "Access Token and Secret", cliquer sur "Generate"
* sauvegarder les clés car elles ne seront plus accessibles ensuite (dans `pytwidon.py`, `access_token` sera votre "Access Token" et `access_token_secret` sera votre "Access Token Secret")
* Voilà pour Twitter!


### 2. MASTODON (à ne faire qu'une fois)

Dans code ci-dessous:
* pour `mastodon_url`, indiquer l'addresse de votre instance Mastodon.
* remplacer "pytooterapp" par un nom de votre choix
* remplacer "your_mastodon_email" par l'adresse courriel utilisée pour se connecter à Mastodon
* remplacer "your_mastodon_password" par votre mot de passe Mastodon

Exécuter le code et copier le contenu de `pytooter_usercred.secret`.

Dans `pytwidon.py`, coller le contenu de `pytooter_usercred.secret` dans `mastodon_token` et compléter `mastodon_url` en indiquand l'adresse de votre instance Mastodon.

```python
from mastodon import Mastodon
mastodon_url = 'https://mastodon.social'
Mastodon.create_app(
     'pytooterapp',
     api_base_url = mastodon_url,
     to_file = 'pytooter_clientcred.secret'
)
mastodon = Mastodon(
    client_id = 'pytooter_clientcred.secret',
    api_base_url = mastodon_url
)
mastodon.log_in(
    'your_mastodon_email',
    'your_mastodon_password',
    to_file = 'pytooter_usercred.secret'
)
```
