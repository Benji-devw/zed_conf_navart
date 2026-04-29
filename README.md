# Zed — Magic UI for windows

> Config personnelle pour [Zed](https://zed.dev) sur Windows 11, avec effet de transparence blur via Windhawk.

![Aperçu de Zed](/assets/preview.png)

---

## 🧰 Fonctionnalités

- **Thème** : Catppuccin Frappé (Blur) en mode sombre
- **Police éditeur** : JetBrainsMono Nerd Font Mono, taille 18, graisse 300, interligne 1.9
- **Police UI** : System UI Font
- **Transparence** : fond semi-transparent `#33344190` avec panneaux quasi-transparents
- **Raccourcis clavier** personnalisés (style BÉPO-like sur AZERTY) — voir `keymap.json`
- **Agents IA** : GitHub Copilot (GPT-4.1 par défaut, Gemini Flash pour l'assistant inline)
- **Autosave** : à chaque changement de fenêtre
- **Git panel** : vue arborescente, ancré à gauche

---

## Effet blur transparent (Windows)

L'effet de fond transparent avec blur natif Windows nécessite **Windhawk**.

### Installation

1. Télécharger et installer **[Windhawk](https://windhawk.net)**
2. Dans Windhawk, chercher et activer le mod **Translucent Windows**
3. Dans les paramètres du mod, ajouter un **nouvel élément** :
   - **Process** : chemin complet vers `zed.exe`
     (ex. `C:\Users\<nom>\AppData\Local\Programs\Zed\zed.exe`)
4. Pour ce processus, activer :
   - **Background translucent effects** → `Blur (AccentBlurBehind)`
5. Appliquer — Zed sera relancé automatiquement.

> Les couleurs de fond dans `settings.json` utilisent un canal alpha (`#RRGGBBAA`).
> La valeur `#33344190` correspond à la couleur Catppuccin Frappé avec ~56 % d'opacité.

---

## Fichiers

| Fichier | Rôle |
|---|---|
| `settings.json` | Configuration générale (thème, polices, IA, terminal…) |
| `keymap.json` | Raccourcis clavier personnalisés |

---

## Raccourcis clavier

### Éditeur

| Raccourci | Action |
|---|---|
| `Ctrl+E` | Commenter / décommenter (toggle) |
| `Shift+Alt+Z` / `Shift+Alt+S` | Déplacer la ligne haut / bas |
| `Alt+Entrée` | Insérer une ligne en dessous |
| `Alt+O` / `Alt+N` | Scroll page haut / bas |

### Curseur

| Raccourci | Action |
|---|---|
| `Alt+Z` / `Alt+S` | Ligne haut / bas |
| `Alt+K` / `Alt+J` | 5 lignes haut / bas |
| `Alt+Q` / `Alt+D` | Caractère gauche / droite |
| `Alt+W` | Début de ligne |
| `Alt+F` | Fin de ligne |
| `Alt+H` / `Alt+L` | Mot précédent / suivant |

### Sélection

| Raccourci | Action |
|---|---|
| `Alt+E` | Étendre la sélection syntaxique |
| `Shift+Alt+Q` / `Shift+Alt+D` | Sélection caractère gauche / droite |
| `Shift+Alt+K` / `Shift+Alt+J` | Sélection ligne haut / bas |
| `Shift+Alt+H` / `Shift+Alt+L` | Sélection sous-mot gauche / droite |

### Suppression

| Raccourci | Action |
|---|---|
| `Alt+U` / `Alt+I` | Backspace / Suppr |
| `Shift+Alt+I` | Supprimer la ligne entière |
| `Ctrl+Alt+U` / `Ctrl+Alt+I` | Supprimer mot gauche / droite |

### Onglets (AZERTY)

| Raccourci | Action |
|---|---|
| `Alt+&` (Alt+1) | Onglet précédent |
| `Alt+à` (Alt+0) | Onglet suivant |
| `Alt+é` (Alt+2) | Tab switcher |

### Workspace & Panneaux

| Raccourci | Action |
|---|---|
| `Ctrl+Alt+H` / `Ctrl+Alt+L` | Focus panneau gauche / droit |
| `Ctrl+Alt+K` / `Ctrl+Alt+J` | Focus panneau haut / bas |
| `Alt+X` | Outline (symboles du fichier) |
| `Ctrl+Alt+N` | Panneau Git (toggle) |
| `Ctrl+Alt+G` | Focus panneau Git |
| `Alt+K` / `Alt+J` | Navigation dans le ProjectPanel |

---

## 📦 Prérequis

- [Zed](https://zed.dev) pour Windows
- [JetBrainsMono Nerd Font](https://www.nerdfonts.com/font-downloads)
- [Windhawk](https://windhawk.net) (pour l'effet blur)
- Extension Zed : **Catppuccin** (thème)
- Extension Zed : **Material Icon Theme**


## Zed Panel Git Fix

```bash
git config --global --add safe.directory '*'
```

## 👤 Auteur
[NAVART](https://github.com/Benji-devw/)
