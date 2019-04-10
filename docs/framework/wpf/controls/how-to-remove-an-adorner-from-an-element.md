---
title: 'Procédure : Supprimer un ornement d’un élément'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], removing
ms.assetid: 97cf4d9f-0596-429e-8526-32a30aa4ae99
ms.openlocfilehash: 256dd6fa0117f88aec2ef6b60c6dcd4c33b57855
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59212399"
---
# <a name="how-to-remove-an-adorner-from-an-element"></a>Procédure : Supprimer un ornement d’un élément
Cet exemple montre comment supprimer par programme un ornement spécifique à partir d’une certaine <xref:System.Windows.UIElement>.  
  
## <a name="example"></a>Exemple  
 Cet exemple de code en clair supprime le premier ornement dans le tableau des ornements retourné par <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>.  Cet exemple se produit pour récupérer les ornements sur un <xref:System.Windows.UIElement> nommé *myTextBox*.  Si l’élément spécifié dans l’appel à <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> a pas d’ornements, `null` est retournée.  Ce code vérifie un tableau null explicitement et est mieux adapté aux applications où un tableau null est censé être relativement courante.  
  
 [!code-csharp[AdornersMiscCode#_RemoveSpecificAdornerLong](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removespecificadornerlong)]
 [!code-vb[AdornersMiscCode#_RemoveSpecificAdornerLong](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removespecificadornerlong)]  
  
## <a name="example"></a>Exemple  
 Cet exemple de code condensé est fonctionnellement équivalent à l’exemple détaillé ci-dessus. Ce code ne vérifie pas explicitement un tableau null, il est donc possible qu’un <xref:System.NullReferenceException> exception peut être déclenchée.  Ce code est mieux adapté aux applications où un tableau null est censé être rares.  
  
 [!code-csharp[AdornersMiscCode#_RemoveSpecificAdornerShort](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removespecificadornershort)]
 [!code-vb[AdornersMiscCode#_RemoveSpecificAdornerShort](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removespecificadornershort)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble des ornements](adorners-overview.md)
