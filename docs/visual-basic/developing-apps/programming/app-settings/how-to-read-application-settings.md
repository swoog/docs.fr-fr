---
title: 'Procédure : lire des paramètres d’application en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- reading application settings
- My.Settings object [Visual Basic], reading application settings
- application settings [Visual Basic], reading
ms.assetid: eb3428ef-115e-49a8-a878-e0613183fee0
ms.openlocfilehash: 032e06e674f2298d68f879f3ad474c79e3ff02db
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54659495"
---
# <a name="how-to-read-application-settings-in-visual-basic"></a>Procédure : lire des paramètres d’application en Visual Basic
Vous pouvez lire un paramètre utilisateur en accédant à la propriété du paramètre dans l’objet `My.Settings`.  
  
 L’objet `My.Settings` expose chaque paramètre en tant que propriété. Le nom de la propriété est le même que le nom du paramètre et le type de la propriété est le même que le type du paramètre. La **portée** du paramètre indique si la propriété est en lecture seule. La propriété d’un paramètre de portée **Application** est en lecture seule, tandis que la propriété d’un paramètre de portée **Utilisateur** est en lecture/écriture. Pour plus d’informations, consultez [My.Settings, objet](../../../../visual-basic/language-reference/objects/my-settings-object.md).  
  
## <a name="example"></a>Exemple  
 Cet exemple affiche la valeur du paramètre `Nickname`.  
  
 [!code-vb[VbVbalrMyResources#14](../../../../visual-basic/developing-apps/programming/app-settings/codesnippet/VisualBasic/how-to-read-application-settings_1.vb)]  
  
 Pour que cet exemple fonctionne, votre application doit avoir un paramètre `Nickname` de type `String`. Pour plus d'informations, consultez [Gestion des paramètres d’une application (.NET)](/visualstudio/ide/managing-application-settings-dotnet).  
  
## <a name="see-also"></a>Voir aussi
- [My.Settings (objet)](../../../../visual-basic/language-reference/objects/my-settings-object.md)
- [Guide pratique pour modifier les paramètres utilisateur en Visual Basic](../../../../visual-basic/developing-apps/programming/app-settings/how-to-change-user-settings.md)
- [Guide pratique pour rendre persistants les paramètres utilisateur en Visual Basic](../../../../visual-basic/developing-apps/programming/app-settings/how-to-persist-user-settings.md)
- [Guide pratique pour créer des grilles de propriétés pour les paramètres utilisateur en Visual Basic](../../../../visual-basic/developing-apps/programming/app-settings/how-to-create-property-grids-for-user-settings.md)
- [Gestion des paramètres d’une application (.NET)](/visualstudio/ide/managing-application-settings-dotnet)
