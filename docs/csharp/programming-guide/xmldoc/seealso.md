---
title: '&lt;seealso&gt; (Guide de programmation C#)'
ms.date: 07/20/2015
f1_keywords:
- cref
- <seealso>
- seealso
helpviewer_keywords:
- cref [C#], see also
- seealso C# XML tag
- cref [C#]
- cross-references [C#], tags
- <seealso> C# XML tag
ms.assetid: 8e157f3f-f220-4fcf-9010-88905b080b18
ms.openlocfilehash: e3c9d68884e5cd4f5a4f81580f60cdde775458a3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33349133"
---
# <a name="ltseealsogt-c-programming-guide"></a><span data-ttu-id="b106f-102">&lt;seealso&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="b106f-102">&lt;seealso&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="b106f-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b106f-103">Syntax</span></span>  
  
```xml  
<seealso cref="member"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b106f-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b106f-104">Parameters</span></span>  
 <span data-ttu-id="b106f-105">cref = " `member`"</span><span class="sxs-lookup"><span data-stu-id="b106f-105">cref = " `member`"</span></span>  
 <span data-ttu-id="b106f-106">Référence à un membre ou un champ qu’il est possible d’appeler à partir de l’environnement de compilation actuel.</span><span class="sxs-lookup"><span data-stu-id="b106f-106">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="b106f-107">Le compilateur vérifie que l’élément de code donné existe, et qu’il passe `member` au nom d’élément dans le code XML de sortie. `member`</span><span class="sxs-lookup"><span data-stu-id="b106f-107">The compiler checks that the given code element exists and passes `member` to the element name in the output XML.`member`</span></span> <span data-ttu-id="b106f-108">doit être placé entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="b106f-108">must appear within double quotation marks (" ").</span></span>  
  
 <span data-ttu-id="b106f-109">Pour plus d’informations sur la création d’une référence cref à un type générique, consultez [\<see>](../../../csharp/programming-guide/xmldoc/see.md).</span><span class="sxs-lookup"><span data-stu-id="b106f-109">For information on how to create a cref reference to a generic type, see [\<see>](../../../csharp/programming-guide/xmldoc/see.md).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b106f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b106f-110">Remarks</span></span>  
 <span data-ttu-id="b106f-111">La balise \<seealso> vous permet de spécifier le texte que vous souhaitez voir apparaître dans une section Voir aussi.</span><span class="sxs-lookup"><span data-stu-id="b106f-111">The \<seealso> tag lets you specify the text that you might want to appear in a See Also section.</span></span> <span data-ttu-id="b106f-112">Utilisez [\<see>](../../../csharp/programming-guide/xmldoc/see.md) pour spécifier un lien à partir de l’intérieur du texte.</span><span class="sxs-lookup"><span data-stu-id="b106f-112">Use [\<see>](../../../csharp/programming-guide/xmldoc/see.md) to specify a link from within text.</span></span>  
  
 <span data-ttu-id="b106f-113">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="b106f-113">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b106f-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="b106f-114">Example</span></span>  
 <span data-ttu-id="b106f-115">Pour obtenir un exemple d’utilisation de \<seealso>, consultez [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md).</span><span class="sxs-lookup"><span data-stu-id="b106f-115">See [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md) for an example of using \<seealso>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b106f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b106f-116">See Also</span></span>  
 [<span data-ttu-id="b106f-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b106f-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="b106f-118">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="b106f-118">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
