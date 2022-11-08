# Publication sur Twitter et Mastodon avec Python

`pytwidon.py` permet de publier simultanément sur Twitter et Mastodon du texte et des images. Avantage: plus besoin de passer par http://crossposter.masto.donte.com.br (ou équivalent) et donc plus besoin de partager des paramètres de connexion avec des sites tiers.

Code : https://github.com/laurentabbal/publication-sur-twitter-et-mastodon-avec-python/blob/main/pytwidon.py

Pour pouvoir utiliser `pytwidon.py`, il faut tout d'abord créer les clés Twitter et Mastodon. A ne faire qu'une fois.

### CLÉS TWITTER
* se connecter à son compte Twitter
* ouvrir : https://developer.twitter.com/en/portal/petition/essential/basic-info
* remplir le formulaire et valider
* accepter les termes et conditions
* suivre la procédure pour vérifier l'adresse courriel
* donner un nom à l'application et valider
* ATTENTION : sauvegarder les clés car elles ne seront plus accessibles ensuite
* "API Key" sera votre `api_key` et "API Key Secret" sera votre `api_key_secret`
* Générer ensuite les "Access Token and Secret. "Access Token" sera votre `access_token` et "Access Token Secret" sera votre `access_token_secret`
* Enfin, "Bearer Token" sera votre `bearer_token`
* Voilà pour Twitter!


### CLÉS MASTODON

