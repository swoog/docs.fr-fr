---
title: '&lt;c&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- c XML tag
- <c> XML tag
ms.assetid: 36ad5d1b-11f7-4012-8932-41962ac327d1
ms.openlocfilehash: 0e3ed08a62e9a52efa231c573a8061ff92d3cee0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54604155"
---
# <a name="ltcgt-visual-basic"></a><span data-ttu-id="63b25-102">&lt;c&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="63b25-102">&lt;c&gt; (Visual Basic)</span></span>
<span data-ttu-id="63b25-103">Indique que le texte d’une description est code.</span><span class="sxs-lookup"><span data-stu-id="63b25-103">Indicates that text within a description is code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63b25-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63b25-104">Syntax</span></span>  
  
```xml  
<c>text</c>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="63b25-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63b25-105">Parameters</span></span>  
  
|<span data-ttu-id="63b25-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="63b25-106">Parameter</span></span>|<span data-ttu-id="63b25-107">Description</span><span class="sxs-lookup"><span data-stu-id="63b25-107">Description</span></span>|  
|---|---|  
|`text`|<span data-ttu-id="63b25-108">Texte que vous souhaitez indiquer comme étant du code.</span><span class="sxs-lookup"><span data-stu-id="63b25-108">The text you would like to indicate as code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="63b25-109">Notes</span><span class="sxs-lookup"><span data-stu-id="63b25-109">Remarks</span></span>  
 <span data-ttu-id="63b25-110">Le `<c>` balise vous donne un moyen d’indiquer que le texte d’une description doit être marqué en tant que code.</span><span class="sxs-lookup"><span data-stu-id="63b25-110">The `<c>` tag gives you a way to indicate that text within a description should be marked as code.</span></span> <span data-ttu-id="63b25-111">Utilisez [\<code>](../../../visual-basic/language-reference/xmldoc/code.md) pour indiquer plusieurs lignes comme étant du code.</span><span class="sxs-lookup"><span data-stu-id="63b25-111">Use [\<code>](../../../visual-basic/language-reference/xmldoc/code.md) to indicate multiple lines as code.</span></span>  
  
 <span data-ttu-id="63b25-112">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="63b25-112">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="63b25-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="63b25-113">Example</span></span>  
 <span data-ttu-id="63b25-114">Cet exemple utilise le `<c>` balise dans la section Résumé pour indiquer que `Counter` est le code.</span><span class="sxs-lookup"><span data-stu-id="63b25-114">This example uses the `<c>` tag in the summary section to indicate that `Counter` is code.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/c_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="63b25-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63b25-115">See also</span></span>
- [<span data-ttu-id="63b25-116">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="63b25-116">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
