---
title: '&lt;exception&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <exception> XML tag
- exception XML tag
ms.assetid: c0517549-171e-4dae-ab88-a9c1700b6eee
ms.openlocfilehash: f29b8e01239f46b0d56319ba3da1a8fe179a17e8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33601151"
---
# <a name="ltexceptiongt-visual-basic"></a><span data-ttu-id="32363-102">&lt;exception&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="32363-102">&lt;exception&gt; (Visual Basic)</span></span>
<span data-ttu-id="32363-103">Spécifie les exceptions qui peuvent être levées.</span><span class="sxs-lookup"><span data-stu-id="32363-103">Specifies which exceptions can be thrown.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="32363-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32363-104">Syntax</span></span>  
  
```xml  
<exception cref="member">description</exception>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="32363-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32363-105">Parameters</span></span>  
 `member`  
 <span data-ttu-id="32363-106">Référence à une exception qui est disponible à partir de l’environnement de compilation actuel.</span><span class="sxs-lookup"><span data-stu-id="32363-106">A reference to an exception that is available from the current compilation environment.</span></span> <span data-ttu-id="32363-107">Le compilateur vérifie que l’exception donnée existe, et il traduit `member` en nom d’élément canonique dans le fichier XML de sortie.</span><span class="sxs-lookup"><span data-stu-id="32363-107">The compiler checks that the given exception exists and translates `member` to the canonical element name in the output XML.</span></span> <span data-ttu-id="32363-108">`member` doit apparaître entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="32363-108">`member` must appear within double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="32363-109">Une description.</span><span class="sxs-lookup"><span data-stu-id="32363-109">A description.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="32363-110">Notes</span><span class="sxs-lookup"><span data-stu-id="32363-110">Remarks</span></span>  
 <span data-ttu-id="32363-111">Utilisez le `<exception>` balise pour spécifier les exceptions qui peuvent être levées.</span><span class="sxs-lookup"><span data-stu-id="32363-111">Use the `<exception>` tag to specify which exceptions can be thrown.</span></span> <span data-ttu-id="32363-112">Cette balise est appliquée à une définition de méthode.</span><span class="sxs-lookup"><span data-stu-id="32363-112">This tag is applied to a method definition.</span></span>  
  
 <span data-ttu-id="32363-113">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="32363-113">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="32363-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="32363-114">Example</span></span>  
 <span data-ttu-id="32363-115">Cet exemple utilise le `<exception>` balises pour décrire une exception qui le `IntDivide` fonction peut lever une exception.</span><span class="sxs-lookup"><span data-stu-id="32363-115">This example uses the `<exception>` tag to describe an exception that the `IntDivide` function can throw.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#3](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/exception_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="32363-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32363-116">See Also</span></span>  
 [<span data-ttu-id="32363-117">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="32363-117">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)
