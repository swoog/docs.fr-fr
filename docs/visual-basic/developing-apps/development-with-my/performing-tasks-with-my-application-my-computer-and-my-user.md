---
title: Exécution de tâches avec My.Application, My.Computer et My.User (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- My.Application object [Visual Basic], developing applications
- rapid application development (RAD), My.Application
- rapid application development (RAD), My.Computer
- rapid application development (RAD), My.User
- My.Computer object [Visual Basic], developing applications
- My.User object [Visual Basic], developing applications
ms.assetid: c8af61bd-4dd3-4a0f-9af5-795b594b240b
ms.openlocfilehash: 0372fbf63f6d12e266674f92225183911aa4ca30
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58834039"
---
# <a name="performing-tasks-with-myapplication-mycomputer-and-myuser-visual-basic"></a>Exécution de tâches avec My.Application, My.Computer et My.User (Visual Basic)
Les trois central `My` sont des objets qui fournissent l’accès aux informations et couramment utilisé la fonctionnalité `My.Application` (<xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase>), `My.Computer` (<xref:Microsoft.VisualBasic.Devices.Computer>), et `My.User` (<xref:Microsoft.VisualBasic.ApplicationServices.User>). Vous pouvez utiliser ces objets pour accéder aux informations relatives à l’application actuelle, l’application est installée sur l’ordinateur ou l’utilisateur actuel de l’application, respectivement.  
  
## <a name="myapplication-mycomputer-and-myuser"></a>My.Application, My.Computer et My.User  
 Les exemples suivants montrent comment les informations peuvent être récupérées à l’aide `My`.  
  
 [!code-vb[VbVbcnMy#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMy/VB/Class1.vb#1)]  
  
 [!code-vb[VbVbcnMy#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMy/VB/Class1.vb#2)]  
  
 En plus de la récupération des informations, les membres exposés via ces trois objets vous permettent également d’exécuter des méthodes associées à cet objet. Par exemple, vous pouvez accéder à diverses méthodes pour manipuler des fichiers ou mettre à jour le Registre via `My.Computer`.  
  
 Fichier d’e/s est considérablement plus facile et plus rapide avec `My`, qui inclut une variété de méthodes et propriétés pour la manipulation de fichiers, répertoires et lecteurs. Le <xref:Microsoft.VisualBasic.FileIO.TextFieldParser> objet vous permet de lire à partir des fichiers volumineux structurés qui ont délimitées ou les champs de largeur fixe. Cet exemple ouvre le `TextFieldParser` `reader` et l’utilise pour lire à partir de `C:\TestFolder1\test1.txt`.  
  
 [!code-vb[VbVbalrTextFieldParser#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrTextFieldParser/VB/Class1.vb#23)]  
  
 `My.Application` vous permet de modifier la culture de votre application. L’exemple suivant montre comment cette méthode peut être appelée.  
  
 [!code-vb[VbVbcnMy#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMy/VB/Class1.vb#3)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase>
- <xref:Microsoft.VisualBasic.Devices.Computer>
- <xref:Microsoft.VisualBasic.ApplicationServices.User>
- [Comment My dépend du type de projet](../../../visual-basic/developing-apps/development-with-my/how-my-depends-on-project-type.md)
