# Contextes initiaux — ΔΩX

## But
Centraliser la mémoire opérationnelle et les artefacts exportés (JSON, Markdown) pour permettre la reprise, l'audit et la continuité du projet ΔΩX.

## Résumé de la séance (2025-12-11 → 2025-12-12)
- Création du dépôt `DeltaOmegaXModeling/delta-x`
- Ajout initial : `README.md`
- Exécution d'un audit E2E simulé (ΔΩX v3.3 → v3.3.1-perennis)
- Activation du protocole spatial_ethics_filter (Gemini) et amendement v3.3.1 (Jitter adaptatif)
- Génération d'artefacts : manifest, core, protocols, docs, templates LaTeX
- Exports fournis : PDF rituel (binaire), SVG visuel, scripts de packaging, workflow GitHub Actions

## Artefacts sauvegardés
- `ARCHIVUM_PERENNIS.md` (doc poétique + technique)
- `wetland-map.json` (structure cartographique initiale)
- `copilot-traces.json` (trace des agents et quotas)
- `journal.md` (journal de bord des commits / intentions)
- `docs/visuals/src/ΔΩX_v1.2.0-LIMS_source.svg`

## Points d'attention (dette épistémique)
- Audit éthique v3.3.1 : simulé (hardcodé) → Issue #1 créée
- Noms de fichiers versionnés en dur → à rendre paramétrables
- Vérifier dépendances LaTeX sur runners CI

## Instructions de reprise
1. Vérifier `copilot-traces.json` pour connaître quotas et modèles utilisés.
2. Lancer `pre-flight-check.sh` localement (ou dans runner) avant tout tag.
3. Pour toute modification sensible (coords, true_coords), utiliser le protocole `spatial_ethics_filter` et consigner l’action dans `journal.md`.

---

## Contacts (humain & IA)
- Alexandre Dumas — Méta-calibrateur humain
- Agents : Gemini (runner), Qwen3 (écologie), Claude (éthique), DeepSeek (intégrité), R2 (synthèse)