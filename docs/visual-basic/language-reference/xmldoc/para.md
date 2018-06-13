---
title: '&lt;Para&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <para> XML tag
- para XML tag
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
ms.openlocfilehash: cb80f4b39bee128790b311732adf1202dbbc6993
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33601723"
---
# <a name="ltparagt-visual-basic"></a><span data-ttu-id="b6b0f-102">&lt;Para&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b6b0f-102">&lt;para&gt; (Visual Basic)</span></span>
<span data-ttu-id="b6b0f-103">Spécifie que le contenu est mis en forme comme un paragraphe.</span><span class="sxs-lookup"><span data-stu-id="b6b0f-103">Specifies that the content is formatted as a paragraph.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6b0f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6b0f-104">Syntax</span></span>  
  
```xml  
<para>content</para>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b6b0f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6b0f-105">Parameters</span></span>  
 `content`  
 <span data-ttu-id="b6b0f-106">Texte du paragraphe.</span><span class="sxs-lookup"><span data-stu-id="b6b0f-106">The text of the paragraph.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b6b0f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b6b0f-107">Remarks</span></span>  
 <span data-ttu-id="b6b0f-108">Le `<para>` balise est destinée à l’intérieur d’une balise, tel que [ \<Résumé >](../../../visual-basic/language-reference/xmldoc/summary.md), [ \<Notes >](../../../visual-basic/language-reference/xmldoc/remarks.md), ou [ \<retourne >](../../../visual-basic/language-reference/xmldoc/returns.md), et vous permet de structurer le texte.</span><span class="sxs-lookup"><span data-stu-id="b6b0f-108">The `<para>` tag is for use inside a tag, such as [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md), [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md), or [\<returns>](../../../visual-basic/language-reference/xmldoc/returns.md), and lets you add structure to the text.</span></span>  
  
 <span data-ttu-id="b6b0f-109">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="b6b0f-109">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b6b0f-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6b0f-110">Example</span></span>  
 <span data-ttu-id="b6b0f-111">Cet exemple utilise le `<para>` balise pour fractionner la section Notes pour le `UpdateRecord` méthode en deux paragraphes.</span><span class="sxs-lookup"><span data-stu-id="b6b0f-111">This example uses the `<para>` tag to split the remarks section for the `UpdateRecord` method into two paragraphs.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/para_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="b6b0f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6b0f-112">See Also</span></span>  
 [<span data-ttu-id="b6b0f-113">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="b6b0f-113">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)
