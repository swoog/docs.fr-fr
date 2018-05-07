---
title: 'Comment : mettre un Freezable en lecture seule'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Freezable objects [WPF], making read-only
ms.assetid: 6c544b7d-d3c9-4736-aa90-4b8728234ccb
ms.openlocfilehash: be3abd74a71fc711cd9f4bf6796b7d55017355ef
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-make-a-freezable-read-only"></a>Comment : mettre un Freezable en lecture seule
Cet exemple montre comment rendre un <xref:System.Windows.Freezable> en lecture seule en appelant sa <xref:System.Windows.Freezable.Freeze%2A> (méthode).  
  
 Vous ne pouvez pas figer un <xref:System.Windows.Freezable> si l’une des conditions suivantes est de l’objet `true` sur l’objet :  
  
-   Il a animé ou propriétés lié aux données.  
  
-   Il possède des propriétés qui sont définies par une ressource dynamique. Pour plus d’informations sur les ressources dynamiques, consultez le [ressources XAML](../../../../docs/framework/wpf/advanced/xaml-resources.md).  
  
-   Il contient <xref:System.Windows.Freezable> sous-objets qui ne peut pas être figés.  
  
 Si ces conditions sont `false` pour votre <xref:System.Windows.Freezable> objet et que vous ne souhaitez pas modifier, envisagez de geler pour gagner des avantages de performances.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant gèle un <xref:System.Windows.Media.SolidColorBrush>, qui est un type de <xref:System.Windows.Freezable> objet.  
  
 [!code-csharp[freezablesample_procedural#FreezeExample1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#freezeexample1)]
 [!code-vb[freezablesample_procedural#FreezeExample1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#freezeexample1)]  
  
 Pour plus d’informations sur <xref:System.Windows.Freezable> , consultez la [vue d’ensemble des objets Freezable](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Freezable>  
 <xref:System.Windows.Freezable.CanFreeze%2A>  
 <xref:System.Windows.Freezable.Freeze%2A>  
 [Vue d’ensemble des objets Freezable](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md)  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/advanced/base-elements-how-to-topics.md)
