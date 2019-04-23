---
title: 'Procédure : ajouter plusieurs jeux de paramètres à votre application en C#'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], multiple sets
- application settings [Windows Forms], C#
ms.assetid: 45007ac6-cf07-4be7-bc38-3f0ef962faf9
ms.openlocfilehash: 9a4913f635204aac2214d97225c7b8147c6fe9ab
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59326604"
---
# <a name="how-to-add-multiple-sets-of-settings-to-your-application-in-c"></a>Procédure : Ajouter plusieurs jeux de paramètres à votre Application en C\#
Dans certains cas, vous souhaiterez avoir plusieurs jeux de paramètres dans une application. Par exemple, si vous développez une application où un groupe particulier de paramètres est amené à changer fréquemment, il peut être judicieux de les placer dans un seul fichier afin que le fichier puisse être remplacé globalement, sans affecter les autres paramètres. Visual Studio permet d’ajouter plusieurs jeux de paramètres à votre projet. Ensembles de paramètres supplémentaires sont accessibles via l’objet Properties.Settings.  
  
### <a name="to-add-an-additional-set-of-setting-to-your-application"></a>Pour ajouter un jeu supplémentaire de paramètres à votre Application  
  
1. Dans le menu **Projet**, sélectionnez **Ajouter un nouvel élément**. La boîte de dialogue **Ajouter un nouvel élément** s’ouvre.  
  
2. Dans le **ajouter un nouvel élément** boîte de dialogue, sélectionnez **fichier de paramètres**, tapez un nom pour le fichier, puis cliquez sur **ajouter** pour ajouter un nouveau fichier de paramètres à votre solution.  
  
3. Dans **l’Explorateur de solutions**, faites glisser le nouveau fichier de paramètres dans le **propriétés** dossier. Ainsi, vos nouveaux paramètres soient disponibles dans le code.  
  
4. Ajouter et utiliser des paramètres dans ce fichier comme vous le feriez pour tout autre fichier de paramètres. Vous pouvez accéder à ce groupe de paramètres via l’objet Properties.Settings.  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation de paramètres d'application et de paramètres utilisateur](using-application-settings-and-user-settings.md)
- [Vue d'ensemble des paramètres d'application](application-settings-overview.md)
