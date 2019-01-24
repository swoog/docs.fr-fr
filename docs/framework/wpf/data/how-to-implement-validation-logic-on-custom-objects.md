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
ms.openlocfilehash: e2b77ef65c92ae596c5620c9122dcf3db0bf9462
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54525987"
---
# <a name="how-to-implement-validation-logic-on-custom-objects"></a><span data-ttu-id="48773-102">Procédure : Implémenter une logique de validation sur des objets personnalisés</span><span class="sxs-lookup"><span data-stu-id="48773-102">How to: Implement Validation Logic on Custom Objects</span></span>
<span data-ttu-id="48773-103">Cet exemple montre comment implémenter une logique de validation sur un objet personnalisé, puis lier à ce dernier.</span><span class="sxs-lookup"><span data-stu-id="48773-103">This example shows how to implement validation logic on a custom object and then bind to it.</span></span>  
  
## <a name="example"></a><span data-ttu-id="48773-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="48773-104">Example</span></span>  
 <span data-ttu-id="48773-105">Vous pouvez fournir la logique de validation sur la couche métier si votre objet source implémente <xref:System.ComponentModel.IDataErrorInfo>, comme dans l’exemple suivant, qui définit un `Person` objet qui implémente <xref:System.ComponentModel.IDataErrorInfo>:</span><span class="sxs-lookup"><span data-stu-id="48773-105">You can provide validation logic on the business layer if your source object implements <xref:System.ComponentModel.IDataErrorInfo>, as in the following example, which defines a `Person` object that implements <xref:System.ComponentModel.IDataErrorInfo>:</span></span>  
  
 [!code-csharp[BusinessLayerValidation#IDataErrorInfo](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BusinessLayerValidation/CSharp/Data.cs#idataerrorinfo)]
 [!code-vb[BusinessLayerValidation#IDataErrorInfo](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BusinessLayerValidation/VisualBasic/Data.vb#idataerrorinfo)]  
  
 <span data-ttu-id="48773-106">Dans l’exemple suivant, la propriété de texte de la zone de texte est liée à la `Person.Age` propriété, qui a été rendue disponible pour une liaison via une déclaration de ressource qui reçoit le `x:Key` `data`.</span><span class="sxs-lookup"><span data-stu-id="48773-106">In the following example, the text property of the text box binds to the `Person.Age` property, which has been made available for binding through a resource declaration that is given the `x:Key` `data`.</span></span> <span data-ttu-id="48773-107">Le <xref:System.Windows.Controls.DataErrorValidationRule> vérifie les erreurs de validation déclenchés par le <xref:System.ComponentModel.IDataErrorInfo> implémentation.</span><span class="sxs-lookup"><span data-stu-id="48773-107">The <xref:System.Windows.Controls.DataErrorValidationRule> checks for the validation errors raised by the <xref:System.ComponentModel.IDataErrorInfo> implementation.</span></span>  
  
 [!code-xaml[BusinessLayerValidation#BoundTextBox](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BusinessLayerValidation/CSharp/Window1.xaml?highlight=8,11-19,25-42)]  
  
 <span data-ttu-id="48773-108">Vous pouvez également, au lieu d’utiliser le <xref:System.Windows.Controls.DataErrorValidationRule>, vous pouvez définir le <xref:System.Windows.Data.Binding.ValidatesOnDataErrors%2A> propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="48773-108">Alternatively, instead of using the <xref:System.Windows.Controls.DataErrorValidationRule>, you can set the <xref:System.Windows.Data.Binding.ValidatesOnDataErrors%2A> property to `true`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48773-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48773-109">See also</span></span>
- <xref:System.Windows.Controls.ExceptionValidationRule>
- [<span data-ttu-id="48773-110">Implémenter la validation de la liaison</span><span class="sxs-lookup"><span data-stu-id="48773-110">Implement Binding Validation</span></span>](../../../../docs/framework/wpf/data/how-to-implement-binding-validation.md)
- [<span data-ttu-id="48773-111">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="48773-111">How-to Topics</span></span>](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
