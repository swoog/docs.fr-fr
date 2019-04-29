---
title: 'Procédure : Ajouter un écran de démarrage dans une application WPF'
ms.date: 08/18/2018
helpviewer_keywords:
- WPF [WPF], splash screen
- startup window [WPF]
- SplashScreen class [WPF]
- splash screen [WPF]
ms.assetid: d70a25c4-5fb9-4c27-b01d-b1b8ef39b3fd
ms.openlocfilehash: 3120ee64d65822d323800a89466c6b707169aaaa
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61947899"
---
# <a name="how-to-add-a-splash-screen-to-a-wpf-application"></a>Procédure : Ajouter un écran de démarrage dans une application WPF

Cette rubrique montre comment ajouter une fenêtre de démarrage, ou *écran de démarrage*, à une application Windows Presentation Foundation (WPF).

## <a name="to-add-an-existing-image-as-a-splash-screen"></a>Pour ajouter une image existante en tant qu’un écran de démarrage

1. Créer ou rechercher une image que vous souhaitez utiliser pour l’écran de démarrage. Vous pouvez utiliser n’importe quel format d’image pris en charge par le composant WIC (Windows Imaging Component). Par exemple, vous pouvez utiliser le format BMP, GIF, JPEG, PNG ou TIFF.

2. Ajoutez le fichier image au projet d’Application WPF.

3. Dans **l’Explorateur de solutions**, sélectionnez l’image.

4. Dans la fenêtre Propriétés, cliquez sur la flèche déroulante pour le **Action de génération** propriété.

5. Sélectionnez **SplashScreen** dans la liste déroulante.

6. Appuyez sur **F5** pour générer et exécuter l’application.

     L’image d’écran de démarrage s’affiche dans le centre de l’écran, puis disparaît lorsque la fenêtre principale de l’application s’affiche.

## <a name="to-exclude-the-splash-screen-from-build"></a>Pour exclure de l’écran de démarrage à partir de la build

1. Dans **l’Explorateur de solutions**, sélectionnez l’image d’écran de démarrage.

2. Dans le **propriétés** fenêtre, définissez la **Action de génération** à **aucun**.

## <a name="to-remove-the-splash-screen-from-an-application"></a>Pour supprimer l’écran de démarrage à partir d’une application

Dans **l’Explorateur de solutions**, supprimez l’image d’écran de démarrage.

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.SplashScreen>
- [Guide pratique pour Ajouter des éléments existants à un projet](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100))
