---
title: <para> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <para> XML tag
- para XML tag
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
ms.openlocfilehash: de0387298f6ff505b286db35047065ef88541a62
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55280447"
---
# <a name="para-visual-basic"></a><span data-ttu-id="46900-102">\<para > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="46900-102">\<para> (Visual Basic)</span></span>
<span data-ttu-id="46900-103">Spécifie que le contenu est mis en forme comme un paragraphe.</span><span class="sxs-lookup"><span data-stu-id="46900-103">Specifies that the content is formatted as a paragraph.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46900-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46900-104">Syntax</span></span>  
  
```xml  
<para>content</para>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="46900-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46900-105">Parameters</span></span>  
 `content`  
 <span data-ttu-id="46900-106">Texte du paragraphe.</span><span class="sxs-lookup"><span data-stu-id="46900-106">The text of the paragraph.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="46900-107">Notes</span><span class="sxs-lookup"><span data-stu-id="46900-107">Remarks</span></span>  
 <span data-ttu-id="46900-108">Le `<para>` balise est destinée à l’intérieur d’une balise, tel que [ \<Résumé >](../../../visual-basic/language-reference/xmldoc/summary.md), [ \<remarks >](../../../visual-basic/language-reference/xmldoc/remarks.md), ou [ \<retourne >](../../../visual-basic/language-reference/xmldoc/returns.md), et vous permet d’ajouter une structure au texte.</span><span class="sxs-lookup"><span data-stu-id="46900-108">The `<para>` tag is for use inside a tag, such as [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md), [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md), or [\<returns>](../../../visual-basic/language-reference/xmldoc/returns.md), and lets you add structure to the text.</span></span>  
  
 <span data-ttu-id="46900-109">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="46900-109">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="46900-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="46900-110">Example</span></span>  
 <span data-ttu-id="46900-111">Cet exemple utilise le `<para>` balise pour fractionner la section Notes pour la `UpdateRecord` méthode en deux paragraphes.</span><span class="sxs-lookup"><span data-stu-id="46900-111">This example uses the `<para>` tag to split the remarks section for the `UpdateRecord` method into two paragraphs.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/para_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="46900-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46900-112">See also</span></span>
- [<span data-ttu-id="46900-113">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="46900-113">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
