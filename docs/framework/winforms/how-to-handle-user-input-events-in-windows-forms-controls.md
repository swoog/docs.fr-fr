---
title: 'Procédure : gérer les événements d’entrée utilisateur dans des contrôles Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms controls, user input
- user input [Windows Forms], Windows Forms controls
ms.assetid: 3de74dcf-fae3-42d0-92b5-bc04a61a6888
ms.openlocfilehash: 5dc1997dffc53632ce8b36bc5fe89e768871fd0f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59108665"
---
# <a name="how-to-handle-user-input-events-in-windows-forms-controls"></a>Procédure : gérer les événements d’entrée utilisateur dans des contrôles Windows Forms
Cet exemple montre comment gérer la plupart des événements de clavier, de souris, de focus et de validation qui peuvent se produire dans un contrôle Windows Forms. La zone de texte nommée `TextBoxInput` reçoit les événements quand elle a le focus et les informations relatives à chaque événement sont écrites dans la zone de texte nommée `TextBoxOutput` dans l'ordre dans lequel les événements sont déclenchés. L'application comprend également un ensemble de cases à cocher qui peuvent servir à filtrer les événements pour lesquels établir un rapport.  
  
## <a name="example"></a>Exemple  
 [!code-cpp[System.Windows.Forms.UserInputWalkthrough#0](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.UserInputWalkthrough/cpp/form1.cpp#0)]
 [!code-csharp[System.Windows.Forms.UserInputWalkthrough#0](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.UserInputWalkthrough/CS/form1.cs#0)]
 [!code-vb[System.Windows.Forms.UserInputWalkthrough#0](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.UserInputWalkthrough/VB/form1.vb#0)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   des références aux assemblys System, System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="see-also"></a>Voir aussi

- [Entrées d’utilisateur dans les Windows Forms](user-input-in-windows-forms.md)
