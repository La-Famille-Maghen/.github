---
title: "Guide de Contribution — Testeurs e-PhotoID Express"
version: "1.0 — 26 septembre 2026"
propriétaire: "Direction Technique"
révision: "Annuelle"
conformité:
  - "Guide RH v1.2"
  - "LAU v1.1"
documents_associés:
  - "README.md"
  - "CODE_OF_CONDUCT.md"
  - "SECURITY.md"
  - "LICENSE"
  - "RECRUITMENT.md"
---

# 🤝 Guide de Contribution — e-PhotoID Express 🚀

> **Merci de mettre votre temps et vos compétences au service de la Tech-for-Good !**

Ce dépôt ne contient pas le code source d'e-PhotoID Express (privé). Vous y contribuez aujourd'hui en tant que **testeur / testeuse QA**. Une contribution de code pourra être ouverte plus tard, au cas par cas, selon votre implication dans les tests et les résultats obtenus (voir §3).

---

## 0. Cadre d'application selon votre statut

- **recommandé** pour les **bénévoles et stagiaires** : votre engagement reste **libre et volontaire**. Vous pouvez refuser une recommandation sans que cela constitue un manquement.
- **obligatoire** pour les **salariés CEA**, dans le respect du Code du travail.
- **contractuel** pour les **prestataires indépendants**, selon leur contrat.

> **Principe RH** (LAU v1.1 §6.2, Guide RH v1.2) : **aucune obligation de pointage, aucun contrôle horaire, aucune sanction disciplinaire d'employeur** ne s'applique aux bénévoles et stagiaires. La saisie du temps, si elle existe, est volontaire et sert uniquement à la valorisation comptable du bénévolat en nature (CVN).

---

## 1. Contribuer en tant que testeur (voie principale)

1. **Rejoindre le programme** : `contact@maghen.eu` ou réponse à une offre — voir [`RECRUITMENT.md`](RECRUITMENT.md).
2. **Recevoir l'invitation** sur notre espace Jira + BesTest (gratuit, ≤10 comptes).
3. **Récupérer le build** à tester — voir [`README.md`](README.md#-récupérer-un-build-de-test).
4. **Exécuter les cas de test** fournis (cas réels multilingues, conditions de luminosité/arrière-plan variées pour la conformité ANTS/ICAO).
5. **Rapporter chaque anomalie** dans Jira/BesTest avec :
   - Titre explicite (ex. `[Android] Échec du recadrage sur fond clair`)
   - Comportement observé vs attendu
   - Étapes de reproduction précises
   - Environnement (OS, version, modèle d'appareil)
   - Capture d'écran ou log si possible

> ⚠️ N'utilisez **jamais** de données personnelles réelles pour vos tests — voir [`SECURITY.md`](SECURITY.md).

## 2. Automatisation (mission secondaire, sur ce dépôt)

Si votre mission inclut de l'automatisation (ex. scripts d'accompagnement des tests, tri de candidatures), le code correspondant peut vivre dans ce dépôt. Il suit alors les mêmes règles que la section 3 ci-dessous.

## 3. Contribution de code — évolution possible, pas encore ouverte

Selon votre implication dans les tests/recettes et les résultats obtenus, la possibilité de proposer des **mini-correctifs** pourra être discutée avec vous plus tard. Tant que ce n'est pas confirmé pour votre cas, ne soumettez pas de Pull Request de code sans en avoir discuté au préalable avec la Direction Technique.

Quand cette voie s'ouvre, le workflow ci-dessous s'applique :

### 3.1 Licence de vos contributions (DCO)

Vous **conservez vos droits** sur vos contributions. En soumettant une Pull Request, vous accordez à **La Famille Maghen** une licence non exclusive, mondiale et gratuite pour utiliser, modifier et distribuer votre contribution dans le cadre du projet, et vous certifiez en être l'auteur (**Developer Certificate of Origin — DCO**) :

```bash
git commit -s -m "fix(readme): corriger le lien de téléchargement Windows"
```

### 3.2 Workflow Git

1. `git checkout main && git pull origin main`
2. `git checkout -b <prefixe>/<nom-de-la-tache>` — préfixes : `fix/`, `docs/`, `test/`, `chore/`
3. Développez, testez localement.
4. Ouvrez une Pull Request vers `main`, en liant le ticket (`Closes #12`).
5. Revue par un responsable technique — délai cible **48 heures ouvrées**.
6. Fusion après validation d'au moins **un approbateur**. **Aucun auto-merge**, quel que soit le statut.

### 3.3 Convention de nommage des commits

`<type>(<périmètre optionnel>): <description>` — types : `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`, `ci`.

### 3.4 Sécurité des contributions

- **Tolérance Zéro Secret** : jamais de mot de passe, clé d'API ou jeton en clair. Variables d'environnement (`.env`), jamais committé.
- Voir [`SECURITY.md`](SECURITY.md) pour la divulgation de vulnérabilités.

---

## 4. Devenir mainteneur

Ouvert aux testeurs et contributeurs ayant démontré un engagement régulier et le respect du [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md). Décision prise par le bureau de l'association.

---

## 5. Valorisation de votre contribution

Votre participation (tests, rapports d'anomalie, éventuel code) est enregistrée et nous vous encourageons à l'inclure dans votre rapport de stage ou vos profils professionnels (LinkedIn/CV). L'équipe de direction valide volontiers vos compétences auprès de vos futurs recruteurs.

---

## 6. Documentation associée

- **Conduite** : [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md)
- **Sécurité** : [`SECURITY.md`](SECURITY.md)
- **Licence** : [`LICENSE`](LICENSE)
- **Recrutement** : [`RECRUITMENT.md`](RECRUITMENT.md)

> **Principe directeur** : la qualification d'une relation dépend des **conditions réelles d'exécution**, pas de son intitulé.

---

## 7. Historique des versions

| Version | Date | Modifications |
|---------|------|---------------|
| 1.0 | 26/09/2026 | Version initiale pour le dépôt testeurs — contribution QA comme voie principale, contribution de code repositionnée en évolution future conditionnelle |

---

*Pour toute question : `contact@maghen.eu`.*
**© 2026 — La Famille Maghen — Tous droits réservés.**
