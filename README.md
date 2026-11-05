<div align="center">

# Budget

**Ton budget personnel, sur ton ordinateur et ton téléphone. Tes données restent chez toi.**

Tu importes les relevés de ta banque (CSV BoursoBank) ou tu saisis tes opérations ; Budget les classe, compare le
réel au prévu mois par mois, suit ton épargne et, si tu veux, ton portefeuille de bourse.

### [⬇️ Télécharger pour Mac](https://github.com/Jklmooo/budget-releases/releases/latest/download/Budget.dmg) · [⬇️ Télécharger pour Windows](https://github.com/Jklmooo/budget-releases/releases/latest/download/Budget-Setup.exe)

<sub>Gratuit · sans compte · aucune donnée envoyée · [toutes les versions](https://github.com/Jklmooo/budget-releases/releases)</sub>

</div>

---

## Installer

### Mac

1. Ouvre `Budget.dmg` et glisse **Budget** dans **Applications**.
2. Ouvre Budget. macOS la bloque la première fois, car elle n'est pas signée par un compte développeur Apple :
   **Réglages Système → Confidentialité et sécurité → Ouvrir quand même**, puis rouvre-la.
3. À la première ouverture, Budget s'installe dans ta bibliothèque, sans mot de passe. S'il n'y a pas de Python 3.12
   sur le Mac, environ 20 Mo sont téléchargés, une seule fois.

Ensuite, ouvrir l'app lance Budget en arrière-plan et l'ouvre dans ton navigateur.
Pour l'arrêter : bouton **Thème** (en haut à droite) → **Arrêter Budget**.

### Windows

1. Lance `Budget-Setup.exe`. Si SmartScreen s'affiche : **Informations complémentaires → Exécuter quand même**.
2. Budget s'installe pour ton compte seul, sans mot de passe administrateur, puis s'ouvre dans ton navigateur.
   S'il n'y a pas de Python 3.12, environ 20 Mo sont téléchargés, une seule fois.

Un raccourci **Budget** est créé sur le Bureau et dans le menu Démarrer. Pour l'arrêter : bouton **Thème** →
**Arrêter Budget**. On le désinstalle depuis **Paramètres → Applications** ; tes données restent dans
`%LOCALAPPDATA%\Programs\Budget\donnees`.

## Ce que fait Budget

- **Mois** : d'où vient l'argent, où il va, le reste à dépenser, chaque catégorie face à son prévu.
- **Plan** : prévus, échéances, objectifs d'épargne, catégories.
- **Tendances** : les derniers mois comparés, ou l'année mois par mois.
- **Bourse** : ton portefeuille à partir des exports BoursoBank (valeur, versements, performance, positions).
- **Journal** : ajouter, corriger, filtrer tes opérations ; importer un relevé, classé avant d'enregistrer.

Thèmes : Clair, Sombre, Nuit, Edgerunners, Sable.

## Sur le téléphone

Avec [Tailscale](https://tailscale.com/download) (gratuit) sur l'ordinateur et le téléphone, connectés au même
compte, lance une fois sur l'ordinateur :

```
tailscale serve --bg --https=8443 8790
```

puis ouvre sur le téléphone l'adresse affichée (`https://<ordinateur>.<ton-tailnet>.ts.net:8443`) et ajoute-la à
l'écran d'accueil. L'accès reste privé : seul ton compte Tailscale entre.

## Modules facultatifs

Bouton **Thème → Modules facultatifs**, à ajouter ou retirer quand tu veux :

- **Discussion avec une IA** : pose des questions sur tes dépenses et ton épargne, avec le modèle de ton choix (un
  agent comme Claude Code ou Mistral Vibe avec ton abonnement, un service en ligne avec ta clé, ou Ollama sur
  l'ordinateur). Il peut proposer de recatégoriser des opérations ou d'ajouter une règle ; rien ne change avant ta
  validation.
- **Finary** : importe les opérations de ton compte courant et garde ton PEA à jour, en lecture seule.

## Mises à jour

Budget se met à jour lui-même : bouton **Thème → Version → Mettre à jour** quand une nouvelle version existe. Tes
données et tes modules sont gardés. Pas besoin de retélécharger l'application.

## Tes données

Tout reste sur ton ordinateur : dans `~/Library/Application Support/Budget/app/donnees` (Mac) ou
`%LOCALAPPDATA%\Programs\Budget\donnees` (Windows). Rien ne part ailleurs, sauf ce que tu choisis : la lecture de ton
compte Finary si tu ajoutes ce module, et tes questions au service en ligne que tu choisis dans la Discussion.
