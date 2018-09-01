---
title: '&lt;Para&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <para> XML tag
- para XML tag
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
ms.openlocfilehash: fa11c713a5ed5793b50865753f8bcdeaabf56e83
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43386153"
---
# <a name="ltparagt-visual-basic"></a><span data-ttu-id="b49fb-102">&lt;Para&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b49fb-102">&lt;para&gt; (Visual Basic)</span></span>
<span data-ttu-id="b49fb-103">Spécifie que le contenu est mis en forme comme un paragraphe.</span><span class="sxs-lookup"><span data-stu-id="b49fb-103">Specifies that the content is formatted as a paragraph.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b49fb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b49fb-104">Syntax</span></span>  
  
```xml  
<para>content</para>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b49fb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b49fb-105">Parameters</span></span>  
 `content`  
 <span data-ttu-id="b49fb-106">Texte du paragraphe.</span><span class="sxs-lookup"><span data-stu-id="b49fb-106">The text of the paragraph.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b49fb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b49fb-107">Remarks</span></span>  
 <span data-ttu-id="b49fb-108">Le `<para>` balise est destinée à l’intérieur d’une balise, tel que [ \<Résumé >](../../../visual-basic/language-reference/xmldoc/summary.md), [ \<remarks >](../../../visual-basic/language-reference/xmldoc/remarks.md), ou [ \<retourne >](../../../visual-basic/language-reference/xmldoc/returns.md), et vous permet d’ajouter une structure au texte.</span><span class="sxs-lookup"><span data-stu-id="b49fb-108">The `<para>` tag is for use inside a tag, such as [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md), [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md), or [\<returns>](../../../visual-basic/language-reference/xmldoc/returns.md), and lets you add structure to the text.</span></span>  
  
 <span data-ttu-id="b49fb-109">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="b49fb-109">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b49fb-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="b49fb-110">Example</span></span>  
 <span data-ttu-id="b49fb-111">Cet exemple utilise le `<para>` balise pour fractionner la section Notes pour la `UpdateRecord` méthode en deux paragraphes.</span><span class="sxs-lookup"><span data-stu-id="b49fb-111">This example uses the `<para>` tag to split the remarks section for the `UpdateRecord` method into two paragraphs.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/para_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="b49fb-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b49fb-112">See Also</span></span>  
 [<span data-ttu-id="b49fb-113">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="b49fb-113">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
