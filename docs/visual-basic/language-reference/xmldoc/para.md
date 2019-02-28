---
title: <para> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <para> XML tag
- para XML tag
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
ms.openlocfilehash: 96ef62d53fd1cc806c0dc72d2d0781b1c6297dc6
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56970868"
---
# <a name="para-visual-basic"></a><span data-ttu-id="71da0-102">\<para > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="71da0-102">\<para> (Visual Basic)</span></span>
<span data-ttu-id="71da0-103">Spécifie que le contenu est mis en forme comme un paragraphe.</span><span class="sxs-lookup"><span data-stu-id="71da0-103">Specifies that the content is formatted as a paragraph.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="71da0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71da0-104">Syntax</span></span>  
  
```xml  
<para>content</para>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="71da0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71da0-105">Parameters</span></span>  
 `content`  
 <span data-ttu-id="71da0-106">Texte du paragraphe.</span><span class="sxs-lookup"><span data-stu-id="71da0-106">The text of the paragraph.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="71da0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="71da0-107">Remarks</span></span>  
 <span data-ttu-id="71da0-108">Le `<para>` balise est destinée à l’intérieur d’une balise, tel que [ \<Résumé >](../../../visual-basic/language-reference/xmldoc/summary.md), [ \<remarks >](../../../visual-basic/language-reference/xmldoc/remarks.md), ou [ \<retourne >](../../../visual-basic/language-reference/xmldoc/returns.md), et vous permet d’ajouter une structure au texte.</span><span class="sxs-lookup"><span data-stu-id="71da0-108">The `<para>` tag is for use inside a tag, such as [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md), [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md), or [\<returns>](../../../visual-basic/language-reference/xmldoc/returns.md), and lets you add structure to the text.</span></span>  
  
 <span data-ttu-id="71da0-109">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="71da0-109">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="71da0-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="71da0-110">Example</span></span>  
 <span data-ttu-id="71da0-111">Cet exemple utilise le `<para>` balise pour fractionner la section Notes pour la `UpdateRecord` méthode en deux paragraphes.</span><span class="sxs-lookup"><span data-stu-id="71da0-111">This example uses the `<para>` tag to split the remarks section for the `UpdateRecord` method into two paragraphs.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="71da0-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71da0-112">See also</span></span>
- [<span data-ttu-id="71da0-113">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="71da0-113">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
