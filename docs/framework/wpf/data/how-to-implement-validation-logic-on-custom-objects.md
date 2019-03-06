---
title: 'Procédure : Implémenter une logique de validation sur des objets personnalisés'
ms.date: 08/02/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- checking for validation errors [WPF]
- validation errors [WPF], checking for
- implementing validation logic on custom objects [WPF]
- custom objects [WPF], implementing validation logic on
ms.assetid: 751fda9b-44f9-4d63-b4f2-1df07ac41e0f
ms.openlocfilehash: e183d286e4b9cd037c352126203b1ecdcca89ebb
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57365358"
---
# <a name="how-to-implement-validation-logic-on-custom-objects"></a>Procédure : Implémenter une logique de validation sur des objets personnalisés
Cet exemple montre comment implémenter une logique de validation sur un objet personnalisé, puis lier à ce dernier.  
  
## <a name="example"></a>Exemple  
 Vous pouvez fournir la logique de validation sur la couche métier si votre objet source implémente <xref:System.ComponentModel.IDataErrorInfo>, comme dans l’exemple suivant, qui définit un `Person` objet qui implémente <xref:System.ComponentModel.IDataErrorInfo>:  
  
 [!code-csharp[BusinessLayerValidation#IDataErrorInfo](~/samples/snippets/csharp/VS_Snippets_Wpf/BusinessLayerValidation/CSharp/Data.cs#idataerrorinfo)]
 [!code-vb[BusinessLayerValidation#IDataErrorInfo](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BusinessLayerValidation/VisualBasic/Data.vb#idataerrorinfo)]  
  
 Dans l’exemple suivant, la propriété de texte de la zone de texte est liée à la `Person.Age` propriété, qui a été rendue disponible pour une liaison via une déclaration de ressource qui reçoit le `x:Key` `data`. Le <xref:System.Windows.Controls.DataErrorValidationRule> vérifie les erreurs de validation déclenchés par le <xref:System.ComponentModel.IDataErrorInfo> implémentation.  
  
 [!code-xaml[BusinessLayerValidation#BoundTextBox](~/samples/snippets/csharp/VS_Snippets_Wpf/BusinessLayerValidation/CSharp/Window1.xaml?highlight=8,11-19,25-42)]  
  
 Vous pouvez également, au lieu d’utiliser le <xref:System.Windows.Controls.DataErrorValidationRule>, vous pouvez définir le <xref:System.Windows.Data.Binding.ValidatesOnDataErrors%2A> propriété `true`.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Controls.ExceptionValidationRule>
- [Implémenter la validation de la liaison](how-to-implement-binding-validation.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
