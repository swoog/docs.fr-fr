---
title: <example> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- example XML tag
- <example> XML tag
ms.assetid: 90eeda1c-3fc4-427c-879c-5046d265a97c
ms.openlocfilehash: 510b00d2220b9c65b0e2b8fa3ead70925a9f54ba
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58821918"
---
# <a name="example-visual-basic"></a><span data-ttu-id="1d12b-102">\<exemple > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1d12b-102">\<example> (Visual Basic)</span></span>
<span data-ttu-id="1d12b-103">Spécifie un exemple pour le membre.</span><span class="sxs-lookup"><span data-stu-id="1d12b-103">Specifies an example for the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1d12b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d12b-104">Syntax</span></span>  
  
```xml  
<example>description</example>  
```  
  
## <a name="parameters"></a><span data-ttu-id="1d12b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d12b-105">Parameters</span></span>  
 `description`  
 <span data-ttu-id="1d12b-106">Description de l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="1d12b-106">A description of the code sample.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1d12b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1d12b-107">Remarks</span></span>  
 <span data-ttu-id="1d12b-108">Le `<example>` balise vous permet de spécifier un exemple montrant comment utiliser une méthode ou autres membres de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="1d12b-108">The `<example>` tag lets you specify an example of how to use a method or other library member.</span></span> <span data-ttu-id="1d12b-109">Cela implique généralement l’utilisation de la balise [\<code>](../../../visual-basic/language-reference/xmldoc/code.md).</span><span class="sxs-lookup"><span data-stu-id="1d12b-109">This commonly involves using the [\<code>](../../../visual-basic/language-reference/xmldoc/code.md) tag.</span></span>  
  
 <span data-ttu-id="1d12b-110">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="1d12b-110">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1d12b-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="1d12b-111">Example</span></span>  
 <span data-ttu-id="1d12b-112">Cet exemple utilise le `<example>` balise pour inclure un exemple d’utilisation de la `ID` champ.</span><span class="sxs-lookup"><span data-stu-id="1d12b-112">This example uses the `<example>` tag to include an example for using the `ID` field.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="1d12b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d12b-113">See also</span></span>

- [<span data-ttu-id="1d12b-114">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="1d12b-114">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
