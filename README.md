# 🚀 Déploiement Continu avec GitHub Actions & Render

Ce projet est une application web Python développée avec **Flask**, avec :
- **Tests automatisés** à chaque push sur GitHub (CI)
- **Déploiement automatique** sur **Render** (CD)

---

## 📁 Structure du projet

mon-projet/
├── main.py # Application Flask
├── test_app.py # Tests unitaires
├── requirements.txt # Dépendances
└── .github/
└── workflows/
└── ci.yaml # Pipeline GitHub Actions
---

## ✅ Fonctionnalités

- **Flask** pour créer l’application web
- **pytest** pour exécuter les tests unitaires
- **gunicorn** pour le déploiement en production
- **GitHub Actions** pour la CI
- **Render.com** pour le déploiement automatique

---

## ⚙️ Configuration GitHub Actions

- Déclencheur : `push` et `pull_request` sur la branche `main`
- Étapes :
  1. Cloner le code
  2. Installer Python
  3. Installer les dépendances (`requirements.txt`)
  4. Exécuter les tests (`pytest`)

---

## 🌐 Déploiement Render

- Type : Web Service
- Source : GitHub
- Branch : `main`
- Build command : `pip install -r requirements.txt`
- Start command : `gunicorn main:app`
- Variable d’environnement : `PORT=10000`

Le déploiement s’effectue automatiquement à chaque push sur `main`.

---

## 🧪 Exemple de test

Le fichier `test_app.py` vérifie que l'application répond bien à la racine `/` avec le message attendu et un code 200.

---

## 📦 Installation locale

```bash
pip install -r requirements.txt
python main.py
