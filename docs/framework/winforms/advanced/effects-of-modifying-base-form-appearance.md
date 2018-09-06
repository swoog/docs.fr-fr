---
title: Conséquences de la modification de l’aspect d’un formulaire de base
ms.date: 03/30/2017
helpviewer_keywords:
- parent forms [Windows Forms]
- inherited forms [Windows Forms], modifications to base form
- Windows Forms, base form appearance
- base forms
- inheritance [Windows Forms], forms
ms.assetid: 1c3f2b29-a05c-4c6f-aa1a-4e66b94f343a
ms.openlocfilehash: adaf9224fd340c6ea4342e2591806a7c877e83ff
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43746170"
---
# <a name="effects-of-modifying-a-base-form39s-appearance"></a>Conséquences de la modification de l’aspect d’un formulaire de base
Pendant le développement d’applications, vous êtes souvent amené à modifier l’apparence du formulaire de base dont héritent d’autres formulaires du projet (ou d’autres projets).  
  
 Au moment du design, les modifications apportées à l’aspect du formulaire de base (qu’il s’agisse de la définition de propriétés ou de l’addition et de la soustraction de contrôles) sont répercutées dans les formulaires hérités lors de la génération du projet contenant le formulaire de base. Il ne suffit pas d’enregistrer les modifications apportées au formulaire de base. Pour générer un projet, sélectionnez **Générer** dans le menu **Générer**.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
 Les modifications apportées au formulaire à l’exécution n’ont aucune incidence sur les formulaires hérités déjà instanciés.  
  
## <a name="see-also"></a>Voir aussi  
 [base](~/docs/csharp/language-reference/keywords/base.md)  
 [Comment : hériter des Windows Forms](../../../../docs/framework/winforms/advanced/how-to-inherit-windows-forms.md)  
 [Héritage visuel des Windows Forms](../../../../docs/framework/winforms/advanced/windows-forms-visual-inheritance.md)
