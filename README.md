# TP-OutilsFormel__KPANIGO-OBED-MARCEL

TP
L'objectif  est de spécifier, modéliser, vérifier et optimiser un système de contrôle d'accès pour un bâtiment sécurisé. Ce système utilise des règles de logique formelle, des automates pour gérer les états du système, des circuits logiques pour la réalisation matérielle, et des méthodes formelles pour vérifier la conformité du système avec les spécifications.

	SPECIFICATIONS 
Pour le bon déroulement de l'algorithme comme fonctionnalités nous avons :
 - Enregistrer des utilisateurs avec un nom, un code d'entrée et une carte d'accès unique.  
 - Autoriser ou refuser l'accès en fonction de la validité de la carte et du code.  
 - Suivre si une personne est à l'intérieur du bâtiment ou non.  
 - Enregistrer un historique des entrées et sorties avec l'heure.  
 - Gérer les erreurs comme les codes invalides ou les tentatives multiples échouées. 

	DESCRIPTION DE L'AUTOMATE
Pour l'automate nous avons plusieurs états :
 - q0 = état initial
 - q1 = accès accordé
 - q2 = accès refusé
 - q3 = alarme déclenchée

q0 : Aucun accès encore accordé.  
q1 : L'utilisateur est authentifié et peut entrer.  
q2 : L'accès est rejeté pour des raisons de sécurité.  
q3 : Plus de trois échecs d'accès entraînent une alerte.  

Les transitions entre ces états dépendent des actions de l'utilisateur, comme l'utilisation d'une carte ou l'entrée d'un code.

	VERIFICATIONS ET RESULTATS
Nous avons fait plusieurs éventualité pour vérifier le système : 
 - Accès avec carte et code valides : Fonctionne correctement, l'utilisateur peut entrer.  
 - Accès avec carte invalide : L'accès est refusé immédiatement.  
 - Code incorrect 3 fois : L'alarme est déclenchée.  
 - Double entrée : Impossible pour une personne déjà à l'intérieur.
Et nous avons l'historique qui est mis à jour correctement pour chaque entrée et sortie.

	DEFIS RENCONTRES ET SOLUTIONS APPORTES
 - Cartes d'accès dupliquées : nous avons en sorte que chaque utilisateurs ait une carte unique avant qu'il soit enregistré 
 - Erreur d'état : Pour cela on a ajouté une vérification pour savoir si l'utilisateur est déjà dans le bâtiment avant qu'on lui accorde l'accès 
 - Limitation des tentatives : Après trois erreurs, une alarme est déclenchée pour garantir la sécurité.

	CONCLUSION
Le système est fiable, efficace et simple à utiliser. Il respecte toutes les spécifications initiales. Il est efficace dans le sens où on a une gestion claire es états et des transitions puis une un historique détaillé et horodaté et une robustesse face aux erreurs
