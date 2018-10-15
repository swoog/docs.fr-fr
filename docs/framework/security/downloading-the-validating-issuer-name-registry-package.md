---
title: Téléchargement du package de validation du registre des noms d'émetteurs
ms.date: 10/10/2018
ms.assetid: ff8b0014-c5d4-4614-90f0-13fcc0ba777a
ms.openlocfilehash: 833a0722fdd27df4e488ed7fac99444c6d9b8905
ms.sourcegitcommit: d88024e6d6d8b242feae5f4007a709379355aa24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2018
ms.locfileid: "49316184"
---
# <a name="download-the-validating-issuer-name-registry-package"></a>Télécharger le Package de Registre de nom émetteur lors de la validation

Cette rubrique explique comment télécharger et utiliser le Registre des noms d’émetteurs de validation (VINR, Validating Issuer Name Registry) dans votre projet.

Le Registre VINR est disponible sous forme de package NuGet, qui ajoute les assemblys et les références nécessaires à votre projet. Si vous n’avez pas encore installé NuGet, accédez à [nuget.org](https://nuget.org) pour l’installer. Vous pouvez voir l’historique de gestion de version de l’extension en accédant à sa page sur NuGet : [Registre des noms d’émetteurs de validation Microsoft sur NuGet](https://nuget.org/packages/System.IdentityModel.Tokens.ValidatingIssuerNameRegistry/)

## <a name="use-the-package-manager-gui"></a>Utiliser l’interface utilisateur graphique du Gestionnaire de Package

1. Dans Visual Studio, cliquez sur votre projet dans l’**Explorateur de solutions**, puis sélectionnez **Gérer les packages NuGet**.

2. Dans la fenêtre **Gérer les packages NuGet**, cliquez sur la zone de recherche et tapez `ValidatingIssuerNameRegistry`, puis appuyez sur **Entrée**.

3. Dans le volet de résultats, cliquez sur le bouton **Installer** pour le premier résultat.

4. Le téléchargement du package commence. Avant l’ajout du package à votre projet, la boîte de dialogue d’acceptation de licence s’affiche. Si vous êtes d’accord avec les termes du contrat de licence, cliquez sur **Accepter**.

5. Les assemblys VINR les plus récents seront téléchargés et ajoutés à votre projet.

## <a name="use-the-package-manager-console"></a>Utilisez la Console du Gestionnaire de Package

1. Dans Visual Studio, cliquez sur **outils** > **Gestionnaire de Package NuGet** > **Console du Gestionnaire de Package**.

2. La **Console du Gestionnaire de package** s’affiche. Tapez le texte suivant et appuyez sur **Entrée** :

    ```powershell
    Install-Package System.IdentityModel.Tokens.ValidatingIssuerNameRegistry
    ```

3. Les assemblys VINR les plus récents seront téléchargés et ajoutés à votre projet.