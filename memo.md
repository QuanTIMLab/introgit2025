# Fiche mémo Git (débutant)

## Configuration (à faire une fois par machine)

```bash
git config --global user.name "Prénom Nom"
git config --global user.email "prenom.nom@example.com"
# Windows: normaliser les fins de lignes
git config --global core.autocrlf true
```

## Workflow de base

- Voir l'état:
```bash
git status
```
- Ajouter des fichiers (préparer):
```bash
git add <fichier>
# ou tout: git add .
```
- Enregistrer un instantané:
```bash
git commit -m "Message clair au présent/impératif"
```
- Historique rapide:
```bash
git log --oneline --graph --decorate
```
- Comparer:
```bash
git diff            # avant add
git diff --staged   # après add, avant commit
```

## Distant (optionnel)

```bash
git remote add origin <url.git>
git branch -M main
git push -u origin main
git pull
```

Astuce authentification (GitHub):
- Au premier `git push`, utilisez la connexion via navigateur (Git Credential Manager) plutôt qu’un mot de passe (GitHub n’accepte plus les mots de passe simples).
 - Si le `git push` échoue pour cause de droits (403), vérifiez votre appartenance à l’organisation cible et que le remote pointe vers la bonne URL.

## Messages de commit — bonnes pratiques

- Court (50–72 caractères), impératif: « Ajoute X », « Corrige Y ».
- Décrit le « quoi » et éventuellement le « pourquoi ».

## Problèmes fréquents

- Git demande votre identité → configurer `user.name` et `user.email`.
- Fin de ligne sur Windows → `core.autocrlf true`.
- Oubli dans le commit → refaire `git add` + `git commit --amend`.
- Conflit: repérer `<<<<<<<` dans le fichier, éditer, puis `git add` et `git commit`.

## Ressources

- Pro Git (FR): https://git-scm.com/book/fr/v2
- Explain Git simply: https://xosh.org/explain-git-in-simple-words/
- Missing Semester (Git): https://missing.csail.mit.edu/
