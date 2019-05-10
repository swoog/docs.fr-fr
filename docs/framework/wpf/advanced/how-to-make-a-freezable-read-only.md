---
title: 'Procédure : Mettre un Freezable en lecture seule'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Freezable objects [WPF], making read-only
ms.assetid: 6c544b7d-d3c9-4736-aa90-4b8728234ccb
ms.openlocfilehash: 5748b7929db18578bbe00e3217b1578ac5fbc0f4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64614587"
---
# <a name="how-to-make-a-freezable-read-only"></a>Procédure : Mettre un Freezable en lecture seule
Cet exemple montre comment rendre un <xref:System.Windows.Freezable> en lecture seule en appelant son <xref:System.Windows.Freezable.Freeze%2A> (méthode).  
  
 Vous ne pouvez pas figer un <xref:System.Windows.Freezable> objet si l’une des conditions suivantes est `true` sur l’objet :  
  
- Il a animé ou propriétés liées aux données.  
  
- Il possède des propriétés qui sont définies par une ressource dynamique. Pour plus d’informations sur les ressources dynamiques, consultez le [XAML ressources](xaml-resources.md).  
  
- Il contient <xref:System.Windows.Freezable> sous-objets qui ne peut pas être figés.  
  
 Si ces conditions sont `false` pour votre <xref:System.Windows.Freezable> objet et que vous ne souhaitez pas modifier, envisagez de geler pour profiter des avantages de performances.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant se fige un <xref:System.Windows.Media.SolidColorBrush>, qui est un type de <xref:System.Windows.Freezable> objet.  
  
 [!code-csharp[freezablesample_procedural#FreezeExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#freezeexample1)]
 [!code-vb[freezablesample_procedural#FreezeExample1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#freezeexample1)]  
  
 Pour plus d’informations sur <xref:System.Windows.Freezable> , voir la [vue d’ensemble des objets Freezable](freezable-objects-overview.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.CanFreeze%2A>
- <xref:System.Windows.Freezable.Freeze%2A>
- [Vue d’ensemble des objets Freezable](freezable-objects-overview.md)
- [Rubriques de guide pratique](base-elements-how-to-topics.md)
