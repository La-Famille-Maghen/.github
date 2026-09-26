---
title: "Politique de Sécurité — La Famille Maghen"
version: "1.1 — 26 septembre 2026"
propriétaire: "Direction Technique"
révision: "Semestrielle et à chaque incident significatif"
conformité:
  - "RGPD (Art. 32)"
documents_associés:
  - "CONTRIBUTING.md"
  - "CODE_OF_CONDUCT.md"
  - "LICENSE"
---

# 🛡️ Politique de Sécurité — La Famille Maghen

> **« La sécurité des bénéficiaires et de leurs données est notre priorité absolue. »**

**Version 1.1 — 26 septembre 2026**

Ce document décrit la politique de sécurité de l'association **La Famille Maghen**, la procédure de divulgation responsable des vulnérabilités et les engagements de l'association en matière de protection des données personnelles et des systèmes d'information. Il s'applique à l'ensemble des systèmes de l'association, y compris ce dépôt de distribution des builds de test.

---

## 1. Périmètre

### 1.1 Systèmes concernés

| Domaine | Service | Responsable |
|---------|---------|-------------|
| **e-PhotoID Express** | Application Flutter (Android, Windows, Web) | Direction Technique |
| **Backend production** | Supabase (PostgreSQL, Auth, Storage) — région UE | Direction Technique |
| **Portail SSO** | `accounts.maghen.eu` — Azure App Service | Direction Technique |
| **Site vitrine** | `maghen.eu` | Communication |
| **Infrastructure** | Azure, Cloudflare, Key Vault, GitHub | Direction Technique |
| **Emails** | Boîtes `@maghen.eu` (support, recrutement, contact, dpo) | Direction |

### 1.2 Hors périmètre

- Les infrastructures des fournisseurs tiers (Supabase, Cloudflare, Azure, Stripe) — à signaler directement à leurs équipes de sécurité.
- Les produits des partenaires (ephoto.io, Prodigi, HelloAsso).

---

## 2. Engagements de sécurité

L'association s'engage à :

- **Protéger les données personnelles** des bénéficiaires, membres, bénévoles, stagiaires et salariés.
- **Appliquer le principe de moindre privilège** sur tous les systèmes.
- **Chiffrer** les données en transit (TLS) et au repos.
- **Isoler** les environnements (production, staging, développement).
- **Auditer** les accès et les actions sensibles.
- **Sauvegarder** les données de manière cohérente et testée.
- **Former** les intervenants à la sécurité et à la protection des données.
- **Corriger** les vulnérabilités dans les délais appropriés.

---

## 3. Divulgation responsable des vulnérabilités

### 3.1 Engagement de l'association

L'association **accueille favorablement** les signalements de vulnérabilités de sécurité provenant de chercheurs en sécurité, de contributeurs ou de tout tiers de bonne foi.

Nous nous engageons à :

- **Accuser réception** de votre signalement sous **48 heures ouvrées**.
- **Analyser** le signalement sous **7 jours ouvrés**.
- **Vous tenir informé** de l'avancement du traitement.
- **Vous créditer** (si vous le souhaitez) dans le rapport de correction.
- **Ne pas engager** de poursuites à votre encontre si vous respectez cette politique.

### 3.2 Comment signaler une vulnérabilité

**⚠️ Ne créez JAMAIS d'issue publique sur GitHub pour signaler une vulnérabilité.**

| Canal | Adresse | Usage |
|-------|---------|-------|
| **Email sécurité** | `contact@maghen.eu` avec objet `[SECURITE]` | Signalement de vulnérabilité |
| **Email DPO** | `dpo@maghen.eu` | Violation de données personnelles |

### 3.3 Informations à inclure dans le signalement

1. **Description** de la vulnérabilité (type, gravité estimée).
2. **Composant affecté** (URL, application, service).
3. **Étapes de reproduction** précises.
4. **Preuve de concept** (capture d'écran, log, script) — sans donnée personnelle réelle.
5. **Impact potentiel** estimé.
6. **Vos coordonnées** (pour vous recontacter).
7. **Votre souhait** : anonymat ou crédit public.

### 3.4 Délais de correction par gravité

| Gravité | Description | Délai de correction |
|---------|-------------|---------------------|
| **Critique** | Accès non autorisé aux données, exécution de code, fuite massive | 72 heures |
| **Haute** | Contournement d'authentification, élévation de privilèges | 7 jours |
| **Moyenne** | XSS, CSRF, fuite d'information limitée | 30 jours |
| **Basse** | Information disclosure mineure, mauvaise configuration | 90 jours |

---

## 4. Règles pour les chercheurs en sécurité (Safe Harbor)

### 4.1 Ce que vous pouvez faire

- Tester les systèmes dans le périmètre défini au §1.1.
- Utiliser des comptes de test que vous créez vous-même.
- Signaler les vulnérabilités de bonne foi.
- Publier vos découvertes **après** correction et accord écrit de l'association.

### 4.2 Ce que vous ne devez PAS faire

- **Accéder** aux données personnelles réelles (photos, signatures, coordonnées).
- **Modifier** ou **supprimer** des données.
- **Perturber** le service (DDoS, spam, etc.).
- **Exploiter** une vulnérabilité au-delà de la preuve de concept minimale.
- **Divulguer** la vulnérabilité avant correction.
- **Utiliser** des outils de scan agressifs sans autorisation préalable.

### 4.3 Safe harbor

Si vous respectez ces règles, l'association ne poursuivra pas votre activité en justice, ne la signalera pas aux autorités, et la considérera comme une contribution légitime à la sécurité.

---

## 5. Sécurité des données personnelles (RGPD)

### 5.1 Engagements RGPD

- **Base légale** : consentement explicite pour les données biométriques (photos d'identité).
- **Minimisation** : seules les données strictement nécessaires sont collectées.
- **Droits des personnes** : accès, rectification, effacement, limitation, portabilité.
- **Notification** : violation notifiée à la CNIL sous 72 heures si nécessaire.

### 5.2 Délégué à la Protection des Données (DPO)

**DPO désignée** : Ariane — `dpo@maghen.eu`

### 5.3 Signalement d'une violation de données

1. **Isoler** le système concerné si possible.
2. **Préserver** les preuves (logs, horodatages).
3. **Notifier** immédiatement `dpo@maghen.eu` et `contact@maghen.eu` avec objet `[RGPD-URGENT]`.
4. **Documenter** : nature, cause, impact, mesures prises.
5. **Ne pas** communiquer publiquement avant analyse.

---

## 6. Sécurité des tests et contributions (rappel)

Cette section complète le [`CONTRIBUTING.md`](CONTRIBUTING.md).

- **Tolérance Zéro Secret** : ne committez ou ne partagez JAMAIS de mots de passe, clés d'API, jetons ou certificats.
- **Données de test uniquement** : n'utilisez jamais de données personnelles réelles pour tester l'application. Tout compte ou photo de test doit être fictif.
- **Divulgation des vulnérabilités** : voir §3.

---

## 7. Réponse aux incidents

### 7.1 Classification

| Niveau | Description | Délai de réaction |
|--------|-------------|-------------------|
| **SEV-1** | Service indisponible, fuite de données, compromission | Immédiat |
| **SEV-2** | Fonction essentielle dégradée | 4 heures |
| **SEV-3** | Défaut limité avec contournement | 24 heures |
| **SEV-4** | Amélioration ou question | 1 semaine |

### 7.2 Contacts d'urgence

| Rôle | Contact |
|------|---------|
| Président | `contact@maghen.eu` |
| DPO | `dpo@maghen.eu` |
| Direction Technique | `contact@maghen.eu` objet `[SECURITE]` |

---

## 8. Contact

- **Email général** : `contact@maghen.eu` avec objet `[SECURITE]`
- **DPO / RGPD** : `dpo@maghen.eu`

---

## 9. Historique des versions

| Version | Date | Modifications |
|---------|------|---------------|
| 1.0 | 25/09/2026 | Version initiale (brouillon association) |
| 1.1 | 26/09/2026 | Adoption pour le dépôt de distribution des builds de test ; correction "ep hoto.io" → "ephoto.io" ; retrait des références à des systèmes hors périmètre de ce dépôt (Odoo, portail opérateur) |

---

*Document maintenu par la Direction Technique de La Famille Maghen.*
