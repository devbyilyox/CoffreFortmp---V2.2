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
  <img src="1.png" alt="Écran de connexion" width="47%">
  <img src="2.png" alt="Coffre & détails" width="47%">
</p>


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

**🔐 Pour des raisons de sécurité , tout est stocké localement 




 
