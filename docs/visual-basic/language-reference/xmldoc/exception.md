---
title: <exception> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <exception> XML tag
- exception XML tag
ms.assetid: c0517549-171e-4dae-ab88-a9c1700b6eee
ms.openlocfilehash: 4e2f441863d6a8677593a257cdb2cc841634d47c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58820241"
---
# <a name="exception-visual-basic"></a><span data-ttu-id="202d0-102">\<exception > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="202d0-102">\<exception> (Visual Basic)</span></span>
<span data-ttu-id="202d0-103">Spécifie quelles exceptions peuvent être levées.</span><span class="sxs-lookup"><span data-stu-id="202d0-103">Specifies which exceptions can be thrown.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="202d0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="202d0-104">Syntax</span></span>  
  
```xml  
<exception cref="member">description</exception>  
```  
  
## <a name="parameters"></a><span data-ttu-id="202d0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="202d0-105">Parameters</span></span>  
 `member`  
 <span data-ttu-id="202d0-106">Référence à une exception qui est disponible à partir de l’environnement de compilation actuel.</span><span class="sxs-lookup"><span data-stu-id="202d0-106">A reference to an exception that is available from the current compilation environment.</span></span> <span data-ttu-id="202d0-107">Le compilateur vérifie que l’exception donnée existe, et il traduit `member` en nom d’élément canonique dans le fichier XML de sortie.</span><span class="sxs-lookup"><span data-stu-id="202d0-107">The compiler checks that the given exception exists and translates `member` to the canonical element name in the output XML.</span></span> <span data-ttu-id="202d0-108">`member` doit apparaître entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="202d0-108">`member` must appear within double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="202d0-109">Description.</span><span class="sxs-lookup"><span data-stu-id="202d0-109">A description.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="202d0-110">Notes</span><span class="sxs-lookup"><span data-stu-id="202d0-110">Remarks</span></span>  
 <span data-ttu-id="202d0-111">Utilisez le `<exception>` balise pour spécifier quelles exceptions peuvent être levées.</span><span class="sxs-lookup"><span data-stu-id="202d0-111">Use the `<exception>` tag to specify which exceptions can be thrown.</span></span> <span data-ttu-id="202d0-112">Cette balise est appliquée à une définition de méthode.</span><span class="sxs-lookup"><span data-stu-id="202d0-112">This tag is applied to a method definition.</span></span>  
  
 <span data-ttu-id="202d0-113">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="202d0-113">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="202d0-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="202d0-114">Example</span></span>  
 <span data-ttu-id="202d0-115">Cet exemple utilise le `<exception>` balises pour décrire une exception qui le `IntDivide` fonction peut lever.</span><span class="sxs-lookup"><span data-stu-id="202d0-115">This example uses the `<exception>` tag to describe an exception that the `IntDivide` function can throw.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="202d0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="202d0-116">See also</span></span>

- [<span data-ttu-id="202d0-117">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="202d0-117">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
