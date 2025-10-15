Scénario


Vous travaillez chez Steel Door Data Protection, Inc, une entreprise de taille moyenne dans le secteur des services informatiques qui se consacre principalement à la sécurité des données.

Vous avez rejoint la société il y a une semaine en tant qu’analyste junior. Vous faites partie de l’équipe sécurité de niveau 2, ce qui signifie que vous traitez les incidents caractérisés qui ont été triés par l’équipe sécurité niveau 1.

Passé le niveau 1, Steel Door Data Protection dispose d’une configuration unique. L’équipe de niveau 2 est divisée en deux groupes : l’équipe d’investigation et l’équipe d’intervention. Pour tout incident, l’équipe d’investigation recueille des informations, identifie les potentielles actions de remédiation et compile un rapport d’incident. L’équipe d’intervention analyse le rapport et conçoit et exécute un plan d’action. Vous êtes affecté à l’équipe d’investigation.


Votre superviseure, l’analyste principale Fatima Osei, vous a confié ce matin votre première mission dans ce mail : 

------------- ------------------------ ------------------------------ ---------------------------------- ----------------------------------------
Objet : Première mission : Alertes d’hameçonnage

Bonjour !
J’ai une première mission à te confier. Nous avons reçu deux alertes d’hameçonnage de la part de membres de deux services différents, que tu trouveras en pièce jointe. J’aimerais que tu les examines.

Pour chaque incident :

Recueille autant d’informations que possible sur l’incident. Tu peux utiliser les outils énumérés ci-dessous et les journaux de notre système de gestion des informations et des événements de sécurité (SIEM), ainsi que toute autre source reprise dans les tickets d’alerte.
Rédige ensuite un rapport d’incident décrivant les faits. Inclus les détails de l’attaque, toutes les informations que tu as recueillies et toutes les recommandations que tu as formulées. L’équipe d’intervention se basera sur ton rapport pour élaborer un plan d’action.
 
Tu peux utiliser les outils suivants pour recueillir tes informations :
- MXToolbox
- Whois
 
Envoie-moi ton (tes) e-mail(s) et ton rapport d’incident pour vérification avant de les expédier. Je passerai dans ton bureau pour un débriefing en fin de journée, sois prêt à me présenter votre documentation et à m’expliquer vos choix. Bien que tu ne sois pas en charge de la mise en œuvre de bonnes pratiques de sécurité telles que le sandboxing, je pourrai te poser des questions à ce sujet pour m’assurer que l’enquête s’est déroulée dans les meilleures conditions possibles.

Je t’enverrai les tickets d’alerte originaux soumis par les utilisateurs. Restons en contact ! 
Merci.

------------------------------------- -------------------------------- ----------------------------------- -------------------------------------
Recommandations : 

Vérifiez le ticket :
- Ce qu’a fait l’utilisateur jusqu’à présent.
- Examinez les pièces jointes ou les liens.
- Lisez la note du membre de l’équipe de niveau 1.
- Vérifiez les fichiers ou les documents envoyés par le membre de l’équipe de niveau 1.
- Lisez-les pour y rechercher toute information utile. À considérer : 

Vérifiez l’e-mail brut :
- Identifiez l’origine de l’adresse e-mail et du serveur en utilisant un outil d’analyse d’en-tête de messagerie en ligne (tel que MXToolbox).
- Vérifiez les résultats des tests SPF, DKIM et DMARC, ainsi que le score antispam Karma indiqué dans l’en-tête X-Haraka-Karma.
- Identifiez l’URL qui héberge le site web d’hameçonnage.
- Utilisez un outil (tel que whois.com) pour identifier l’IP, l’emplacement et l'hébergeur qui se cache derrière l’URL.
- Ouvrez le fichier .eml à l’aide d’un éditeur de texte basique ou d’une application de messagerie. 
- Vérifiez l’en-tête.

Vérifiez le corps du message :
- Vérifiez le code du formulaire d’hameçonnage.
- Identifiez dans le code l’endroit où apparaît le script utilisé pour recueillir des informations (celui qui a été isolé par votre collègue). 
- Vérifiez la présence d’autres éléments suspects dans le code.
- Ouvrez le fichier index.html et examinez le code source :
- Examinez le script .php fourni par votre collègue. Essayez de déterminer son objectif et la manière dont il est utilisé.
 

Ce que vous devez garder à l’esprit :

- L’e-mail brut peut s’afficher comme un e-mail normal dans une application de messagerie. Vous devrez peut-être consulter la fonction d’aide de l’application pour savoir comment afficher l’e-mail brut.
- Les résultats SPF, DKIM, DMARC et les scores Karma doivent tous figurer dans l’en-tête de l’e-mail brut. 
- Les résultats négatifs, manquants ou indiquant un danger peuvent être des éléments malveillants. 
- La présence de résultats positifs n’indique pas nécessairement que l’e-mail est sûr. Il est toutefois peu probable que ces éléments particuliers soient à l’origine d’une activité malveillante.
