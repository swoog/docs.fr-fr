---
title: "Comment : obtenir l'objet de liaison d'une propriété cible liée aux données"
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], getting binding objects from bound target properties
- properties [WPF], getting binding objects from
ms.assetid: 87974c5f-136b-4de7-b07d-9285b62ab123
ms.openlocfilehash: 0bc793d4c95f8919517a83e434cf795e971dcd32
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33556729"
---
# <a name="how-to-get-the-binding-object-from-a-bound-target-property"></a>Comment : obtenir l'objet de liaison d'une propriété cible liée aux données
Cet exemple montre comment obtenir l’objet de liaison à partir d’une propriété cible liée à des données.  
  
## <a name="example"></a>Exemple  
 Vous pouvez procédez comme suit pour obtenir le <xref:System.Windows.Data.Binding> objet :  
  
 [!code-csharp[BindValidation#GetBinding](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BindValidation/CSharp/Window1.xaml.cs#getbinding)]  
  
> [!NOTE]
>  Vous devez spécifier la propriété de dépendance pour la liaison de votre choix car il est possible que plusieurs propriétés de l’objet cible utilisent la liaison de données.  
  
 Vous pouvez également obtenir le <xref:System.Windows.Data.BindingExpression> , puis d’obtenir la valeur de la <xref:System.Windows.Data.BindingExpression.ParentBinding%2A> propriété.  
  
 Pour obtenir un exemple complet, consultez [Validation de liaison, exemple](http://go.microsoft.com/fwlink/?LinkID=159972).  
  
> [!NOTE]
>  Si votre liaison est un <xref:System.Windows.Data.MultiBinding>, utilisez <xref:System.Windows.Data.BindingOperations>.<xref:System.Windows.Data.BindingOperations.GetMultiBinding%2A>. S’il s’agit un <xref:System.Windows.Data.PriorityBinding>, utilisez <xref:System.Windows.Data.BindingOperations>.<xref:System.Windows.Data.BindingOperations.GetPriorityBinding%2A>. Si vous ne savez pas si la propriété cible est liée à l’aide un <xref:System.Windows.Data.Binding>, un <xref:System.Windows.Data.MultiBinding>, ou un <xref:System.Windows.Data.PriorityBinding>, vous pouvez utiliser <xref:System.Windows.Data.BindingOperations>.<xref:System.Windows.Data.BindingOperations.GetBindingBase%2A>.  
  
## <a name="see-also"></a>Voir aussi  
 [Créer une liaison dans du code](../../../../docs/framework/wpf/data/how-to-create-a-binding-in-code.md)  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
