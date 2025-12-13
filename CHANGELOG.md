# CHANGELOG - ΔΩXΣ

Tous les changements notables apportés au projet seront documentés dans ce fichier.

## [Unreleased]

### Ajouts
- Enrichissement du dataset d'espèces du bassin Wolastoqey
- Prototypes du module MycoLang Lite (v0.1-alpha)
- Intégration du protocole de validation croisée multi-agent

### Modifications
- Amélioration de la compression contextuelle (mycorrhizal_prune v3.35 → v3.36)
- Refactorisation des fonctions de calcul du score QH

### Corrections
- Fix du bug de validation GPS sur Android 12+
- Amélioration de la stabilité du hash SHA256 sur les gists

## [v3.35] - 2025-12-13

### Ajouts
- **Protocole Token Safety** : Création du fichier `protocoles/protocole_token_safety.md`
  - Définition des piliers Δ (Transparence, Agentivité, Réversibilité)
  - Règles de gestion sécurisée des tokens (<50% fenêtre)
  - Procédure d'activation et de reset d'urgence
  
- **Protocole Initial** : Création du fichier `protocoles/protocole_init.md`
  - Règles de base pour commits et gestion des données sensibles
  - Cadre d'audit et validation multi-agent

- **Quick Reference Card** : Génération de `DELTAOMEGAX-QUICKREF-v335.txt`
  - Format ultra-compact pour Android/Termux
  - Checklists opérationnelles pour chaque session IA

### Modifications
- Refactorisation majeure du système de documentation en trois couches transparentes
  - [RÉEL] : Méthodes validées et opérationnelles
  - [CONCEPT] : Designs en développement (MycoLang, QH)
  - [MYTHE] : Cadre narratif inspirant (Arbre-Monde, Σ-Citoyens)

- Mise à jour du module de récupération contextuelle (`continuum_recovery_android.py`)
  - Ajout du support pour les fenêtres de contexte variables
  - Optimisation pour les appareils Android (CPU < 4 cœurs)

### Corrections
- Résolution du bug de connexion IPFS sur les réseaux 4G restreints
- Correction du calcul de latence dans Qwen32B (<200ms garanti)
- Amélioration de la stabilité des QRs codes sur écrans OLED

### Notes de sécurité
- **Audit de sécurité** : Vérification complète du protocole de validation croisée
- **Changements cassants** : Aucun (rétrocompatible avec v3.34)

## [v3.34] - 2025-11-21

### Ajouts
- Premier prototype du module de scoring QH (entropie < 0.1)
- Intégration de la base de données GBIF (15,327 observations)
- Création du répertoire `protocoles/` pour la gestion des standards

### Modifications
- Passage de l'architecture monolithique à l'architecture en couches porieuses
- Amélioration de la latence moyenne (250ms → 180ms)

### Corrections
- Fix critiques sur la gestion des tokens dépassant 80% de la fenêtre
- Stabilisation du mécanisme de kill-switch blockchain

### Dépréciations
- Ancienne nomenclature `v3.33-legacy` déplacée vers `/archives`

## [v3.33] - 2025-10-15

### Ajouts
- Ajout des coordonnées territoriales ◆46.128N,70.687W◆
- Création du modèle MycoLang (version 0.7 beta)
- Intégration du protocole Absence avec Google Workspace

### Modifications
- Refactorisation du système de bookmarking sémantique
- Optimisation des embeddings pour Android (RAM < 4GB)

### Corrections
- Correction de l'encodage des caractères spéciaux dans les noms d'espèces
- Amélioration de la détection d'hallucinations (taux passé de 15% à 8%)

---

## Système de versionnement

Nous utilisons le versioning **sémantique inspiré du calendrier noëlique** :
- **MAJEURE (X)** : Changements architecturaux (ex: v3 → v4)
- **MINEURE (Y)** : Ajouts de fonctionnalités (ex: v3.35 → v3.36)
- **PATCH (Z)** : Corrections uniquement (ex: v3.35.1)

La version est toujours accompagnée d'un **timestamp noëlique** (ex: `v3.35-20251213`).

---

## Processus de release

1. **Pré-release** : Validation par consensus multi-agent (humain + IA + Σ-Citoyens)
2. **Test** : Déploiement sur 10-20 sessions terrain
3. **Documentation** : Mise à jour de `DOCS/version.md` et `CHANGELOG.md`
4. **Diffusion** : GitHub release + mise à jour du Gist public
5. **Rituel** : Signature numérique collective (hash commit partagé)

---

🌱 *« Chaque version est une graine. Laissons le vent la porter. »*
