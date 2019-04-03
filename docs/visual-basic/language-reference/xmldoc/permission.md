---
title: <permission> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <permission> XML tag
- permission XML tag
ms.assetid: 0edf0500-5cd7-49c0-9255-64c48f972b77
ms.openlocfilehash: 7333d4a4d051c157f6732224da0fffe4d7cd35ee
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58827664"
---
# <a name="permission-visual-basic"></a><span data-ttu-id="b966b-102">\<autorisation > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b966b-102">\<permission> (Visual Basic)</span></span>
<span data-ttu-id="b966b-103">Spécifie une autorisation requise pour le membre.</span><span class="sxs-lookup"><span data-stu-id="b966b-103">Specifies a required permission for the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b966b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b966b-104">Syntax</span></span>  
  
```xml  
<permission cref="member">description</permission>  
```  
  
## <a name="parameters"></a><span data-ttu-id="b966b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b966b-105">Parameters</span></span>  
 `member`  
 <span data-ttu-id="b966b-106">Référence à un membre ou un champ qu’il est possible d’appeler à partir de l’environnement de compilation actuel.</span><span class="sxs-lookup"><span data-stu-id="b966b-106">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="b966b-107">Le compilateur vérifie que l’élément de code donné existe et traduit `member` en nom d’élément canonique dans le fichier XML de sortie.</span><span class="sxs-lookup"><span data-stu-id="b966b-107">The compiler checks that the given code element exists and translates `member` to the canonical element name in the output XML.</span></span> <span data-ttu-id="b966b-108">Placez `member` entre guillemets ( » «).</span><span class="sxs-lookup"><span data-stu-id="b966b-108">Enclose `member` in quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="b966b-109">Description de l’accès au membre.</span><span class="sxs-lookup"><span data-stu-id="b966b-109">A description of the access to the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b966b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b966b-110">Remarks</span></span>  
 <span data-ttu-id="b966b-111">Utilisez le `<permission>` balise à documenter l’accès d’un membre.</span><span class="sxs-lookup"><span data-stu-id="b966b-111">Use the `<permission>` tag to document the access of a member.</span></span> <span data-ttu-id="b966b-112">Utilisez la <xref:System.Security.PermissionSet> classe pour spécifier l’accès à un membre.</span><span class="sxs-lookup"><span data-stu-id="b966b-112">Use the <xref:System.Security.PermissionSet> class to specify access to a member.</span></span>  
  
 <span data-ttu-id="b966b-113">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="b966b-113">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b966b-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="b966b-114">Example</span></span>  
 <span data-ttu-id="b966b-115">Cet exemple utilise le `<permission>` balises pour décrire qui le <xref:System.Security.Permissions.FileIOPermission> est requis par le `ReadFile` (méthode).</span><span class="sxs-lookup"><span data-stu-id="b966b-115">This example uses the `<permission>` tag to describe that the <xref:System.Security.Permissions.FileIOPermission> is required by the `ReadFile` method.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#7)]  
  
## <a name="see-also"></a><span data-ttu-id="b966b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b966b-116">See also</span></span>

- [<span data-ttu-id="b966b-117">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="b966b-117">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
