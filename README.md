# Synapse - Second Brain Kit

Un vault Obsidian preconfigure pour donner une memoire permanente a Claude Code.

## Installation

1. Dezippe ce dossier ou tu veux sur ta machine
2. Ouvre Obsidian -> "Open folder as vault" -> selectionne ce dossier
3. Lance Claude Code dans le dossier du vault
4. Tape `/prime` pour charger le contexte

## Structure

```
raw/           <- Ton espace. Articles, docs, notes.
wiki/          <- L'espace de Claude. Il compile et organise.
CLAUDE.md      <- Les regles du jeu.
.claude/       <- Commandes et skills locaux Claude.
skills/        <- Instructions pour les operations.
```

## Les 5 operations

| Commande  | Ce qu'elle fait                               |
| --------- | --------------------------------------------- |
| `/prime`  | Charge le contexte en debut de session        |
| `/ingest` | Compile tes sources brutes en notes wiki      |
| `/save`   | Sauvegarde ce que tu as fait dans la session  |
| `/query`  | Cherche une info dans ton wiki                |
| `/lint`   | Verifie la sante du vault                     |

## Architecture 3 couches

```
raw/           Humain ecrit, LLM lit (immutable)
wiki/          LLM ecrit, Humain browse (compile)
CLAUDE.md      Schema - regles du vault (humain configure)
```

Plus tu alimentes le vault, plus Claude a de contexte, plus il est pertinent.
