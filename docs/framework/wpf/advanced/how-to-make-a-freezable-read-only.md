---
title: 'Procédure : Mettre un Freezable en lecture seule'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Freezable objects [WPF], making read-only
ms.assetid: 6c544b7d-d3c9-4736-aa90-4b8728234ccb
ms.openlocfilehash: e0cc5d73f9b9f15fc02bf20a70c84da1a7c535c9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54671666"
---
# <a name="how-to-make-a-freezable-read-only"></a>Procédure : Mettre un Freezable en lecture seule
Cet exemple montre comment rendre un <xref:System.Windows.Freezable> en lecture seule en appelant son <xref:System.Windows.Freezable.Freeze%2A> (méthode).  
  
 Vous ne pouvez pas figer un <xref:System.Windows.Freezable> objet si l’une des conditions suivantes est `true` sur l’objet :  
  
-   Il a animé ou propriétés liées aux données.  
  
-   Il possède des propriétés qui sont définies par une ressource dynamique. Pour plus d’informations sur les ressources dynamiques, consultez le [XAML ressources](../../../../docs/framework/wpf/advanced/xaml-resources.md).  
  
-   Il contient <xref:System.Windows.Freezable> sous-objets qui ne peut pas être figés.  
  
 Si ces conditions sont `false` pour votre <xref:System.Windows.Freezable> objet et que vous ne souhaitez pas modifier, envisagez de geler pour profiter des avantages de performances.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant se fige un <xref:System.Windows.Media.SolidColorBrush>, qui est un type de <xref:System.Windows.Freezable> objet.  
  
 [!code-csharp[freezablesample_procedural#FreezeExample1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#freezeexample1)]
 [!code-vb[freezablesample_procedural#FreezeExample1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#freezeexample1)]  
  
 Pour plus d’informations sur <xref:System.Windows.Freezable> , voir la [vue d’ensemble des objets Freezable](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.CanFreeze%2A>
- <xref:System.Windows.Freezable.Freeze%2A>
- [Vue d’ensemble des objets Freezable](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md)
- [Rubriques de guide pratique](../../../../docs/framework/wpf/advanced/base-elements-how-to-topics.md)
