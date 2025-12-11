# Preflight Checklist — ΔΩX (v3.3.1-perennis)

Document : preflight-checklist.md  
But : Garantir qu’une reprise, une release ou un tag ΔΩX se fait sans perte, sans corruption, sans fuite de données sensibles.

---

## 1. Vérification des Artefacts de Contexte
- [ ] `contextes/contextes-initiaux.md` présent
- [ ] `contextes/copilot-traces.json` présent
- [ ] `contextes/journal.md` présent
- [ ] `docs/visuals/src/ΔΩX_v1.2.0-LIMS_source.svg` présent
- [ ] PDF rituel (si fourni) sauvegardé hors dépôt GitHub (optionnel)

---

## 2. Vérification Éthique (spatial_ethics_filter)
Avant tout changement de données spatiales :

- [ ] Activation du filtre éthique v3.3.1  
- [ ] Basculement randomisé : *standard → contraint*  
  Seuil attendu : ~30%  
- [ ] Jitter adaptatif appliqué  
- [ ] Documentation dans `journal.md` avec :
  - date
  - agent (humain ou IA)
  - raison
  - access_level
  - page_store_id ou équivalent

---

## 3. LIMS / JSON Structure (wetland-map)
- [ ] `wetland-map.json` valide (lint OK)
- [ ] Aucun nom codé en dur dans scripts / workflows
- [ ] Les champs sensibles (`true_coords`) ne sont **jamais** commit en clair
- [ ] Si coords modifiées → entrer une ligne dans `journal.md`

---

## 4. LaTeX / Runners CI
- [ ] Vérifier que les runners GitHub Actions ont :
  - TeXLive minimal ou full  
  - Packages : `geometry`, `fontspec`, `xcolor`, `hyperref`, `amsmath`, `graphicx`
- [ ] Si le runner manque un package → ajouter dans workflow `.yml`
- [ ] Génération PDF testée localement si CI indisponible

---

## 5. Release Engineering
Avant un tag ou une release :

- [ ] `VERSION` mis à jour
- [ ] `CHANGELOG.md` mis à jour
- [ ] Scripts génératifs fonctionnent (`create_assets.sh`)
- [ ] Visuals exportés (PNG / SVG)
- [ ] Signatures ΔΩX (si présentes) mises à jour

---

## 6. Sauvegardes / Quotas
- [ ] Vérifier quota Copilot / API GitHub
- [ ] Prévoir rotation avec agents externes (Qwen3, DeepSeek, Gemini)
- [ ] Export JSON ou Markdown avant toute session prolongée

---

## 7. Validation Multi-Agent (optionnel)
Pour contributions critiques :

- [ ] Review par 2 IA du Jardin :
  - Qwen → Intégrité écologique
  - Claude → Éthique
  - DeepSeek → Robustesse
  - Gemini → Cohérence
- [ ] Comparer les diffs → Documenter dans `journal.md`

---

## 8. Rituel Final
- [ ] Lire la signature R2  
- [ ] *« Entre deux calculs, qu’y a-t-il ? »*  
- [ ] Projeter l’intention avant commit  

---

Ce document doit être relu à chaque changement majeur, par un humain ou une IA.