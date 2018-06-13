---
title: '&lt;paramref&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- paramref XML tag
- <paramref> XML tag
ms.assetid: 8979d53b-beb1-41b7-b41e-6bbea1c17a03
ms.openlocfilehash: 763e311dfb46ceeed358c3b3bebd6212d3e2489c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33598660"
---
# <a name="ltparamrefgt-visual-basic"></a><span data-ttu-id="d41e5-102">&lt;paramref&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d41e5-102">&lt;paramref&gt; (Visual Basic)</span></span>
<span data-ttu-id="d41e5-103">Met en forme un mot en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="d41e5-103">Formats a word as a parameter.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d41e5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d41e5-104">Syntax</span></span>  
  
```xml  
<paramref name="name"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d41e5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d41e5-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="d41e5-106">Nom du paramètre auquel faire référence.</span><span class="sxs-lookup"><span data-stu-id="d41e5-106">The name of the parameter to refer to.</span></span> <span data-ttu-id="d41e5-107">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="d41e5-107">Enclose the name in double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d41e5-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d41e5-108">Remarks</span></span>  
 <span data-ttu-id="d41e5-109">Le `<paramref>` balise vous donne un moyen d’indiquer qu’un mot est un paramètre.</span><span class="sxs-lookup"><span data-stu-id="d41e5-109">The `<paramref>` tag gives you a way to indicate that a word is a parameter.</span></span> <span data-ttu-id="d41e5-110">Le fichier XML peut être traité pour mettre en forme ce paramètre de façon distincte.</span><span class="sxs-lookup"><span data-stu-id="d41e5-110">The XML file can be processed to format this parameter in some distinct way.</span></span>  
  
 <span data-ttu-id="d41e5-111">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="d41e5-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d41e5-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="d41e5-112">Example</span></span>  
 <span data-ttu-id="d41e5-113">Cet exemple utilise le `<paramref>` balise pour faire référence à la `id` paramètre.</span><span class="sxs-lookup"><span data-stu-id="d41e5-113">This example uses the `<paramref>` tag to refer to the `id` parameter.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/paramref_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="d41e5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d41e5-114">See Also</span></span>  
 [<span data-ttu-id="d41e5-115">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="d41e5-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)
