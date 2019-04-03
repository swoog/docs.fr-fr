---
title: Développement rapide d'application avec My.Resources et My.Settings (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- My.Settings object [Visual Basic], developing applications
- rapid application development (RAD), My.Resources
- rapid application development (RAD), My.Settings
- My.Resources object [Visual Basic], developing applications
ms.assetid: 68284ab1-b685-4814-a2a4-01ae40445ff8
ms.openlocfilehash: 4a9021af23200323397cc49fa1a44a0cc48b5a1d
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58816705"
---
# <a name="rapid-application-development-with-myresources-and-mysettings-visual-basic"></a>Développement rapide d'application avec My.Resources et My.Settings (Visual Basic)
Le `My.Resources` objet fournit l’accès aux ressources de l’application et vous permet de récupérer dynamiquement des ressources pour votre application.  
  
## <a name="retrieving-resources"></a>Récupération de ressources  
 Un nombre de ressources, telles que des fichiers audio, les icônes, les images et les chaînes peut être récupéré via la `My.Resources` objet. Par exemple, vous pouvez accéder les fichiers de ressources spécifiques à la culture de l’application. L’exemple suivant définit l’icône du formulaire à l’icône nommée `Form1Icon` stockées dans le fichier de ressources de l’application.  
  
 [!code-vb[VbVbcnMy#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMy/VB/Class1.vb#7)]  
  
 Le `My.Resources` objet expose uniquement les ressources globales. Il ne donne pas accès aux fichiers de ressources associés aux formulaires. Vous devez accéder à des ressources du formulaire à partir du formulaire.  
  
 De même, le `My.Settings` objet fournit l’accès aux paramètres de l’application et vous permet de stocker et récupérer des paramètres de propriété et d’autres informations pour votre application de manière dynamique. Pour plus d’informations, consultez [My.Resources (objet)](../../../visual-basic/language-reference/objects/my-resources-object.md) et [My.Settings, objet](../../../visual-basic/language-reference/objects/my-settings-object.md).  
  
## <a name="see-also"></a>Voir aussi

- [My.Resources (objet)](../../../visual-basic/language-reference/objects/my-resources-object.md)
- [My.Settings (objet)](../../../visual-basic/language-reference/objects/my-settings-object.md)
- [Accès aux paramètres d’application](../../../visual-basic/developing-apps/programming/app-settings/index.md)
