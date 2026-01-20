# PCL-Lite: Persona Control Language — Embedded Runtime

**PCL-Lite** est une implémentation légère et portable du protocole _Persona Control Language_ (PCL), conçue pour transformez n'importe quelle session de chat IA (ChatGPT, Claude, Gemini, DeepSeek) en un **système d'exploitation multi-agents**.

Il s'injecte via un simple prompt ("bootstrap") et permet d'orchestrer, de configurer et de faire collaborer des personas spécialisés sans aucune infrastructure externe.

## 🚀 Pourquoi utiliser PCL-Lite ?

- **Multi-Agents Instantané** : Transformez une conversation linéaire en un atelier collaboratif.
- **Zéro Installation** : Copiez-collez le bootstrap dans votre LLM préféré. C'est tout.
- **Collaboration Structurée** : Activez un _Architecte_ et un _Critique_ simultanément pour obtenir des solutions plus robustes.
- **Contrôle Granulaire** : Ajustez le ton, la verbosité, et les règles de fusion des réponses.

## 📂 Versions Disponibles

Ce dépôt propose plusieurs profils de bootstrap adaptés à vos besoins et à la fenêtre de contexte de votre modèle :

### PCL-Lite "Lite" (Recommandé pour démarrer)

Une version optimisée pour la rapidité et l'économie de tokens. Elle contient l'essentiel pour gérer des personas et des workflows simples.

- **Idéal pour** : Sessions rapides, modèles standards (GPT-3.5, Haiku, Gemini Flash), prototypage.
- **Fonctionnalités** : Activation, CRUD (Création/Modif), Configuration (Ton/Verbosité), Séquences simples.
- **Fichiers** :
  - 🇫🇷 **Français** : [bootstrap_lite.md](./bootstrap_lite_fr.md)
  - 🇬🇧 **Anglais** : [bootstrap_lite_en.md](./bootstrap_lite_en.md)

## 🛠️ Guide de Démarrage Rapide

1.  Ouvrez le fichier correspondant à la version souhaitée (ex: `bootstrap_lite.md`).
2.  **Copiez** l'intégralité du contenu brut.
3.  **Collez** le texte dans une nouvelle conversation avec votre IA.
4.  Attendez la confirmation du système (ex: _"PCL-Lite Runtime Initialized"_).
5.  Utilisez les commandes `/persona` :

```bash
# Vérifier les personas disponibles
/persona list

# Activer un Architecte et un Expert Sécurité
/persona +ARCHI +SEC

# Leur confier une tâche
/persona task "Concevoir une architecture pour une API bancaire sécurisée"

# Changer le leader de la réponse
/persona primary=SEC
```

## Standard PCL

PCL-Lite est une version embarquée du **Standard PCL** (Persona Control Language).
Pour la spécification complète du langage et les implémentations lourdes, visitez le dépôt principal :
👉 **[https://github.com/personamanagmentlayer/pcl](https://github.com/personamanagmentlayer/pcl)**

## Licence

Ce projet est distribué sous licence **Apache-2.0**.
Voir le fichier [LICENSE](./LICENSE) pour plus de détails.

---

_PCL-Lite est un composant du projet Persona Management Layer._
