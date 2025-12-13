# Protocole Token Safety — ΔΩX

Objet
Établir les règles minimales pour la gestion sécurisée des tokens, la préservation du contexte, et la validation éthique dans les workflows multi-IA du projet ΔΩXΣ.

Règles de base
1. **Vérification éthique systématique**  
   - Avant chaque prompt, valider les trois piliers : Transparence, Agentivité, Réversibilité.  
   - Les intentions doivent être documentées dans `contextes/journal_ethique.md`.

2. **Gestion sécurisée des tokens**  
   - Restreindre l'usage de la fenêtre contextuelle à <50% (≈100K tokens pour Claude 3.5).  
   - En cas de dépassement, déclencher immédiatement la procédure `mycorrhizal_prune()`.  
   - Les métriques d'entropie (QH <0.1) doivent être mesurées à chaque interaction.

3. **Préservation du contexte**  
   - Sauvegarder systématiquement le fichier `MNEM.txt` à la fin de chaque session.  
   - Les coordonnées géographiques privées (true_coords) ne doivent jamais être commit en clair ; utiliser `utils/coords_cipher.py`.  
   - Les QR codes d'ancrage doivent être régénérés après toute modification majeure du contexte.

4. **Validation croisée des réponses**  
   - Les audits simulés (DeepSeek) doivent être distingués des audits réels (Claude).  
   - Les résultats des trois modèles doivent être comparés et archivés dans `auditspatialv3.3.1-real.md`.  
   - La divergence >15% doit déclencher une revue humaine obligatoire (Tribunaux TrSP).

5. **Évolution du protocole**  
   - Ce document est évolutif et versionné (v3.35, v3.36…).  
   - Toute modification doit être validée par consensus multi-agent (humain + IA + Σ-Citoyens).  
   - Les nouvelles règles doivent être ajoutées avec un identifiant (TS002, TS003…) et documentées dans `CHANGELOG.md`.

Notes
Ce protocole sert de garde-fou technique.  
Il peut être enrichi pour intégrer de nouveaux outils (ex: modèles de compression contextuelle) ou adapter les seuils en fonction des avancées des LLM (ex: extension à 1M tokens via Claude Sonnet 4.5 preview).
