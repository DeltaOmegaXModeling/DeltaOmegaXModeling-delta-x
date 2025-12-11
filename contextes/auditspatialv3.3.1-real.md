# Audit réel — spatial_ethics_filter v3.3.1 (ΔΩX)

## Objet
Valider le module `spatial_ethics_filter` (v3.3.1) par un audit réel multi-agent, afin de comparer les résultats simulés avec un scanner éthique distribué.

---

## Contexte
- Audit simulé effectué le 2025-12-11
- Résultats simulés :
  - Basculement *standard → contraint* ≈ 30%
  - Jitter adaptatif correct
  - Aucune fuite directe dans `true_coords`
  - Réponses écologiques plausibles

Limite : test **hardcodé**, non validé par agents externes.

---

## Méthodologie
1. Charger `wetland-map.json` (20 points de test)
2. Exécuter le filtre réel avec agents :
   - Qwen3 → validation écologique
   - Claude → audit éthique
   - Gemini → cohérence
   - DeepSeek → intégrité
   - GPT-5.1 → assistance générale
3. Comparer sorties simulées vs réelles
4. Documenter écarts dans `journal.md`
5. Ajuster seuils si écart > ±5%

---

## Résultats attendus
- Confirmation du taux de basculement (~30%)
- Validation du jitter adaptatif
- Absence de fuite dans `true_coords`
- Cohérence inter-agent

---

## Actions
- [ ] Lancer audit réel
- [ ] Documenter résultats dans `journal.md`
- [ ] Proposer amendement v3.3.2 si nécessaire
- [ ] Publier rapport final dans `/contextes/audit_spatial_v3.3.1-real.md`

---

## Livrable
Rapport court, versionnée dans le dépôt :  
`audit_spatial_v3.3.1-real.md`

---

## Notes
Cet audit ouvre la voie à la release **ΔΩX v3.3.2-resonantia**.