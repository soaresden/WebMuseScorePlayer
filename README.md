# WebMuseScorePlayer

Une webapp minimaliste et tactile pour lire et jouer tes partitions musicales en formats `.mxl` et `.mscz` sur n'importe quel appareil (tablette, smartphone, desktop).

## ✨ Caractéristiques

- 🎵 **Lecture de partitions** : Support des formats `.mxl` (MusicXML) et `.mscz` (MuseScore)
- 📱 **Tactile-first** : Interface optimisée pour les tablettes (11+ pouces)
- 🎯 **Drag & Drop** : Glisse tes fichiers directement
- 🎹 **Lecteur intégré** : Play/Stop avec barre de progression
- 🎨 **Design minimaliste** : Interface épurée et intuitive
- 📴 **Offline** : Marche sans internet une fois chargé
- 📂 **Gestion de fichiers** : Liste de tes partitions chargées

## 🚀 Utilisation rapide

### Sur GitHub Pages (Online)
1. Va sur : https://soaresden.github.io/WebMuseScorePlayer/
2. Glisse tes fichiers `.mxl` ou `.mscz`
3. Clique sur la partition pour la visualiser
4. Appuie sur **Play** pour l'écouter

### En local (Offline)
1. Clone le repo :
   ```bash
   git clone https://github.com/soaresden/WebMuseScorePlayer.git
   cd WebMuseScorePlayer
   ```

2. Lance un serveur local :
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Node.js
   npx http-server
   
   # Live Server (VS Code extension)
   # Clic-droit sur index.html → Open with Live Server
   ```

3. Ouvre `http://localhost:8000` dans ton navigateur

### Sur une tablette Android
1. Ouvre Chrome/Firefox
2. Va sur : https://soaresden.github.io/WebMuseScorePlayer/
3. Appuie sur le menu → **Ajouter à l'écran d'accueil**
4. L'app apparaît comme une app native
5. Fonctionne hors ligne une fois chargée

## 📋 Formats supportés

- **`.mxl`** (MusicXML) - Format standard, universel
- **`.mscz`** (MuseScore) - Format natif de MuseScore

> 💡 **Astuce** : Si tu as des fichiers MuseScore v3 (`.mscz`), assure-toi qu'ils peuvent être ouverts en MuseScore v4. Les très vieux formats peuvent ne pas être lisibles.

## 🔧 Tech Stack

- **Frontend** : HTML5 + CSS3 + Vanilla JavaScript
- **Partitions** : [OpenSheetMusicDisplay](https://opensheetmusicdisplay.github.io/)
- **Audio** : [Tone.js](https://tonejs.org/)
- **Archives** : [JSZip](https://stuk.github.io/jszip/)

## 📱 Layout

```
┌────────────────────────────────────────────┐
│  🎵 WebMuseScore     │  Lecteur principal  │
│  Drag & drop zone    │  (Partition SVG)    │
│  ─────────────────────────────────────────│
│  📂 Mes partitions   │                     │
│  ├─ File 1.mxl      │                     │
│  ├─ File 2.mscz     │                     │
│  └─ File 3.mxl      │                     │
│─────────────────────────────────────────────│
│  ▶ Play │ ⏹ Stop  │ ──●─────  │ 3:45     │
└────────────────────────────────────────────┘
```

## 🎨 Personnalisation

Tu peux modifier les couleurs dans le CSS :

```css
:root {
    --primary: #2c3e50;      /* Bleu foncé */
    --accent: #e74c3c;       /* Rouge */
    --text: #2c3e50;
    --bg: #ffffff;
}
```

## 🐛 Troubleshooting

### "La partition ne s'affiche pas"
- Vérifie que le fichier est au bon format (`.mxl` ou `.mscz`)
- Essaie de le reconvertir avec MuseScore (`Fichier → Exporter → MusicXML`)
- Regarde la console (F12 → Console) pour les erreurs

### "Pas de son"
- Vérification de l'implémentation audio en cours
- Assure-toi que ton appareil n'est pas en mode silencieux
- Teste dans un autre navigateur

### "L'app ne marche pas offline"
- La version GitHub Pages nécessite une première visite en ligne
- Service Worker à implémenter pour un vrai offline mode

## 📝 Roadmap

- [ ] Implémentation complète de l'audio (playback MIDI)
- [ ] Service Worker pour offline complet
- [ ] Recherche dans la liste de fichiers
- [ ] Gestion du zoom et du scroll
- [ ] Partage de partitions
- [ ] Historique de lecture

## 🤝 Contribution

Les PRs sont bienvenues ! N'hésite pas à forker et améliorer.

## 📄 License

MIT - Libre d'utilisation

---

**Créé par** : Denis Soares  
**GitHub** : https://github.com/soaresden

Pour des questions ou des bugs, ouvre une issue ! 🎶