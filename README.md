# 1- Nebula Strike 

un jeu d’arcade spatial où le joueur contrôle un vaisseau, affronte des vagues d’ennemis aux comportements différents, améliore son armement et tente d’obtenir le meilleur score.

## 2-Fonctionnalités principales :

 . Menu principal, écran de jeu, pause, game over et écran des meilleurs scores.

 . Contrôle du vaisseau au clavier, tir automatique ou manuel, déplacements limités à l’écran.

 . Vagues d’ennemis progressives avec plusieurs types : ennemi simple, kamikaze, tireur, boss.

 . Système de collisions entre projectiles, ennemis et joueur.

 . Armements interchangeables : laser simple, tir double, missile, tir en éventail.

 . Système de score, combo, vies/bouclier, power-ups et progression par vagues.

 . Sauvegarde locale des meilleurs scores en JSON .

 . Effets visuels simples : sprites, animations, explosions, sons et interface de jeu.

## 3- Structure du projet

```text
nebula Strike
├── pyproject.toml
├── readme.md
├── .gitignore
├── src/
│   └── projet_jeu_arcade/
│       ├── __init__.py
│       ├── main.py
│       ├── core/
│       │   ├── jeu.py
│       │   ├── etat_jeu.py
│       │   ├── evenements.py
│       │   ├── entites/
│       │   │   ├── joueur.py
│       │   │   ├── ennemi.py
│       │   │   ├── projectile.py
│       │   │   └── bonus.py
│       │   ├── armes/
│       │   │   ├── arme.py
│       │   │   ├── laser.py
│       │   │   ├── missile.py
│       │   │   └── tir_en_eventail.py
│       │   ├── vagues/
│       │   │   ├── vague.py
│       │   │   └── fabrique_de_vagues.py
│       │   └── services/
│       │       ├── service_collisions.py
│       │       ├── service_score.py
│       │       └── service_sauvegarde.py
│       ├── interface/
│       │   ├── rendu_pygame.py
│       │   ├── gestionnaire_entrees.py
│       │   ├── scenes/
│       │   │   ├── scene_menu.py
│       │   │   ├── scene_jeu.py
│       │   │   ├── scene_pause.py
│       │   │   └── scene_fin_de_partie.py
│       │   └── ressources/
│       ├── configuration/
│       │   └── parametres.py
│       └── persistance/
│           ├── depot_scores.py
│           └── depot_scores_json.py
└── tests/
    ├── test_joueur.py
    ├── test_service_collisions.py
    ├── test_armes.py
    ├── test_fabrique_de_vagues.py
    └── test_service_score.py