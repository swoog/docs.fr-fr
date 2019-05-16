---
title: Téléchargement du package du Gestionnaire de jetons Web JSON
ms.date: 10/10/2018
ms.assetid: d12b3f5b-f1f1-4a9d-a159-0c13e5976c90
ms.openlocfilehash: a8685a71d46778d932595965f32c0041b176bd83
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65633524"
---
# <a name="download-the-json-web-token-handler-package"></a>Télécharger le Package du Gestionnaire de jetons Web JSON

Cette rubrique explique comment télécharger et utiliser le Gestionnaire de jetons Web JSON dans votre projet.

L’extension du Gestionnaire de jetons Web JSON est disponible sous forme de package NuGet, qui ajoute les assemblys et les références nécessaires à votre projet. Si vous n’avez pas encore installé NuGet, accédez à [nuget.org](https://nuget.org) pour l’installer. Vous pouvez consulter l’historique de contrôle de version pour l’extension en visitant sa page sur NuGet : [Gestionnaire de jetons Web JSON sur NuGet](https://www.nuget.org/packages/System.IdentityModel.Tokens.Jwt/)

## <a name="use-the-package-manager-gui"></a>Utiliser l’interface utilisateur graphique du Gestionnaire de Package

1. Dans Visual Studio, cliquez sur votre projet dans l’**Explorateur de solutions**, puis sélectionnez **Gérer les packages NuGet**.

2. Dans la fenêtre **Gérer les packages NuGet**, cliquez sur la zone de recherche et tapez `JWT Token Handler`, puis appuyez sur **Entrée**.

3. Dans le volet de résultats, cliquez sur le bouton **Installer** pour le premier résultat.

4. Le téléchargement du package commence. Avant l’ajout du package à votre projet, la boîte de dialogue d’acceptation de licence s’affiche. Si vous êtes d’accord avec les termes du contrat de licence, cliquez sur **Accepter**.

5. Les assemblys du Gestionnaire de jetons Web JSON les plus récents seront téléchargés et ajoutés à votre projet.

## <a name="use-the-package-manager-console"></a>Utilisez la Console du Gestionnaire de Package

1. Dans Visual Studio, cliquez sur **outils** > **Gestionnaire de Package NuGet** > **Console du Gestionnaire de Package**.

2. La **Console du Gestionnaire de package** s’affiche. Tapez le texte suivant et appuyez sur **Entrée** :

    ```powershell
    Install-Package System.IdentityModel.Tokens.Jwt
    ```

3. Les assemblys du Gestionnaire de jetons Web JSON les plus récents seront téléchargés et ajoutés à votre projet.
