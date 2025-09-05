# CoffreMP v2 — Gestionnaire de mots de passe sécurisé

<p align="center">
  <img src="docs/cover.png" alt="CoffreMP v2 – cover" width="950">
</p>

<p align="center">
  <a href="../../releases/latest/">
    <img src="https://img.shields.io/badge/version-v2.0-6366f1?style=for-the-badge" alt="version">
  </a>
  <a href="LICENSE">
    <img src="https://img.shields.io/badge/license-MIT-22c55e?style=for-the-badge" alt="license">
  </a>
  <img src="https://img.shields.io/badge/platform-Windows%2010%2F11-0ea5e9?style=for-the-badge" alt="platform">
  <img src="https://img.shields.io/badge/made%20with-Python%203.10%2B-10b981?style=for-the-badge" alt="python">
</p>

<p align="center">
  <a href="https://coffrefort.ilyox.fr">
    <img src="https://img.shields.io/badge/TÉLÉCHARGER-CoffreMP%20v2.exe-4f46e5?style=for-the-badge&logo=windows" alt="download">
  </a>
</p>

> **CoffreMP v2** est un gestionnaire de mots de passe **100% local**, avec **double authentification par e-mail (OTP)**, **chiffrement fort (Argon2id + Fernet)**, **auto-login (Selenium)** et une interface moderne.  
> Téléchargez, lancez : **pas de cloud, vos données restent chez vous**.

---

## 🧭 Sommaire

- [Fonctionnalités](#-fonctionnalités)
- [Aperçu](#-aperçu)
- [Téléchargement](#-téléchargement)
- [Prise en main rapide](#-prise-en-main-rapide)
- [Sécurité & confidentialité](#-sécurité--confidentialité)
- [Emplacement des données](#-emplacement-des-données)
- [Pré-requis auto-login](#-pré-requis-auto-login)
- [Dépannage](#-dépannage)
- [Checksums](#-checksums)
- [Roadmap](#-roadmap)
- [Contribuer](#-contribuer)
- [Licence](#-licence)

---

## ✨ Fonctionnalités

<table>
<tr>
<td width="33%">
<b>🔐 Chiffrement sérieux</b><br>
<sub>Coffre chiffré en <b>Fernet (AES + HMAC)</b>. Clé dérivée par <b>Argon2id</b> avec sel aléatoire.</sub>
</td>
<td width="33%">
<b>📧 2FA par e-mail (OTP)</b><br>
<sub>À chaque connexion, un <b>code à 6 chiffres</b> est requis (valide 5 min).</sub>
</td>
<td width="33%">
<b>⚡ Auto-login</b><br>
<sub>Ouvre le site, remplit <b>login + mot de passe</b>, tente la connexion (via Selenium).</sub>
</td>
</tr>
<tr>
<td>
<b>🗂️ Gestion simple</b><br>
<sub>Nom, identifiant, mot de passe (générateur), URL, notes, recherche instantanée.</sub>
</td>
<td>
<b>📋 Copie protégée</b><br>
<sub>Effacement automatique du presse-papiers après délai (20s par défaut).</sub>
</td>
<td>
<b>💾 Sauvegardes</b><br>
<sub>Export / import <i>toujours chiffré</i> pour déplacer votre coffre en toute sécurité.</sub>
</td>
</tr>
</table>

---

## 👀 Aperçu

<p align="center">
  <img src="docs/screenshot-login.png" alt="Écran de connexion" width="47%">
  <img src="docs/screenshot-vault.svg" alt="Coffre & détails" width="47%">
</p>

> Placez vos captures dans `docs/` (remplacez les fichiers si besoin).

---

## 🔽 Téléchargement

- **Windows (EXE autonome)**  
  👉 **[Télécharger CoffreMP v2](https://coffrefort.ilyox.fr/)**  
 
**Vérifier l’intégrité (recommandé)**
## 🧱 Sécurité & confidentialité

- Le mot de passe maître n’est jamais stocké (seul un hash Argon2id + sel est conservé pour la vérification).

- Le coffre (vault.json) est intégralement chiffré (Fernet).

- L’OTP est en mémoire uniquement et expire après 5 minutes.

- Aucune donnée n’est synchronisée ni collectée — seul l’e-mail OTP transite.

**⚠️ Si vous perdez votre mot de passe maître, il est impossible de récupérer vos données (c’est voulu, par sécurité).**

                                                           --<svg xmlns="http://www.w3.org/2000/svg" width="1600" height="600">
  <defs>
    <linearGradient id="g" x1="0" x2="1" y1="0" y2="1">
      <stop offset="0%" stop-color="#0f172a"/>
      <stop offset="100%" stop-color="#1e293b"/>
    </linearGradient>
  </defs>
  <rect width="100%" height="100%" fill="url(#g)"/>
  <g font-family="Segoe UI, Inter, Arial" fill="#e5e7eb" text-anchor="middle">
    <text x="800" y="280" font-size="90" font-weight="700">CoffreMP v2</text>
    <text x="800" y="360" font-size="32" fill="#93c5fd">Gestionnaire de mots de passe sécurisé</text>
  </g>
  <circle cx="1400" cy="130" r="90" fill="#4f46e5" opacity="0.25"/>
  <circle cx="200" cy="500" r="120" fill="#22d3ee" opacity="0.2"/>
</svg>



<svg xmlns="http://www.w3.org/2000/svg" width="1200" height="750">
  <rect width="100%" height="100%" fill="#0f172a"/>
  <rect x="150" y="80" width="900" height="590" rx="24" fill="#111827" stroke="#334155" stroke-width="3"/>
  <text x="600" y="170" font-family="Segoe UI, Inter" font-size="38" fill="#e5e7eb" text-anchor="middle" font-weight="600">
    Écran de connexion
  </text>
  <rect x="300" y="240" width="600" height="56" rx="12" fill="#0b1220" stroke="#334155"/>
  <rect x="300" y="316" width="600" height="56" rx="12" fill="#0b1220" stroke="#334155"/>
  <rect x="470" y="410" width="260" height="50" rx="12" fill="#4f46e5"/>
  <text x="600" y="445" font-family="Segoe UI, Inter" font-size="20" fill="#ffffff" text-anchor="middle">Envoyer code & Continuer</text>
</svg>


<svg xmlns="http://www.w3.org/2000/svg" width="1200" height="750">
  <rect width="100%" height="100%" fill="#0f172a"/>
  <rect x="80" y="70" width="1040" height="610" rx="24" fill="#111827" stroke="#334155" stroke-width="3"/>
  <text x="600" y="130" font-family="Segoe UI, Inter" font-size="38" fill="#e5e7eb" text-anchor="middle" font-weight="600">
    Coffre & Détails
  </text>
  <rect x="120" y="180" width="640" height="420" rx="12" fill="#1e293b" stroke="#475569"/>
  <rect x="790" y="180" width="290" height="420" rx="12" fill="#0b1220" stroke="#334155"/>
  <rect x="140" y="200" width="600" height="40" fill="#0f172a"/>
  <text x="160" y="227" font-family="Segoe UI, Inter" font-size="16" fill="#facc15">Nom</text>
  <text x="300" y="227" font-family="Segoe UI, Inter" font-size="16" fill="#facc15">Identifiant</text>
  <text x="500" y="227" font-family="Segoe UI, Inter" font-size="16" fill="#facc15">URL</text>
  <text x="620" y="227" font-family="Segoe UI, Inter" font-size="16" fill="#facc15">Modifié</text>
  <rect x="810" y="210" width="250" height="36" rx="8" fill="#0b1220" stroke="#334155"/>
  <rect x="810" y="260" width="250" height="36" rx="8" fill="#0b1220" stroke="#334155"/>
  <rect x="810" y="310" width="250" height="36" rx="8" fill="#0b1220" stroke="#334155"/>
  <rect x="840" y="360" width="190" height="40" rx="10" fill="#4f46e5"/>
  <text x="935" y="386" font-family="Segoe UI, Inter" font-size="18" fill="#fff" text-anchor="middle">Se connecter (auto)</text>
</svg>

                                                       
