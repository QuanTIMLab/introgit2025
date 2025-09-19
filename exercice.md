# Exercice — Premier commit (sur le dépôt de l’organisation)

Objectif: cloner le dépôt, ajouter votre prénom à `participants.md`, valider et pousser.
Durée: 10–15 minutes.

## Étapes (réseau requis)

1) Cloner le dépôt et entrer dans le dossier:

```bash
git clone https://github.com/QuanTIMLab/introgit2025.git
cd introgit2025
```

2) Ouvrez `participants.md` et ajoutez UNE ligne avec votre prénom (à la fin du fichier).
3) Sauvegardez, puis dans le terminal:

```bash
git status
git add participants.md
git commit -m "Ajoute <Votre prénom> à la liste des participants"
git pull --rebase origin main
git push origin main
```

Vous devriez voir votre nom apparaître sur la slide « Participants (live) » au bout de quelques secondes.

Astuce anti‑conflits:
- Ajoutez votre ligne à la fin du fichier.
- Faites `git pull --rebase` avant `git push` si quelqu’un a poussé entre-temps.

## Plan B (100% local, sans réseau)

1) Ouvrir ce dossier.
2) Éditer `participants.md`, ajouter votre prénom.
3) Valider:

```bash
git status
git add participants.md
git commit -m "Ajoute <Votre prénom> à la liste des participants"
git log --oneline
```

