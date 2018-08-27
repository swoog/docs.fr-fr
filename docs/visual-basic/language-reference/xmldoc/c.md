---
title: '&lt;c&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- c XML tag
- <c> XML tag
ms.assetid: 36ad5d1b-11f7-4012-8932-41962ac327d1
ms.openlocfilehash: 06c6899895f278fdf652725a05ecc7229805f4d4
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42935356"
---
# <a name="ltcgt-visual-basic"></a><span data-ttu-id="160d6-102">&lt;c&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="160d6-102">&lt;c&gt; (Visual Basic)</span></span>
<span data-ttu-id="160d6-103">Indique que le texte d’une description est code.</span><span class="sxs-lookup"><span data-stu-id="160d6-103">Indicates that text within a description is code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="160d6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="160d6-104">Syntax</span></span>  
  
```xml  
<c>text</c>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="160d6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="160d6-105">Parameters</span></span>  
  
|<span data-ttu-id="160d6-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="160d6-106">Parameter</span></span>|<span data-ttu-id="160d6-107">Description</span><span class="sxs-lookup"><span data-stu-id="160d6-107">Description</span></span>|  
|---|---|  
|`text`|<span data-ttu-id="160d6-108">Texte que vous souhaitez indiquer comme étant du code.</span><span class="sxs-lookup"><span data-stu-id="160d6-108">The text you would like to indicate as code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="160d6-109">Notes</span><span class="sxs-lookup"><span data-stu-id="160d6-109">Remarks</span></span>  
 <span data-ttu-id="160d6-110">Le `<c>` balise vous donne un moyen d’indiquer que le texte d’une description doit être marqué en tant que code.</span><span class="sxs-lookup"><span data-stu-id="160d6-110">The `<c>` tag gives you a way to indicate that text within a description should be marked as code.</span></span> <span data-ttu-id="160d6-111">Utilisez [\<code>](../../../visual-basic/language-reference/xmldoc/code.md) pour indiquer plusieurs lignes comme étant du code.</span><span class="sxs-lookup"><span data-stu-id="160d6-111">Use [\<code>](../../../visual-basic/language-reference/xmldoc/code.md) to indicate multiple lines as code.</span></span>  
  
 <span data-ttu-id="160d6-112">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="160d6-112">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="160d6-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="160d6-113">Example</span></span>  
 <span data-ttu-id="160d6-114">Cet exemple utilise le `<c>` balise dans la section Résumé pour indiquer que `Counter` est le code.</span><span class="sxs-lookup"><span data-stu-id="160d6-114">This example uses the `<c>` tag in the summary section to indicate that `Counter` is code.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/c_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="160d6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="160d6-115">See Also</span></span>  
 [<span data-ttu-id="160d6-116">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="160d6-116">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
