---
title: '&lt;autorisation&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <permission> XML tag
- permission XML tag
ms.assetid: 0edf0500-5cd7-49c0-9255-64c48f972b77
ms.openlocfilehash: bcec5d968f5d0c5400c28e772df151b164888a47
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48793199"
---
# <a name="ltpermissiongt-visual-basic"></a><span data-ttu-id="c817c-102">&lt;autorisation&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c817c-102">&lt;permission&gt; (Visual Basic)</span></span>
<span data-ttu-id="c817c-103">Spécifie une autorisation requise pour le membre.</span><span class="sxs-lookup"><span data-stu-id="c817c-103">Specifies a required permission for the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c817c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c817c-104">Syntax</span></span>  
  
```xml  
<permission cref="member">description</permission>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c817c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c817c-105">Parameters</span></span>  
 `member`  
 <span data-ttu-id="c817c-106">Référence à un membre ou un champ qu’il est possible d’appeler à partir de l’environnement de compilation actuel.</span><span class="sxs-lookup"><span data-stu-id="c817c-106">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="c817c-107">Le compilateur vérifie que l’élément de code donné existe et traduit `member` en nom d’élément canonique dans le fichier XML de sortie.</span><span class="sxs-lookup"><span data-stu-id="c817c-107">The compiler checks that the given code element exists and translates `member` to the canonical element name in the output XML.</span></span> <span data-ttu-id="c817c-108">Placez `member` entre guillemets ( » «).</span><span class="sxs-lookup"><span data-stu-id="c817c-108">Enclose `member` in quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="c817c-109">Description de l’accès au membre.</span><span class="sxs-lookup"><span data-stu-id="c817c-109">A description of the access to the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c817c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c817c-110">Remarks</span></span>  
 <span data-ttu-id="c817c-111">Utilisez le `<permission>` balise à documenter l’accès d’un membre.</span><span class="sxs-lookup"><span data-stu-id="c817c-111">Use the `<permission>` tag to document the access of a member.</span></span> <span data-ttu-id="c817c-112">Utilisez la <xref:System.Security.PermissionSet> classe pour spécifier l’accès à un membre.</span><span class="sxs-lookup"><span data-stu-id="c817c-112">Use the <xref:System.Security.PermissionSet> class to specify access to a member.</span></span>  
  
 <span data-ttu-id="c817c-113">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="c817c-113">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c817c-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="c817c-114">Example</span></span>  
 <span data-ttu-id="c817c-115">Cet exemple utilise le `<permission>` balises pour décrire qui le <xref:System.Security.Permissions.FileIOPermission> est requis par le `ReadFile` (méthode).</span><span class="sxs-lookup"><span data-stu-id="c817c-115">This example uses the `<permission>` tag to describe that the <xref:System.Security.Permissions.FileIOPermission> is required by the `ReadFile` method.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#7](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/permission_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="c817c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c817c-116">See Also</span></span>  
 [<span data-ttu-id="c817c-117">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="c817c-117">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
