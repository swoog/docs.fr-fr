---
title: <value> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <value> XML tag
- value XML tag
ms.assetid: 0b84b02e-9e6d-41b5-a926-0d5dc76dacb5
ms.openlocfilehash: 89a2daad1c47ea8e2a045b2e22a9569e54086e8a
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56970738"
---
# <a name="value-visual-basic"></a><span data-ttu-id="4416a-102">\<valeur > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4416a-102">\<value> (Visual Basic)</span></span>
<span data-ttu-id="4416a-103">Spécifie la description d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="4416a-103">Specifies the description of a property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4416a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4416a-104">Syntax</span></span>  
  
```xml  
<value>property-description</value>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4416a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4416a-105">Parameters</span></span>  
 `property-description`  
 <span data-ttu-id="4416a-106">Description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="4416a-106">A description for the property.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4416a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="4416a-107">Remarks</span></span>  
 <span data-ttu-id="4416a-108">Utilisez le `<value>` balise pour décrire une propriété.</span><span class="sxs-lookup"><span data-stu-id="4416a-108">Use the `<value>` tag to describe a property.</span></span> <span data-ttu-id="4416a-109">Notez que lorsque vous ajoutez une propriété à l’aide de l’Assistant code dans l’environnement de développement Visual Studio, il ajoute un [ \<Résumé >](../../../visual-basic/language-reference/xmldoc/summary.md) balise pour la nouvelle propriété.</span><span class="sxs-lookup"><span data-stu-id="4416a-109">Note that when you add a property using the code wizard in the Visual Studio development environment, it will add a [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md) tag for the new property.</span></span> <span data-ttu-id="4416a-110">Vous devez ensuite ajouter manuellement un `<value>` balise pour décrire la valeur qui représente la propriété.</span><span class="sxs-lookup"><span data-stu-id="4416a-110">You should then manually add a `<value>` tag to describe the value that the property represents.</span></span>  
  
 <span data-ttu-id="4416a-111">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="4416a-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4416a-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="4416a-112">Example</span></span>  
 <span data-ttu-id="4416a-113">Cet exemple utilise le `<value>` balise à décrire la valeur que le `Counter` contient de la propriété.</span><span class="sxs-lookup"><span data-stu-id="4416a-113">This example uses the `<value>` tag to describe what value the `Counter` property holds.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="4416a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4416a-114">See also</span></span>
- [<span data-ttu-id="4416a-115">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="4416a-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
