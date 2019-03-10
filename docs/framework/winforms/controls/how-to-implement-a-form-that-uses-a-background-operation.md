---
title: 'Procédure : Implémenter un formulaire qui utilise une opération d’arrière-plan'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- threading [Windows Forms], forms
- BackgroundWorker component
- background tasks
- forms [Windows Forms], multithreading
- components [Windows Forms], asynchronous
- forms [Windows Forms], background operations
- background threads
- threading [Windows Forms], background operations
- background operations
ms.assetid: 9f483f93-1613-4be1-a021-b4934e9c78f3
ms.openlocfilehash: 9fe514cce4d4aec386f9d61cb84f3a39273c35b0
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57723333"
---
# <a name="how-to-implement-a-form-that-uses-a-background-operation"></a>Procédure : Implémenter un formulaire qui utilise une opération d’arrière-plan
L'exemple de programme suivant crée un formulaire qui calcule les nombres de Fibonacci. Le calcul s'exécute sur un thread distinct du thread d'interface utilisateur, pour que l'interface utilisateur continue de s'exécuter sans délai lors du calcul.  
  
 Cette tâche est très bien prise en charge dans Visual Studio.  
  
 Consultez également [procédure pas à pas : Implémentation d’un formulaire qui utilise une opération d’arrière-plan](walkthrough-implementing-a-form-that-uses-a-background-operation.md).  
  
## <a name="example"></a>Exemple  
 [!code-cpp[System.ComponentModel.BackgroundWorker#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#1)]
 [!code-csharp[System.ComponentModel.BackgroundWorker#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System, System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="robust-programming"></a>Programmation fiable  
  
> [!CAUTION]
>  Quand vous utilisez le multithreading, vous vous exposez potentiellement à des bogues très sérieux et complexes. Consultez les [Meilleures pratiques pour le threading managé](../../../standard/threading/managed-threading-best-practices.md) avant d’implémenter une solution qui utilise le multithreading.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ComponentModel.BackgroundWorker>
- <xref:System.ComponentModel.DoWorkEventArgs>
- [Vue d’ensemble du modèle asynchrone basé sur les événements](../../../standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview.md)
- [Bonnes pratiques de threading géré](../../../standard/threading/managed-threading-best-practices.md)
