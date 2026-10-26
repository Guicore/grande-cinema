Git Branching Strategy — La Grande Cinéma

1. Objectif

Cette convention définit l'organisation des branches Git du projet La Grande Cinéma afin de faciliter le travail en équipe, l'intégration du code et les livraisons.

2. Branches permanentes

main

Contient le code stable et validé, prêt pour la production.

Les modifications passent par une Pull Request.

Chaque livraison peut être identifiée par un tag de version.

develop

Branche d'intégration des fonctionnalités.

Sert de base aux branches de développement.

Reçoit les modifications après revue et validation.

3. Branches temporaires

Préfixe

Utilisation

Exemple

feature/

Nouvelle fonctionnalité

feature/movie-catalog

fix/

Correction d'un bug

fix/seat-availability

hotfix/

Correction urgente en production

hotfix/payment-error

docs/

Documentation

docs/branching-strategy

refactor/

Refactorisation du code

refactor/booking-service

test/

Ajout ou modification de tests

test/booking-api

chore/

Maintenance et configuration

chore/ci-setup

4. Règles de nommage

Utiliser des lettres minuscules.

Séparer les mots avec des tirets (kebab-case).

Éviter les espaces, accents et caractères spéciaux.

Utiliser un préfixe correspondant à la nature du changement.

Garder des noms courts, précis et explicites.

5. Cycle de développement

Créer une branche temporaire depuis develop.

Réaliser les modifications et effectuer des commits explicites.

Ouvrir une Pull Request vers develop.

Vérifier le code et exécuter les tests.

Fusionner après validation.

Préparer une livraison en fusionnant develop dans main via une Pull Request.

Pour un correctif urgent, créer une branche hotfix/ depuis main, puis reporter le correctif dans develop.

6. Bonnes pratiques

Ne pas pousser directement sur main ou develop.

Privilégier les Pull Requests et la revue de code.

Exécuter les tests avant chaque fusion.

Supprimer les branches temporaires après leur fusion.

Ne jamais versionner de secrets, mots de passe ou clés API.

7. Exemples

feature/online-booking

feature/digital-ticket

feature/admin-dashboard

fix/double-booking

docs/api-documentation

test/seat-reservation