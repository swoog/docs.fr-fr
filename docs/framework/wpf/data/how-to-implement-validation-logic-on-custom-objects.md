---
title: 'Comment : implémenter une logique de validation sur des objets personnalisés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- checking for validation errors [WPF]
- validation errors [WPF], checking for
- implementing validation logic on custom objects [WPF]
- custom objects [WPF], implementing validation logic on
ms.assetid: 751fda9b-44f9-4d63-b4f2-1df07ac41e0f
ms.openlocfilehash: dbeddb5eb6996d5758717ddd2d4d5af0b6f57f3c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33555962"
---
# <a name="how-to-implement-validation-logic-on-custom-objects"></a><span data-ttu-id="1d4b7-102">Comment : implémenter une logique de validation sur des objets personnalisés</span><span class="sxs-lookup"><span data-stu-id="1d4b7-102">How to: Implement Validation Logic on Custom Objects</span></span>
<span data-ttu-id="1d4b7-103">Cet exemple montre comment implémenter la logique de validation sur un objet personnalisé, puis lier à ce dernier.</span><span class="sxs-lookup"><span data-stu-id="1d4b7-103">This example shows how to implement validation logic on a custom object and then bind to it.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1d4b7-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="1d4b7-104">Example</span></span>  
 <span data-ttu-id="1d4b7-105">Vous pouvez fournir la logique de validation sur la couche métier si votre objet source implémente <xref:System.ComponentModel.IDataErrorInfo>, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="1d4b7-105">You can provide validation logic on the business layer if your source object implements <xref:System.ComponentModel.IDataErrorInfo>, as in the following example:</span></span>  
  
 [!code-csharp[BusinessLayerValidation#IDataErrorInfo](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BusinessLayerValidation/CSharp/Data.cs#idataerrorinfo)]
 [!code-vb[BusinessLayerValidation#IDataErrorInfo](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BusinessLayerValidation/VisualBasic/Data.vb#idataerrorinfo)]  
  
 <span data-ttu-id="1d4b7-106">Dans l’exemple suivant, la propriété text de la zone de texte lié à la `Age` propriété de la `Person` objet, qui soit devenue disponible pour une liaison via une déclaration de ressource qui reçoit le `x:Key``data`.</span><span class="sxs-lookup"><span data-stu-id="1d4b7-106">In the following example, the text property of the text box binds to the `Age` property of the `Person` object, which has been made available for binding through a resource declaration that is given the `x:Key``data`.</span></span> <span data-ttu-id="1d4b7-107">Le <xref:System.Windows.Controls.DataErrorValidationRule> vérifie les erreurs de validation déclenchées par le <xref:System.ComponentModel.IDataErrorInfo> implémentation.</span><span class="sxs-lookup"><span data-stu-id="1d4b7-107">The <xref:System.Windows.Controls.DataErrorValidationRule> checks for the validation errors raised by the <xref:System.ComponentModel.IDataErrorInfo> implementation.</span></span>  
  
 [!code-xaml[BusinessLayerValidation#BoundTextBox](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BusinessLayerValidation/CSharp/Window1.xaml#boundtextbox)]  
  
 <span data-ttu-id="1d4b7-108">Vous pouvez également, au lieu d’utiliser le <xref:System.Windows.Controls.DataErrorValidationRule>, vous pouvez définir le <xref:System.Windows.Data.Binding.ValidatesOnDataErrors%2A> propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="1d4b7-108">Alternatively, instead of using the <xref:System.Windows.Controls.DataErrorValidationRule>, you can set the <xref:System.Windows.Data.Binding.ValidatesOnDataErrors%2A> property to `true`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d4b7-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d4b7-109">See Also</span></span>  
 <xref:System.Windows.Controls.ExceptionValidationRule>  
 [<span data-ttu-id="1d4b7-110">Implémenter la validation de la liaison</span><span class="sxs-lookup"><span data-stu-id="1d4b7-110">Implement Binding Validation</span></span>](../../../../docs/framework/wpf/data/how-to-implement-binding-validation.md)  
 [<span data-ttu-id="1d4b7-111">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="1d4b7-111">How-to Topics</span></span>](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
