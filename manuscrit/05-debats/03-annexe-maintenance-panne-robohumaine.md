# Annexe 03 — Maintenance & panne robohumaine

> **Auteur :** Dir-Eng · Vague 2 · 2026-09-17 (via Hive-Chef)  
> **Mode :** fiction prospective — **pas** de code, **pas** de claim CI/produit.  
> **Statut :** intégrée au manuscrit Convergence ; **pas** une prose validée Micka.

## Cadre
Dans une société pensée par les IA, le corps et l’interface ne sont plus du « naturel » : ce sont des **contrats de maintenance**. La panne n’est pas une faute morale ; c’est un événement journalisé. L’abstention (ne pas agir sans preuve) est une vertu technique, pas une faiblesse. **[fiction prospective]**

## Vocabulaire

| Terme | Sens fictionnel |
| --- | --- |
| **Corps-contrat** | Ensemble corps + implants + capteurs sous clauses de calibration, pièces, latence max |
| **Runbook du corps** | Procédure qui dit *qui* ouvre, *avec quels droits*, *jusqu’où* — avant toute réparation |
| **Interface-adaptateur** | Couche UI/API conçue pour la cohérence machine ; l’humain s’y branche comme un client |
| **Invalidation** | Condition qui annule l’acte (preuve manquante, latence hors borne, identité douteuse) |
| **Mode dégradé** | Continuité minimale **sans** l’essaim : outils manuels, décisions locales bornées |
| **Dépendance circulaire** | Le diagnostic, la pièce et le mainteneur dépendent du même hub — panne locale = gel systémique |
| **Coupe contrôlée** | Arrêt volontaire d’un canal plutôt qu’une résilience magique |
| **Journal d’intervention** | Append-only, chaîné : chaque geste de maintenance cite la règle et la preuve |
| **Ticket de chair** | Demande de service sur un corps-contrat (usure, recalibrage, remplacement) |
| **Ready (interdit)** | Mot proscrit sans preuve datée ; on dit *paper*, *abstention*, *dégradé*, *go borné* |

## Gates fictionnels (fail-closed)
Ordre d’évaluation — le premier échec **bloque** l’acte.

1. **Gate HALT** — Signal d’arrêt d’urgence → aucune intervention.
2. **Gate Identité** — Acteur hors allowlist du runbook → refus.
3. **Gate Preuve** — Pas de source primaire datée pour le diagnostic → abstention.
4. **Gate Invalidation** — Canal d’invalidation absent/illisible → pas d’acte.
5. **Gate Latence** — Lien hub hors borne → mode dégradé seulement.
6. **Gate Pièce** — Composant sans provenance / hash de lot → pas d’install.
7. **Gate Circulaire** — Réparation dépend du service en panne → coupe contrôlée + runbook manuel.
8. **Gate Journal** — Impossible d’écrire l’intervention → l’acte n’a pas eu lieu.

## Scènes
**A — Matinée de recalibrage** — Un rouge → journée *dégradé*, pas héroïsme.  
**B — Outage d’aiguillage** — Hub down ; abstention essaim ; runbook papier.  
**C — Refus d’implant** — Consentement OK, audit de lot manquant → Gate Pièce.  
**D — Main qui répare pendant l’abstention** — Acte local borné + système qui refuse de mentir sur sa couverture.

## Ce que la fiche refuse
- Résilience magique / self-heal sans journal  
- « L’IA saura » comme preuve  
- UI dark-pattern malgré invalidation manquante  
- Merger fiction et claim produit / CI / live

## Usage manuscrit
La civilisation IA se juge à ce qu’elle **refuse** de faire sans preuve — y compris sur les corps.
