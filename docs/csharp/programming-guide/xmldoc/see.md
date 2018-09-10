---
title: '&lt;see&gt; (Guide de programmation C#)'
ms.date: 07/20/2015
f1_keywords:
- <see>
- see
helpviewer_keywords:
- cref [C#], <see> tag
- <see> C# XML tag
- cross-references [C#]
- see C# XML tag
ms.assetid: 0200de01-7e2f-45c4-9094-829d61236383
ms.openlocfilehash: c37ad869b3eb904377cd4470a85cd557f6560290
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44196359"
---
# <a name="ltseegt-c-programming-guide"></a><span data-ttu-id="f4b56-102">&lt;see&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="f4b56-102">&lt;see&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="f4b56-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4b56-103">Syntax</span></span>  
  
```xml  
<see cref="member"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f4b56-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4b56-104">Parameters</span></span>  
 <span data-ttu-id="f4b56-105">cref = " `member`"</span><span class="sxs-lookup"><span data-stu-id="f4b56-105">cref = " `member`"</span></span>  
 <span data-ttu-id="f4b56-106">Référence à un membre ou un champ qu’il est possible d’appeler à partir de l’environnement de compilation actuel.</span><span class="sxs-lookup"><span data-stu-id="f4b56-106">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="f4b56-107">Le compilateur vérifie que l’élément de code donné existe, et qu’il passe `member` au nom d’élément dans le code XML de sortie. Placez *member* entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="f4b56-107">The compiler checks that the given code element exists and passes `member` to the element name in the output XML.Place *member* within double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f4b56-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f4b56-108">Remarks</span></span>  
 <span data-ttu-id="f4b56-109">La balise \<see> vous permet de spécifier un lien à partir de l’intérieur du texte.</span><span class="sxs-lookup"><span data-stu-id="f4b56-109">The \<see> tag lets you specify a link from within text.</span></span> <span data-ttu-id="f4b56-110">Utilisez [\<seealso>](../../../csharp/programming-guide/xmldoc/seealso.md) pour indiquer que le texte doit être placé dans une section Voir aussi.</span><span class="sxs-lookup"><span data-stu-id="f4b56-110">Use [\<seealso>](../../../csharp/programming-guide/xmldoc/seealso.md) to indicate that text should be placed in a See Also section.</span></span> <span data-ttu-id="f4b56-111">Utilisez l’[attribut cref](../../../csharp/programming-guide/xmldoc/cref-attribute.md) pour créer des liens hypertexte internes aux pages de documentation pour les éléments de code.</span><span class="sxs-lookup"><span data-stu-id="f4b56-111">Use the [cref Attribute](../../../csharp/programming-guide/xmldoc/cref-attribute.md) to create internal hyperlinks to documentation pages for code elements.</span></span>  
  
 <span data-ttu-id="f4b56-112">Compilez avec [-doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="f4b56-112">Compile with [-doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
 <span data-ttu-id="f4b56-113">L’exemple suivant présente une balise \<see> dans une section de résumé (summary).</span><span class="sxs-lookup"><span data-stu-id="f4b56-113">The following example shows a \<see> tag within a summary section.</span></span>  
  
 [!code-csharp[csProgGuideDocComments#12](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/see_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="f4b56-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4b56-114">See Also</span></span>

- [<span data-ttu-id="f4b56-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f4b56-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="f4b56-116">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="f4b56-116">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
