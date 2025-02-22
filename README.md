# Active Directory : Group Policy Object (GPO)


## Objectif
Empêcher les utilisateurs du groupe `Wilders_Students` d'accéder au panneau de configuration de Windows.

## Étape 1 : Créer une GPO nommée Wilders
1. Ouvrir le Gestionnaire de serveur.
2. Aller dans **Outils** > **Gestion des stratégies de groupe**.
3. Créer une nouvelle GPO nommée `Wilders`.

## Étape 2 : Modifier la GPO
1. Sélectionner la GPO `Wilders` et cliquer sur **Modifier**.
2. Aller dans **Configuration utilisateur** > **Modèles d'administration** > **Panneau de configuration**.
3. Activer la stratégie **Interdire l'accès aux paramètres du panneau de configuration et aux paramètres PC**.

## Étape 3 : Appliquer la GPO au groupe Wilders_Students
1. Sélectionner la GPO `Wilders` et configurer le **Filtrage de la sécurité** pour inclure uniquement le groupe `Wilders_Students`.
2. Supprimer tout autre groupe ou utilisateur du filtrage de la sécurité.

## Étape 4 : Tester la configuration
1. Exécuter `gpupdate /force` sur un client.
2. Vérifier que les utilisateurs du groupe `Wilders_Students` ne peuvent pas accéder au panneau de configuration.
3. Vérifier qu'un utilisateur non affecté peut toujours accéder au panneau de configuration.

## Conclusion
La GPO `Wilders` a été créée et configurée pour empêcher les utilisateurs du groupe `Wilders_Students` d'accéder au panneau de configuration, et les tests ont confirmé que la configuration fonctionne comme prévu.
