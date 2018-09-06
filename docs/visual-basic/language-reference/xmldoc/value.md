---
title: '&lt;valeur&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <value> XML tag
- value XML tag
ms.assetid: 0b84b02e-9e6d-41b5-a926-0d5dc76dacb5
ms.openlocfilehash: ef14836c438cf6a1de300270d9882c1e53e716ee
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43855931"
---
# <a name="ltvaluegt-visual-basic"></a><span data-ttu-id="36a65-102">&lt;valeur&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="36a65-102">&lt;value&gt; (Visual Basic)</span></span>
<span data-ttu-id="36a65-103">Spécifie la description d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="36a65-103">Specifies the description of a property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="36a65-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36a65-104">Syntax</span></span>  
  
```xml  
<value>property-description</value>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="36a65-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36a65-105">Parameters</span></span>  
 `property-description`  
 <span data-ttu-id="36a65-106">Description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="36a65-106">A description for the property.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="36a65-107">Notes</span><span class="sxs-lookup"><span data-stu-id="36a65-107">Remarks</span></span>  
 <span data-ttu-id="36a65-108">Utilisez le `<value>` balise pour décrire une propriété.</span><span class="sxs-lookup"><span data-stu-id="36a65-108">Use the `<value>` tag to describe a property.</span></span> <span data-ttu-id="36a65-109">Notez que lorsque vous ajoutez une propriété à l’aide de l’Assistant code dans l’environnement de développement Visual Studio, il ajoute un [ \<Résumé >](../../../visual-basic/language-reference/xmldoc/summary.md) balise pour la nouvelle propriété.</span><span class="sxs-lookup"><span data-stu-id="36a65-109">Note that when you add a property using the code wizard in the Visual Studio development environment, it will add a [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md) tag for the new property.</span></span> <span data-ttu-id="36a65-110">Vous devez ensuite ajouter manuellement un `<value>` balise pour décrire la valeur qui représente la propriété.</span><span class="sxs-lookup"><span data-stu-id="36a65-110">You should then manually add a `<value>` tag to describe the value that the property represents.</span></span>  
  
 <span data-ttu-id="36a65-111">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="36a65-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="36a65-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="36a65-112">Example</span></span>  
 <span data-ttu-id="36a65-113">Cet exemple utilise le `<value>` balise à décrire la valeur que le `Counter` contient de la propriété.</span><span class="sxs-lookup"><span data-stu-id="36a65-113">This example uses the `<value>` tag to describe what value the `Counter` property holds.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/value_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="36a65-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36a65-114">See Also</span></span>  
 [<span data-ttu-id="36a65-115">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="36a65-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
