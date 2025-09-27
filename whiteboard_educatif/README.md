# Tableau Blanc Éducatif Interactif - Flutter

Une application Flutter avancée qui affiche des présentations éducatives interactives avec animations synchronisées.

## 🏗️ Architecture

Cette application suit l'architecture Clean avec le pattern BLoC :

### Domain Layer
- **Entities** : Hypergeneration, Hypertoken, Coordinate
- **Repositories** : Interfaces pour l'accès aux données  
- **Use Cases** : Logique métier (Load, PlayPause, Seek)

### Data Layer  
- **Models** : Mapping JSON vers entités
- **Repository Implementation** : Implémentation concrète
- **Datasources** : Parsing et validation JSON

### Presentation Layer
- **Bloc** : Gestion d'état avec WhiteboardBloc
- **Pages** : Interface utilisateur principale
- **Widgets** : Composants réutilisables
- **CustomPainter** : Rendu graphique avec animations

## 🎨 Fonctionnalités

- ✅ Rendu temps réel des Hypertokens synchronisés
- ✅ Animations typewriter progressives
- ✅ Dessins animés avec coordonnées
- ✅ Mouvements de souris avec chemins
- ✅ Support LaTeX complet
- ✅ Système de coordonnées proportionnelles (0-100%)
- ✅ Contrôles de lecture : play/pause/seek/reset
- ✅ Timeline visuelle avec indicateurs
- ✅ Interface responsive

## 🚀 Installation

1. Créer un nouveau projet Flutter :
```bash
flutter create whiteboard_educatif
cd whiteboard_educatif
```

2. Remplacer le contenu de `pubspec.yaml` par celui fourni

3. Copier tous les fichiers dans la structure appropriée

4. Installer les dépendances :
```bash
flutter pub get
```

5. Lancer l'application :
```bash
flutter run
```

## 📱 Utilisation

1. **Charger des données** : Utilisez le bouton paramètres pour saisir votre JSON
2. **Navigation** : Contrôles play/pause/seek pour naviguer
3. **Timeline** : Barre de progression avec indicateurs de tokens
4. **Animations** : Observer le rendu en temps réel sur le tableau blanc

## 📐 Schéma JSON

```json
{
  "id": 1,
  "title": "Titre du cours",
  "generation": [
    {
      "id": 1,
      "token": "Contenu ou LaTeX",
      "type": "text|drawing|speech|mouse mouvement|simulation",
      "coordinates": [{"x": 10, "y": 20}],
      "animationType": "write|draw|follow path|fade_in|scale_up",
      "startTime": 0,
      "duration": 2000
    }
  ],
  "totalDuration": 10000
}
```

## 🔧 Dépendances Principales

- `flutter_bloc` : Architecture BLoC
- `flutter_math_fork` : Rendu LaTeX
- `equatable` : Comparaisons d'objets
- `dartz` : Programmation fonctionnelle
- `just_audio` : Support audio (extensible)

## 🎯 Extensions Possibles

- Synchronisation audio avec just_audio
- Export des animations en vidéo
- Mode édition interactif
- Thèmes personnalisés
- Partage et collaboration temps réel

---

Cette application démontre l'utilisation avancée de Flutter avec CustomPainter, 
animations complexes et architecture Clean pour des applications éducatives.