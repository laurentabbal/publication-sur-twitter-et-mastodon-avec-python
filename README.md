# Publication sur Twitter et Mastodon avec Python

`pytwidon.py` permet de publier simultanément sur Twitter et Mastodon du texte et des images. Avantage: plus besoin de passer par http://crossposter.masto.donte.com.br (ou équivalent) et donc plus besoin de partager des paramètres de connexion avec des sites tiers.

Code : https://github.com/laurentabbal/publication-sur-twitter-et-mastodon-avec-python/blob/main/pytwidon.py

Pour pouvoir utiliser `pytwidon.py`, il faut tout d'abord créer les clés Twitter et Mastodon. C'est un peu long mais c'est à faire qu'une fois.

EN COURS DE REDACTION

### CLÉS TWITTER
* se connecter à son compte Twitter
* ouvrir : https://developer.twitter.com/en/portal/petition/essential/basic-info
* remplir le formulaire et valider
* cocher "Accept Terms & Conditions" puis cliquer sur "Submit"
* suivre la procédure pour vérifier l'adresse courriel
* donner un nom à l'application et cliquer sur "Get keys"
* inutile de sauvegarder les clés (il faudra les régénérer plus tard), cliquer directement sur "Dashboard" puis sur "Yes, I saved them" (même si vous ne l'avez pas fait)
* cliquer sur l'icone "App settings" de l'application
* dans la rubrique "User authentication settings", cliquer sur "Set up"
* sélectionner "Read and write" dans "App permissions", "WebApp, Automated App or Bot" dans "Type of App" puis, dans "App info", saisir l'adresse d'un site pour "Callback URI / Redirect URL" et "Website URL" (vous pouvez mettre n'importe quel site, même un site qui n'existe pas) 
* cliquer sur "Save" puis sur "Yes" puis sur "Done" (inutile de sauvegarder les données car elles ne serviront pas) et enfin sur "Yes, I saved it" (même si vous ne l'avez pas fait)
* cliquer sur l'onglet "Keys and token"
* pour "API Key and Secret", cliquer sur "Regenerate"
* sauvegarder les clés car elles ne seront plus accessibles ensuite ("API Key" sera votre `api_key` et "API Key Secret" sera votre `api_key_secret`)
* pour "Access Token and Secret", cliquer sur "Generate"
* sauvegarder les clés car elles ne seront plus accessibles ensuite ("Access Token" sera votre `access_token` et "Access Token Secret" sera votre `access_token_secret`)
* Voilà pour Twitter!


### CLÉS MASTODON

