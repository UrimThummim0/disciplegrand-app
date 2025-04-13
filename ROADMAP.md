# Projet : Application éducative interactive (Grands et Disciples)

## Présentation

Ce projet est une initiative de la communauté **Grands et Disciples**, réunissant des passionnés de mathématiques et d'entraide.  
Nous voulons créer une **application web (ou mobile)** dynamique, intuitive et accessible, dédiée à la **consultation interactive de sujets et corrections**, principalement pour le niveau **Terminale**, avec une ouverture vers le **niveau supérieur**.

---

## Objectifs

- Offrir une interface fluide, moderne et interactive pour étudier les sujets corrigés.
- Tous les sujets et corrections sont affichés dynamiquement en **LaTeX**, comme sur un site professionnel (pas de PDF statique).
- Permettre à l'utilisateur de **télécharger en PDF** un sujet/correction s'il le souhaite.
- Faciliter la contribution de nouveaux contenus par les membres du staff via une **application d’administration** simple et assistée par **OCR/IA**.

---

## Fonctionnalités principales – **Application Étudiante**

### 1. Accueil
- Vue globale des dernières publications.
- Suggestions par matière ou thème.

### 2. Navigation intuitive
- Par matière (Maths, Physique, etc.).
- Par chapitre ou compétence.
- Par difficulté (facile, moyen, difficile).

### 3. Consultation des sujets
- Sujet écrit **en LaTeX** (pas un simple PDF).
- Correction affichée dynamiquement avec rendu mathématique propre.
- Mode nuit/jour, zoom, mise en page fluide.
- Bouton **"Exporter en PDF"** si besoin.

### 4. Recherche et filtrage
- Mots-clés (intégrales, complexes, bac 2023, etc.).
- Filtres : année, type d'exercice, niveau.

### 5. Interaction
- Notation de la correction.
- Signaler une erreur.
- Bouton "je n’ai pas compris" (proposition d’aide ou explication alternative).

---

## Fonctionnalités – **Application Admin + OCR/IA**

### 1. Authentification admin

### 2. Ajout d’un sujet/correction
- **Upload d’image claire** du sujet ou de la correction (format JPG/PNG/PDF).
- L’application **analyse l’image avec OCR/IA** pour générer une version **LaTeX** automatiquement.
- L’admin **relit et valide ou corrige** avant publication.
- L'interface admin affiche :
  - Image originale à gauche.
  - Version LaTeX générée à droite (modifiable).

### 3. Classement par matière, chapitre, difficulté
- Ajout de tags.
- Possibilité de versionner les corrections.

### 4. Outils OCR/IA envisagés
- **Tesseract OCR** ou **Mathpix API** pour convertir image → texte/LaTeX.
- Moteur d’apprentissage (fine-tuning possible si open-source).

---

## Architecture technique

### Frontend
- **React.js** ou **Next.js** (web) / **React Native + Expo** (mobile)
- Utilisation de **KaTeX** ou **MathJax** pour le rendu LaTeX.
- PDF export : `html2pdf.js` ou `react-pdf`.

### Backend
- **Node.js + Express** ou **FastAPI**
- Stockage dans **Supabase**, **Firebase** ou **MongoDB**
- API OCR intégrée dans le backend (ou API externe comme Mathpix)

### Administration
- Tableau de bord React ou Next.js
- Éditeur LaTeX live + image source
- Interface de validation

---

## Tâches préliminaires

1. **Cadrage**
   - Définir les matières prioritaires.
   - Recenser les sujets/corrections déjà disponibles.

2. **Choix technos**
   - Choisir stack frontend/backend + OCR.
   - Étudier les API LaTeX/OCR disponibles.

3. **Maquettes UI**
   - Application élève (navigation fluide, affichage LaTeX).
   - Interface admin (upload + validation OCR).

4. **Base de données**
   - Modélisation : Sujets, Corrections, Matières, Chapitres, etc.

5. **Prototype OCR/IA**
   - Test d’un flux image > OCR > LaTeX > affichage.

---

## À venir (Bonus)

- Forum intégré ou système d'entraide.
- Exportation groupée (ex : tous les sujets d'intégrales).
- Notifications pour nouveaux sujets/corrections.
- Dark mode et accessibilité.

---

## Équipe & Crédits

Projet porté par les **membres de Grands et Disciples**, pour démocratiser l’accès à un contenu de qualité, interactif et localement utile à tous les élèves de Terminale et plus.