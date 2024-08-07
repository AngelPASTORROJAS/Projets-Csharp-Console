# Guide de mise à jour sur GitHub sans pull request

## Objectif
Ce guide explique les étapes à suivre pour mettre à jour votre projet GitHub sans passer par une pull request.

## Prérequis
- Avoir accès en écriture au dépôt GitHub du projet
- Connaître les branches principales du projet (ex : `main`, `develop`)

## Étapes

1. **Créer une nouvelle branche à partir de la branche existante** :
```bash
git checkout -b nouvelle-branche origine/branche-existante
```
Cela crée une nouvelle branche `nouvelle-branche` à partir de la branche distante `branche-existante`.

2. **Faire les modifications souhaitées sur la nouvelle branche** :
```bash
git add .
git commit -m "Mes modifications"
```
3. **Pousser la nouvelle branche sur GitHub** :
```bash
git push origin nouvelle-branche
```
Cela pousse la nouvelle branche `nouvelle-branche` sur le dépôt distant.

<!---
4. **Fusionner la nouvelle branche sur la branche principale** (Optionnel) :
```bash
git checkout branche-principale
git merge nouvelle-branche
git push
```
Cela fusionne les modifications de la branche `nouvelle-branche` dans la branche `branche-principale` locale, puis pousse les modifications sur le dépôt distant.
--->

## Considérations
- Vérifiez que votre nouvelle branche ne crée pas de conflits avec la branche principale avant de la fusionner.
- Assurez-vous d'avoir les autorisations nécessaires pour pousser directement sur la branche principale.
- Dans un environnement de production, il peut être préférable d'utiliser une pull request pour une meilleure visibilité et un processus d'approbation.
