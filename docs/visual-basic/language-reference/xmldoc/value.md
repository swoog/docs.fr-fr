---
title: '&lt;valeur&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <value> XML tag
- value XML tag
ms.assetid: 0b84b02e-9e6d-41b5-a926-0d5dc76dacb5
ms.openlocfilehash: f33a4ec32b45d8996bd39f0cc49097b5fd9252e4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33602456"
---
# <a name="ltvaluegt-visual-basic"></a><span data-ttu-id="c9405-102">&lt;valeur&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c9405-102">&lt;value&gt; (Visual Basic)</span></span>
<span data-ttu-id="c9405-103">Spécifie la description d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="c9405-103">Specifies the description of a property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9405-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9405-104">Syntax</span></span>  
  
```xml  
<value>property-description</value>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c9405-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9405-105">Parameters</span></span>  
 `property-description`  
 <span data-ttu-id="c9405-106">Description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="c9405-106">A description for the property.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c9405-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c9405-107">Remarks</span></span>  
 <span data-ttu-id="c9405-108">Utilisez le `<value>` balises pour décrire une propriété.</span><span class="sxs-lookup"><span data-stu-id="c9405-108">Use the `<value>` tag to describe a property.</span></span> <span data-ttu-id="c9405-109">Notez que lorsque vous ajoutez une propriété à l’aide de l’Assistant de code dans l’environnement de développement Visual Studio, il ajoute un [ \<Résumé >](../../../visual-basic/language-reference/xmldoc/summary.md) balise pour la nouvelle propriété.</span><span class="sxs-lookup"><span data-stu-id="c9405-109">Note that when you add a property using the code wizard in the Visual Studio development environment, it will add a [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md) tag for the new property.</span></span> <span data-ttu-id="c9405-110">Vous devez ensuite ajouter manuellement une `<value>` balises pour décrire la valeur représentée par la propriété.</span><span class="sxs-lookup"><span data-stu-id="c9405-110">You should then manually add a `<value>` tag to describe the value that the property represents.</span></span>  
  
 <span data-ttu-id="c9405-111">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="c9405-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c9405-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="c9405-112">Example</span></span>  
 <span data-ttu-id="c9405-113">Cet exemple utilise le `<value>` balises pour décrire la valeur que le `Counter` blocages de la propriété.</span><span class="sxs-lookup"><span data-stu-id="c9405-113">This example uses the `<value>` tag to describe what value the `Counter` property holds.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/value_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="c9405-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9405-114">See Also</span></span>  
 [<span data-ttu-id="c9405-115">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="c9405-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)
