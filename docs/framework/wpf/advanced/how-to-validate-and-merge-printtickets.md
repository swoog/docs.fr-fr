---
title: 'Procédure : Valider et fusionner des PrintTicket'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- merging PrintTickets [WPF]
- PrintTicket [WPF], merging
- validation of PrintTickets [WPF]
- PrintTicket [WPF], validation
ms.assetid: 4fe2d501-d0b0-4fef-86af-6ffe6c162532
ms.openlocfilehash: 750234a7073b3931b4f3ce5674f3989fe119c50c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59199945"
---
# <a name="how-to-validate-and-merge-printtickets"></a>Procédure : Valider et fusionner des PrintTicket
Le [!INCLUDE[TLA#tla_win](../../../../includes/tlasharptla-win-md.md)] [schéma d’impression](https://go.microsoft.com/fwlink/?LinkId=186397) inclut flexible et extensible <xref:System.Printing.PrintCapabilities> et <xref:System.Printing.PrintTicket> éléments. Le premier comptabilise les fonctions d’un périphérique d’impression, et ce dernier spécifie comment l’appareil doit utiliser ces fonctionnalités par rapport à une séquence particulière de documents, de document individuel ou de page individuelle.  
  
 Une séquence de tâches pour une application qui prend en charge l’impression typique se présente comme suit.  
  
1.  Déterminer les fonctionnalités d’une imprimante.  
  
2.  Configurer un <xref:System.Printing.PrintTicket> d’utiliser ces fonctionnalités.  
  
3.  Valider le <xref:System.Printing.PrintTicket>.  
  
 Cet article explique comment effectuer cette opération.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple ci-dessous, nous sommes intéressés uniquement si une imprimante peut prendre en charge, l’impression recto-verso. Les principales étapes sont les suivantes.  
  
1.  Obtenir un <xref:System.Printing.PrintCapabilities> de l’objet avec le <xref:System.Printing.PrintQueue.GetPrintCapabilities%2A> (méthode).  
  
2.  Tester la présence de la fonctionnalité souhaitée. Dans l’exemple ci-dessous, nous testons la <xref:System.Printing.PrintCapabilities.DuplexingCapability%2A> propriété de la <xref:System.Printing.PrintCapabilities> la présence de la fonction d’impression sur les deux côtés d’une feuille de papier avec la rotation de « page » de l’objet le long du côté long de la feuille. Dans la mesure où <xref:System.Printing.PrintCapabilities.DuplexingCapability%2A> est une collection, nous utilisons le `Contains` méthode de <xref:System.Collections.ObjectModel.ReadOnlyCollection%601>.  
  
    > [!NOTE]
    >  Cette étape n’est pas strictement nécessaire. Le <xref:System.Printing.PrintQueue.MergeAndValidatePrintTicket%2A> méthode ci-dessous vérifie chaque demande le <xref:System.Printing.PrintTicket> aux capacités de l’imprimante. Si la fonction demandée n’est pas pris en charge par l’imprimante, le pilote d’imprimante remplacera une autre demande dans le <xref:System.Printing.PrintTicket> retourné par la méthode.  
  
3.  Si l’imprimante prend en charge l’impression recto verso, l’exemple de code crée un <xref:System.Printing.PrintTicket> qui demande la copie recto verso. Mais l’application ne spécifie pas de chaque paramètre disponible dans l’imprimante possible le <xref:System.Printing.PrintTicket> élément. Qui serait une perte de programmeur et durée du programme. Au lieu de cela, le code définit uniquement la demande d’impression recto verso et puis fusionne ce <xref:System.Printing.PrintTicket> avec un existant, entièrement configuré et validé, <xref:System.Printing.PrintTicket>, dans ce cas, par défaut de l’utilisateur <xref:System.Printing.PrintTicket>.  
  
4.  En conséquence, l’exemple appelle la <xref:System.Printing.PrintQueue.MergeAndValidatePrintTicket%2A> méthode pour fusionner la nouvelle minime, <xref:System.Printing.PrintTicket> valeur par défaut de l’utilisateur <xref:System.Printing.PrintTicket>. Cette commande renvoie un <xref:System.Printing.ValidationResult> qui inclut la nouvelle <xref:System.Printing.PrintTicket> comme l’un de ses propriétés.  
  
5.  L’exemple vérifie ensuite que la nouvelle <xref:System.Printing.PrintTicket> demande l’impression recto verso. Le cas échéant, puis l’exemple rend le nouveau ticket d’impression par défaut pour l’utilisateur. Si l’étape 2 ci-dessus avait été ignorée et l’imprimante ne prenait pas en charge impression recto verso le long du côté long, le test aurait dans `false`. (Voir la Remarque ci-dessus.)  
  
6.  La dernière étape importante consiste à valider la modification apportée à la <xref:System.Printing.PrintQueue.UserPrintTicket%2A> propriété de la <xref:System.Printing.PrintQueue> avec la <xref:System.Printing.PrintQueue.Commit%2A> (méthode).  
  
 [!code-csharp[PrintTicketManagment#UsingMergeAndValidate](~/samples/snippets/csharp/VS_Snippets_Wpf/PrintTicketManagment/CSharp/printticket.cs#usingmergeandvalidate)]
 [!code-vb[PrintTicketManagment#UsingMergeAndValidate](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PrintTicketManagment/visualbasic/printticket.vb#usingmergeandvalidate)]  
  
 Afin que vous pouvez rapidement tester cet exemple, le reste de celle-ci est présenté ci-dessous. Créer un projet et un espace de noms, puis collez les deux extraits de code dans cet article dans le bloc d’espace de noms.  
  
 [!code-csharp[PrintTicketManagment#UIForMergeAndValidatePTUtility](~/samples/snippets/csharp/VS_Snippets_Wpf/PrintTicketManagment/CSharp/printticket.cs#uiformergeandvalidateptutility)]
 [!code-vb[PrintTicketManagment#UIForMergeAndValidatePTUtility](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PrintTicketManagment/visualbasic/printticket.vb#uiformergeandvalidateptutility)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Printing.PrintCapabilities>
- <xref:System.Printing.PrintTicket>
- <xref:System.Printing.PrintServer.GetPrintQueues%2A>
- <xref:System.Printing.PrintServer>
- <xref:System.Printing.EnumeratedPrintQueueTypes>
- <xref:System.Printing.PrintQueue>
- <xref:System.Printing.PrintQueue.GetPrintCapabilities%2A>
- [Documents dans WPF](documents-in-wpf.md)
- [Vue d'ensemble de l'impression](printing-overview.md)
- [Schéma d’impression](https://go.microsoft.com/fwlink/?LinkId=186397)
