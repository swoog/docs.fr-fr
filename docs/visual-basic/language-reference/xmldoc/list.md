---
title: <list> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- listheader XML tag
- <item> XML tag
- <list> XML tag
- <listheader> XML tag
- term XML tag
- list XML tag
- <description> XML tag
- description XML tag
- item XML tag
- <term> XML tag
ms.assetid: ec35fced-d58e-4520-a764-0691256e014b
ms.openlocfilehash: 7d7b85867f4c701322c5e6c31f2d89ab38fad05d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58818528"
---
# <a name="list-visual-basic"></a><span data-ttu-id="f02b7-102">\<liste > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f02b7-102">\<list> (Visual Basic)</span></span>
<span data-ttu-id="f02b7-103">Définit une liste ou une table.</span><span class="sxs-lookup"><span data-stu-id="f02b7-103">Defines a list or table.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f02b7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f02b7-104">Syntax</span></span>  
  
```xml  
<list type="type">  
   <listheader>  
      <term>term</term>  
      <description>description</description>  
   </listheader>  
   <item>  
      <term>term</term>  
      <description>description</description>  
   </item>  
</list>  
```  
  
## <a name="parameters"></a><span data-ttu-id="f02b7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f02b7-105">Parameters</span></span>  
 `type`  
 <span data-ttu-id="f02b7-106">Le type de la liste.</span><span class="sxs-lookup"><span data-stu-id="f02b7-106">The type of the list.</span></span> <span data-ttu-id="f02b7-107">Doit être un « bullet » pour une liste à puces, le « nombre » pour une liste numérotée, ou « table » pour une table de deux colonnes.</span><span class="sxs-lookup"><span data-stu-id="f02b7-107">Must be a "bullet" for a bulleted list, "number" for a numbered list, or "table" for a two-column table.</span></span>  
  
 `term`  
 <span data-ttu-id="f02b7-108">Utilisé uniquement lorsque `type` est « table ».</span><span class="sxs-lookup"><span data-stu-id="f02b7-108">Only used when `type` is "table."</span></span> <span data-ttu-id="f02b7-109">Terme à définir, qui est défini dans la balise de description.</span><span class="sxs-lookup"><span data-stu-id="f02b7-109">A term to define, which is defined in the description tag.</span></span>  
  
 `description`  
 <span data-ttu-id="f02b7-110">Lorsque `type` est « puce » ou « numéro », `description` est un élément dans la liste lorsque `type` est « table », `description` est la définition de `term`.</span><span class="sxs-lookup"><span data-stu-id="f02b7-110">When `type` is "bullet" or "number," `description` is an item in the list When `type` is "table," `description` is the definition of `term`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f02b7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f02b7-111">Remarks</span></span>  
 <span data-ttu-id="f02b7-112">Le `<listheader>` bloc définit le titre d’une table ou une définition de liste.</span><span class="sxs-lookup"><span data-stu-id="f02b7-112">The `<listheader>` block defines the heading of either a table or definition list.</span></span> <span data-ttu-id="f02b7-113">Lorsque vous définissez une table, il vous suffit de fournir une entrée pour `term` dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="f02b7-113">When defining a table, you only have to supply an entry for `term` in the heading.</span></span>  
  
 <span data-ttu-id="f02b7-114">Chaque élément dans la liste est spécifié avec un `<item>` bloc.</span><span class="sxs-lookup"><span data-stu-id="f02b7-114">Each item in the list is specified with an `<item>` block.</span></span> <span data-ttu-id="f02b7-115">Lorsque vous créez une liste de définitions, vous devez spécifier les `term` et `description`.</span><span class="sxs-lookup"><span data-stu-id="f02b7-115">When creating a definition list, you must specify both `term` and `description`.</span></span> <span data-ttu-id="f02b7-116">Toutefois, pour une table, une liste à puces ou une liste numérotée, il vous suffit de fournir une entrée pour `description`.</span><span class="sxs-lookup"><span data-stu-id="f02b7-116">However, for a table, bulleted list, or numbered list, you only have to supply an entry for `description`.</span></span>  
  
 <span data-ttu-id="f02b7-117">Une liste ou une table peut avoir autant `<item>` bloque en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="f02b7-117">A list or table can have as many `<item>` blocks as needed.</span></span>  
  
 <span data-ttu-id="f02b7-118">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="f02b7-118">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f02b7-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="f02b7-119">Example</span></span>  
 <span data-ttu-id="f02b7-120">Cet exemple utilise le `<list>` balise pour définir une liste à puces dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="f02b7-120">This example uses the `<list>` tag to define a bulleted list in the remarks section.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#5)]  
  
## <a name="see-also"></a><span data-ttu-id="f02b7-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f02b7-121">See also</span></span>

- [<span data-ttu-id="f02b7-122">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="f02b7-122">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
