```markdown
# 🚀 NEXUS • Mistral AI Advanced Interface

Interface web avancée et autonome pour l'API Mistral AI, avec mémoire globale persistante, système d'agents intelligents, et support multi-modèles. **100% client-side** — aucune installation serveur requise.

![Version](https://img.shields.io/badge/version-1.0-blue) ![License](https://img.shields.io/badge/license-MIT-green) ![Status](https://img.shields.io/badge/status-stable-brightgreen)

---

## ✨ Fonctionnalités

### 🧠 Mémoire Intelligente
- **Mémoire Globale** : Stockage persistant via IndexedDB, accessible à toutes les conversations
- **Injection Contextuelle** : Les mémoires pertinentes sont automatiquement injectées dans le prompt selon la requête
- **Tags & Recherche** : Organisation par tags et scoring de pertinence pour un rappel intelligent
- **Panel Dédié** : Interface coulissante pour gérer vos mémoires sans quitter le chat

### 🤖 Système d'Agents
- **Création Illimitée** : Définissez autant d'agents personnalisés que nécessaire
- **Configuration Avancée** : Nom, description, instructions personnalisées, tags mémoire, pricing (€)
- **Activation Instantanée** : Basculez entre agents en un clic, avec mise à jour dynamique du comportement de l'IA
- **Persistance Navigateur** : Vos agents sont sauvegardés localement via IndexedDB

### 🎯 21 Modèles Mistral "OK" avec Noms Futuristes
| ID Modèle | Nom Futuriste | Usage Optimal | Contexte | Prix/Tok |
|-----------|--------------|---------------|----------|----------|
| `codestral-2508` | CodeForge Nexus | Génération & optimisation de code | 4M | 1€ |
| `devstral-2512` | DevMind Ultra | Assistant dev full-stack intelligent | 4M | 1€ |
| `devstral-medium-2507` | DevPulse Medium | Équilibre parfait pour le dev quotidien | 4M | 1€ |
| `devstral-small-2507` | DevSpark Lite | Rapide et léger pour tâches dev simples | 4M | 1€ |
| `labs-mistral-small-creative` | CreatiFlow | Explosion créative pour idées innovantes | 4M | 1€ |
| `magistral-medium-2509` | MagiCore Balance | Puissance maîtrisée, réponse équilibrée | 1B | 0.08€ |
| `magistral-small-2509` | MagiSwift | Intelligence rapide, précision optimale | 1B | 0.08€ |
| `ministral-14b-2512` | MiniTitan 14B | Performance dense, efficacité énergétique | 4M | 0.5€ |
| `ministral-3b-2512` | NanoMind 3B | Ultra-rapide, idéal pour micro-tâches | 4M | 1€ |
| `ministral-8b-2512` | MicroGenius 8B | Compact mais puissant, polyvalent | 4M | 1€ |
| `mistral-large-2411` | Mistral Prime Legacy | Raisonnement complexe, expertise établie | 200B | 1€ |
| `mistral-large-2512` | Mistral Omega ⭐ | Dernière génération, intelligence suprême | 4M | 1€ |
| `mistral-medium-2505` | Mistral Equinox | Équilibre parfait vitesse/précision | - | 0.42€ |
| `mistral-medium-2508` | Mistral Zenith | Performance medium optimisée | - | 0.42€ |
| `mistral-small-2506` | Mistral Flash | Réponses instantanées, faible latence | 4M | 1€ |
| `mistral-small-2603` | Mistral Nova | Nouvelle ère des modèles compacts | - | 1€ |
| `open-mistral-nemo` | Nemo OpenCore | Polyvalent, open-source, fiable | 4M | 1€ |
| `pixtral-12b-2409` | Pixtral Visionary | Analyse visuelle + texte, multimodal | 4M | 1€ |
| `pixtral-large-2411` | Pixtral OmniSight | Vision premium, compréhension profonde | 4M | 1€ |
| `voxtral-mini-2507` | Voxtral Echo Mini | Traitement audio léger et précis | 4M | 1€ |
| `voxtral-small-2507` | Voxtral Sonic | Audio rapide, transcription intelligente | 4M | 1€ |

### 🎨 Design & Expérience Utilisateur
- **3 Thèmes** : Light ☀️ / Dark 🌙 / Sand 🏖️ avec transition fluide
- **Interface Moderne** : Glassmorphism, gradients subtils, animations CSS
- **Responsive** : Optimisé mobile, tablette et desktop
- **UX Intuitive** : `Entrée` pour envoyer, `Shift+Entrée` pour saut de ligne, toasts contextuels

### 💾 Persistance Universelle (Zero-Install)
- **IndexedDB** : Chats, agents, mémoires et paramètres stockés localement dans le navigateur
- **Cookies Sécurisés** : Clé API Mistral chiffrée, expiration 30 jours, `SameSite=Strict`
- **Reprise Automatique** : Rechargez la page, retrouvez votre session intacte

### 🔐 Gestion de la Clé API
- **Free Tier Mistral** : 1 milliard de tokens/mois offerts (~5 000€ de valeur)
- **Validation Flexible** : Accepte les formats `sk-*`, `mistral-*` ou alphanumérique (20+ caractères)
- **Stockage Local** : La clé reste sur votre machine, jamais envoyée à un serveur tiers

---

## 🚀 Installation & Utilisation

### Prérequis
- Navigateur moderne : Chrome 90+, Firefox 88+, Edge 90+, Safari 14+
- Connexion internet pour les appels API Mistral
- **Aucune installation serveur, build tool ou dépendance requise**

### Démarrage Rapide
1. **Téléchargez** le fichier `index.html` depuis ce dépôt
2. **Ouvrez-le** directement dans votre navigateur (double-clic ou `file://`)
3. **Obtenez votre clé API gratuite** :
   - Rendez-vous sur [console.mistral.ai](https://console.mistral.ai)
   - Créez un compte → API Keys → Generate
   - Copiez votre clé (commence par `sk-` ou `mistral-`)
4. **Collez la clé** dans le modal "🔓 Get Free API" → "💾 Save & Activate"
5. **Commencez à chatter** ! 🎉

### Structure du Projet
```
nexus-mistral-interface/
├── index.html          # Application complète (HTML + CSS + JS)
├── README.md           # Ce fichier
└── .gitignore          # Exclusion des fichiers sensibles
```

---

## ⚙️ Configuration Avancée

### Personnaliser les Modèles
Modifiez le tableau `MODELS` dans la section `<script>` pour :
- Ajouter/supprimer des modèles
- Changer les noms affichés, descriptions ou paramètres (température, prix)

### Ajuster la Mémoire
- **Limite de contexte** : Modifiez `memory.getRelevant(query, 4)` pour changer le nombre de mémoires injectées
- **Score de pertinence** : Ajustez la logique dans `memory.getRelevant()` pour affiner le rappel

### Thèmes Personnalisés
Ajoutez un nouveau thème dans les variables CSS `:root` et `[data-theme="xxx"]` :
```css
[data-theme="custom"] {
  --bg: #your-color;
  --primary: #your-accent;
  /* ... autres variables ... */
}
```

---

## 🔒 Sécurité & Vie Privée

- **Zero Backend** : Toutes les données restent sur votre appareil
- **Clé API Locale** : Stockée dans un cookie `SameSite=Strict`, jamais transmise à un tiers
- **IndexedDB** : Base de données navigateur isolée, inaccessible aux autres sites
- **HTTPS Requis** : L'API Mistral exige une connexion sécurisée (navigateur moderne)

> ⚠️ **Note** : Ne partagez jamais votre fichier `index.html` avec votre clé API déjà enregistrée. La clé est stockée localement — chaque utilisateur doit configurer la sienne.

---

## 🛠️ Dépannage

| Problème | Solution |
|----------|----------|
| ❌ "Invalid API key format" | Vérifiez que votre clé fait 20+ caractères et commence par `sk-` ou `mistral-` |
| ❌ "API Error: 401 Unauthorized" | Votre clé est expirée ou révoquée → régénérez-la sur console.mistral.ai |
| ❌ "IndexedDB error" | Votre navigateur bloque le stockage local → autorisez les cookies/IndexedDB |
| ❌ Pas de réponse de l'IA | Vérifiez votre connexion internet et que le free tier Mistral est actif |
| ❌ Thème non appliqué | Rechargez la page (Ctrl+R / Cmd+R) après avoir changé de thème |

### Console Développeur
Ouvrez les outils dev (F12) → Onglet "Console" pour voir les logs d'erreur détaillés.

---

## 📄 Licence

MIT License — Utilisez, modifiez et distribuez librement. Voir [LICENSE](LICENSE) pour les détails.

```
Copyright (c) 2026 NEXUS Project

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour proposer une amélioration :

1. Fork le dépôt
2. Créez une branche (`git checkout -b feature/AmazingFeature`)
3. Committez vos changements (`git commit -m 'Add: AmazingFeature'`)
4. Push vers la branche (`git push origin feature/AmazingFeature`)
5. Ouvrez une Pull Request

### Roadmap
- [ ] Export/Import des conversations en JSON
- [ ] Support du streaming des réponses (SSE)
- [ ] Plugins pour extensions tierces (calcul, recherche web, etc.)
- [ ] Mode hors-ligne avec modèles locaux (via WebLLM)

---

## 🙏 Crédits

- **[Mistral AI](https://mistral.ai)** — Pour l'API et le free tier généreux
- **[Google Fonts](https://fonts.google.com)** — Typographie Inter & JetBrains Mono
- **[CSS Variables](https://developer.mozilla.org/fr/docs/Web/CSS/Using_CSS_custom_properties)** — Pour le système de thèmes dynamique
- **Vous** — Pour avoir rendu ce projet possible ✦

---

> 💡 **Astuce Pro** : Utilisez `mistral-large-2512` (Mistral Omega) pour les tâches complexes nécessitant un raisonnement profond, et `mistral-small-2603` (Mistral Nova) pour les réponses rapides du quotidien.

**[⬆ Retour en haut](#-nexus--mistral-ai-advanced-interface)**
```
