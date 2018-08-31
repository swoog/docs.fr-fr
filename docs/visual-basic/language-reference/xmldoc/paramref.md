---
title: '&lt;paramref&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- paramref XML tag
- <paramref> XML tag
ms.assetid: 8979d53b-beb1-41b7-b41e-6bbea1c17a03
ms.openlocfilehash: 153f5ddeeb7d09159049af4d466b0695f5cb6f23
ms.sourcegitcommit: a368166a51e5204c0224fbf5e46476e3ed122817
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2018
ms.locfileid: "43331357"
---
# <a name="ltparamrefgt-visual-basic"></a><span data-ttu-id="62058-102">&lt;paramref&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="62058-102">&lt;paramref&gt; (Visual Basic)</span></span>
<span data-ttu-id="62058-103">Met en forme un mot en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="62058-103">Formats a word as a parameter.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="62058-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62058-104">Syntax</span></span>  
  
```xml  
<paramref name="name"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="62058-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62058-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="62058-106">Nom du paramètre auquel faire référence.</span><span class="sxs-lookup"><span data-stu-id="62058-106">The name of the parameter to refer to.</span></span> <span data-ttu-id="62058-107">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="62058-107">Enclose the name in double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="62058-108">Notes</span><span class="sxs-lookup"><span data-stu-id="62058-108">Remarks</span></span>  
 <span data-ttu-id="62058-109">Le `<paramref>` balise vous donne un moyen d’indiquer qu’un mot est un paramètre.</span><span class="sxs-lookup"><span data-stu-id="62058-109">The `<paramref>` tag gives you a way to indicate that a word is a parameter.</span></span> <span data-ttu-id="62058-110">Le fichier XML peut être traité pour mettre en forme ce paramètre d’une manière distincte.</span><span class="sxs-lookup"><span data-stu-id="62058-110">The XML file can be processed to format this parameter in some distinct way.</span></span>  
  
 <span data-ttu-id="62058-111">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="62058-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="62058-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="62058-112">Example</span></span>  
 <span data-ttu-id="62058-113">Cet exemple utilise le `<paramref>` balise pour faire référence à la `id` paramètre.</span><span class="sxs-lookup"><span data-stu-id="62058-113">This example uses the `<paramref>` tag to refer to the `id` parameter.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/paramref_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="62058-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62058-114">See Also</span></span>  
 [<span data-ttu-id="62058-115">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="62058-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
