---
title: '&lt;la section Notes&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <remarks> XML tag
- remarks XML tag
ms.assetid: c6241773-a7ed-41c9-9a8b-9722a0c606a9
ms.openlocfilehash: 6e4e280760b9238fdc403ac5fe586743334e4c69
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33598183"
---
# <a name="ltremarksgt-visual-basic"></a><span data-ttu-id="bc8e1-102">&lt;la section Notes&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bc8e1-102">&lt;remarks&gt; (Visual Basic)</span></span>
<span data-ttu-id="bc8e1-103">Spécifie une section de la section Notes pour le membre.</span><span class="sxs-lookup"><span data-stu-id="bc8e1-103">Specifies a remarks section for the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bc8e1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc8e1-104">Syntax</span></span>  
  
```xml  
<remarks>description</remarks>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bc8e1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc8e1-105">Parameters</span></span>  
 `description`  
 <span data-ttu-id="bc8e1-106">Description du membre.</span><span class="sxs-lookup"><span data-stu-id="bc8e1-106">A description of the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bc8e1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="bc8e1-107">Remarks</span></span>  
 <span data-ttu-id="bc8e1-108">Utilisez le `<remarks>` balise pour ajouter des informations sur un type, de compléter les informations spécifiées avec [ \<Résumé >](../../../visual-basic/language-reference/xmldoc/summary.md).</span><span class="sxs-lookup"><span data-stu-id="bc8e1-108">Use the `<remarks>` tag to add information about a type, supplementing the information specified with [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md).</span></span>  
  
 <span data-ttu-id="bc8e1-109">Ces informations s’affichent dans l’Explorateur d’objets.</span><span class="sxs-lookup"><span data-stu-id="bc8e1-109">This information appears in the Object Browser.</span></span> <span data-ttu-id="bc8e1-110">Pour plus d’informations sur l’Explorateur d’objets, consultez [affichage de la Structure du Code](/visualstudio/ide/viewing-the-structure-of-code).</span><span class="sxs-lookup"><span data-stu-id="bc8e1-110">For information about the Object Browser, see [Viewing the Structure of Code](/visualstudio/ide/viewing-the-structure-of-code).</span></span>  
  
 <span data-ttu-id="bc8e1-111">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="bc8e1-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bc8e1-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="bc8e1-112">Example</span></span>  
 <span data-ttu-id="bc8e1-113">Cet exemple utilise le `<remarks>` balise pour expliquer la `UpdateRecord` méthode.</span><span class="sxs-lookup"><span data-stu-id="bc8e1-113">This example uses the `<remarks>` tag to explain what the `UpdateRecord` method does.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/remarks_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="bc8e1-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc8e1-114">See Also</span></span>  
 [<span data-ttu-id="bc8e1-115">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="bc8e1-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)
