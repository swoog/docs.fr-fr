---
title: 'Procédure : Énumérer un sous-ensemble de files d’attente à l’impression'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- enumerating [WPF], subset of print queues
- print queues [WPF], enumerating subset of
ms.assetid: cc4a1b5b-d46f-4c5e-bc26-22c226e4bee0
ms.openlocfilehash: adcfff0196bd0430ec1ae563fbd5489062de11f3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59217183"
---
# <a name="how-to-enumerate-a-subset-of-print-queues"></a>Procédure : Énumérer un sous-ensemble de files d’attente à l’impression
Une situation courante rencontrée par les professionnels de l’informatique (IT) gère un ensemble d’échelle de la société des imprimantes consiste à générer une liste des imprimantes présentant certaines caractéristiques. Cette fonctionnalité est fournie par le <xref:System.Printing.PrintServer.GetPrintQueues%2A> méthode d’un <xref:System.Printing.PrintServer> objet et le <xref:System.Printing.EnumeratedPrintQueueTypes> énumération.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple ci-dessous, le code commence par créer un tableau d’indicateurs qui spécifient les caractéristiques des files d’attente que nous souhaitons liste. Dans cet exemple, nous recherchons des files d’attente à l’impression qui sont installées localement sur le serveur d’impression et sont partagés. Le <xref:System.Printing.EnumeratedPrintQueueTypes> énumération offre de nombreuses autres possibilités.  
  
 Le code crée ensuite un <xref:System.Printing.LocalPrintServer> de l’objet, une classe dérivée de <xref:System.Printing.PrintServer>. Le serveur d’impression local est l’ordinateur sur lequel l’application est en cours d’exécution.  
  
 La dernière étape importante consiste à passer le tableau à la <xref:System.Printing.PrintServer.GetPrintQueues%2A> (méthode).  
  
 Enfin, les résultats sont présentés à l’utilisateur.  
  
 [!code-cpp[EnumerateSubsetOfPrintQueues#ListSubsetOfPrintQueues](~/samples/snippets/cpp/VS_Snippets_Wpf/EnumerateSubsetOfPrintQueues/CPP/Program.cpp#listsubsetofprintqueues)]
 [!code-csharp[EnumerateSubsetOfPrintQueues#ListSubsetOfPrintQueues](~/samples/snippets/csharp/VS_Snippets_Wpf/EnumerateSubsetOfPrintQueues/CSharp/Program.cs#listsubsetofprintqueues)]
 [!code-vb[EnumerateSubsetOfPrintQueues#ListSubsetOfPrintQueues](~/samples/snippets/visualbasic/VS_Snippets_Wpf/EnumerateSubsetOfPrintQueues/visualbasic/program.vb#listsubsetofprintqueues)]  
  
 Vous pouvez étendre cet exemple en ayant la `foreach` boucle qui parcourt chaque file d’attente d’impression faire davantage de filtrage. Par exemple, vous pourriez filtrer les imprimantes qui ne prennent pas en charge impression recto-verso en demandant à l’appel de la boucle chaque file d’attente à l’impression <xref:System.Printing.PrintQueue.GetPrintCapabilities%2A> (méthode) et test, la valeur retournée pour la présence de l’impression recto verso.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Printing.PrintServer.GetPrintQueues%2A>
- <xref:System.Printing.PrintServer>
- <xref:System.Printing.LocalPrintServer>
- <xref:System.Printing.EnumeratedPrintQueueTypes>
- <xref:System.Printing.PrintQueue>
- <xref:System.Printing.PrintQueue.GetPrintCapabilities%2A>
- [Documents dans WPF](documents-in-wpf.md)
- [Vue d'ensemble de l'impression](printing-overview.md)
- [Microsoft XPS Document Writer](https://go.microsoft.com/fwlink/?LinkId=147319)
