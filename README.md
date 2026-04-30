# Zed — Magic UI for windows

> Config personnelle pour [Zed](https://zed.dev) sur Windows 11, avec effet de transparence blur via Windhawk.

![Aperçu de Zed](/assets/preview.png)

---

## Fichiers

| Fichier | Rôle |
|---|---|
| `settings.json` | Configuration générale (thème, polices, IA, terminal…) |
| `keymap.json` | Raccourcis clavier personnalisés |

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

## 📦 Prérequis

- [Zed](https://zed.dev) pour Windows
- [JetBrainsMono Nerd Font](https://www.nerdfonts.com/font-downloads)
- [Windhawk](https://windhawk.net) (pour l'effet blur)
- Extension Zed : **Catppuccin** (thème)
- Extension Zed : **Material Icon Theme**
- 
---

### Installation

```bash
    cd C:\Users\USERNAME\AppData\Roaming
    mv Zed Zed_backup
    git clone https://github.com/Benji-devw/zed_conf_navart.git
    mv zed_conf_navart Zed
```

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

## 🛠️ Zed Panel Git Fix

```bash
    git config --global --add safe.directory '*'
```

## 👤 Auteur
[NAVART](https://github.com/Benji-devw/)
