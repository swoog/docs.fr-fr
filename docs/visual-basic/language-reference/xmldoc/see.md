---
title: '&lt;consultez&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- see XML tag
- <see> XML tag
ms.assetid: 7e18f60b-ef4a-4678-a797-5eb918635ca9
ms.openlocfilehash: e790f8abd216e198ff5077beab6f857e39981d2b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33602078"
---
# <a name="ltseegt-visual-basic"></a><span data-ttu-id="3f15b-102">&lt;consultez&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="3f15b-102">&lt;see&gt; (Visual Basic)</span></span>
<span data-ttu-id="3f15b-103">Spécifie un lien vers un autre membre.</span><span class="sxs-lookup"><span data-stu-id="3f15b-103">Specifies a link to another member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f15b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f15b-104">Syntax</span></span>  
  
```xml  
<see cref="member"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3f15b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f15b-105">Parameters</span></span>  
 `member`  
 <span data-ttu-id="3f15b-106">Référence à un membre ou un champ qu’il est possible d’appeler à partir de l’environnement de compilation actuel.</span><span class="sxs-lookup"><span data-stu-id="3f15b-106">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="3f15b-107">Le compilateur vérifie que l’élément de code donné existe et qu’il passe `member` nom de l’élément dans la sortie XML.</span><span class="sxs-lookup"><span data-stu-id="3f15b-107">The compiler checks that the given code element exists and passes `member` to the element name in the output XML.</span></span> <span data-ttu-id="3f15b-108">`member` doit apparaître entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="3f15b-108">`member` must appear within double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3f15b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3f15b-109">Remarks</span></span>  
 <span data-ttu-id="3f15b-110">Utilisez le `<see>` balise pour spécifier un lien à partir du texte.</span><span class="sxs-lookup"><span data-stu-id="3f15b-110">Use the `<see>` tag to specify a link from within text.</span></span> <span data-ttu-id="3f15b-111">Utilisez [ \<seealso >](../../../visual-basic/language-reference/xmldoc/seealso.md) pour indiquer le texte que vous souhaitez apparaissent dans une section « Voir aussi ».</span><span class="sxs-lookup"><span data-stu-id="3f15b-111">Use [\<seealso>](../../../visual-basic/language-reference/xmldoc/seealso.md) to indicate text that you might want to appear in a "See Also" section.</span></span>  
  
 <span data-ttu-id="3f15b-112">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="3f15b-112">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3f15b-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="3f15b-113">Example</span></span>  
 <span data-ttu-id="3f15b-114">Cet exemple utilise le `<see>` de balise dans le `UpdateRecord` la section Notes de la section pour faire référence à la `DoesRecordExist` (méthode).</span><span class="sxs-lookup"><span data-stu-id="3f15b-114">This example uses the `<see>` tag in the `UpdateRecord` remarks section to refer to the `DoesRecordExist` method.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/see_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="3f15b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f15b-115">See Also</span></span>  
 [<span data-ttu-id="3f15b-116">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="3f15b-116">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)
