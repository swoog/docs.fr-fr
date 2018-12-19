---
title: '&lt;permission&gt; - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- permission
- <permission>
helpviewer_keywords:
- <permission> C# XML tag
- permission C# XML tag
ms.assetid: 769e93fe-8404-443f-bf99-577aa42b6a49
ms.openlocfilehash: bd5849317fbcb5728033fe271f250401a5993ca3
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53238609"
---
# <a name="ltpermissiongt-c-programming-guide"></a><span data-ttu-id="2cd1c-102">&lt;permission&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="2cd1c-102">&lt;permission&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="2cd1c-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2cd1c-103">Syntax</span></span>  
  
```xml  
<permission cref="member">description</permission>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2cd1c-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2cd1c-104">Parameters</span></span>  
 <span data-ttu-id="2cd1c-105">cref = " `member`"</span><span class="sxs-lookup"><span data-stu-id="2cd1c-105">cref = " `member`"</span></span>  
 <span data-ttu-id="2cd1c-106">Référence à un membre ou un champ qu’il est possible d’appeler à partir de l’environnement de compilation actuel.</span><span class="sxs-lookup"><span data-stu-id="2cd1c-106">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="2cd1c-107">Le compilateur vérifie que l’élément de code donné existe et traduit `member` en nom d’élément canonique dans le fichier XML de sortie.</span><span class="sxs-lookup"><span data-stu-id="2cd1c-107">The compiler checks that the given code element exists and translates `member` to the canonical element name in the output XML.</span></span> <span data-ttu-id="2cd1c-108">Le *membre* doit apparaître entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="2cd1c-108">*member* must appear within double quotation marks (" ").</span></span>  
  
 <span data-ttu-id="2cd1c-109">Pour plus d’informations sur la création d’une référence cref à un type générique, consultez [\<see>](../../../csharp/programming-guide/xmldoc/see.md).</span><span class="sxs-lookup"><span data-stu-id="2cd1c-109">For information on how to create a cref reference to a generic type, see [\<see>](../../../csharp/programming-guide/xmldoc/see.md).</span></span>  
  
 `description`  
 <span data-ttu-id="2cd1c-110">Description de l’accès au membre.</span><span class="sxs-lookup"><span data-stu-id="2cd1c-110">A description of the access to the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2cd1c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2cd1c-111">Remarks</span></span>  
 <span data-ttu-id="2cd1c-112">La balise \<permission> vous permet de documenter l’accès d’un membre.</span><span class="sxs-lookup"><span data-stu-id="2cd1c-112">The \<permission> tag lets you document the access of a member.</span></span> <span data-ttu-id="2cd1c-113">La classe <xref:System.Security.PermissionSet> vous permet de spécifier l’accès à un membre.</span><span class="sxs-lookup"><span data-stu-id="2cd1c-113">The <xref:System.Security.PermissionSet> class lets you specify access to a member.</span></span>  
  
 <span data-ttu-id="2cd1c-114">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="2cd1c-114">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2cd1c-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="2cd1c-115">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#8](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/permission_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="2cd1c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cd1c-116">See Also</span></span>

- [<span data-ttu-id="2cd1c-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="2cd1c-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="2cd1c-118">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="2cd1c-118">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
