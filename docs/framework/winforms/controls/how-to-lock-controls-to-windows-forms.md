---
title: 'Procédure : verrouiller des contrôles avec des Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, locking
- controls [Windows Forms], locking
ms.assetid: 94efe0d2-c14e-4d14-b903-63ea9b07e290
ms.openlocfilehash: ac5fbf33564ed2dd1a030132a35b36164f777519
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59301696"
---
# <a name="how-to-lock-controls-to-windows-forms"></a>Procédure : verrouiller des contrôles avec des Windows Forms
Lorsque vous concevez l’interface utilisateur (IU) de votre application Windows, vous pouvez verrouiller les contrôles une fois qu’ils sont correctement placés, afin que vous ne pas par inadvertance de déplacer ou de les redimensionner lors de la définition d’autres propriétés.  
  
 En outre, vous pouvez verrouiller et déverrouiller tous les contrôles sur le formulaire à la fois, ce qui est utile pour les formulaires avec de nombreux contrôles, ou vous pouvez déverrouiller des contrôles individuels. Une fois que vous avez passé tous les contrôles où vous le souhaitez sur le formulaire, les verrouiller tout en place pour empêcher un mouvement erroné.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-lock-a-control"></a>Pour verrouiller un contrôle  
  
1. Dans le **propriétés** fenêtre, cliquez sur le **verrouillé** propriété et sélectionnez `true`. (Double-cliquez sur le nom Active ou désactive le paramètre de propriété.)  
  
     Ou bien, cliquez sur le contrôle et choisissez **verrouille les contrôles**.  
  
    > [!NOTE]
    >  Contrôles de verrouillage empêche les glissé vers une nouvelle taille ou l’emplacement sur l’aire de conception. Toutefois, vous pouvez toujours modifier la taille ou l’emplacement des contrôles au moyen de la **propriétés** fenêtre ou dans le code.  
  
### <a name="to-lock-all-the-controls-on-a-form"></a>Pour verrouiller tous les contrôles sur un formulaire  
  
1. À partir de la **Format** menu, choisissez **verrouille les contrôles**.  
  
    > [!NOTE]
    >  Cette commande verrouille la taille du formulaire, car un formulaire est un contrôle.  
  
### <a name="to-unlock-all-locked-controls-on-a-form"></a>Pour déverrouiller verrouillés tous les contrôles sur un formulaire  
  
1. À partir de la **Format** menu, choisissez **verrouille les contrôles**.  
  
     Tous les contrôles précédemment verrouillés sur le formulaire sont maintenant déverrouillée.  
  
### <a name="to-unlock-locked-controls-individually"></a>Pour déverrouiller les contrôles verrouillés individuellement  
  
1. Dans le **propriétés** fenêtre, cliquez sur le **verrouillé** propriété et sélectionnez `false`. (Double-cliquez sur le nom Active ou désactive le paramètre de propriété.)  
  
## <a name="see-also"></a>Voir aussi

- [Contrôles Windows Forms](index.md)
- [Disposition des contrôles dans les Windows Forms](arranging-controls-on-windows-forms.md)
- [Création d'étiquettes et de raccourcis pour les contrôles Windows Forms](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)
- [Classement par fonction des contrôles Windows Forms](windows-forms-controls-by-function.md)
