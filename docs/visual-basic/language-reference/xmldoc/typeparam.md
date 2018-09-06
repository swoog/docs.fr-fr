---
title: '&lt;typeparam&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- typeparam XML tag
- <typeparam> XML tag
ms.assetid: 1bb5ba78-f060-478c-905c-77a2e43639af
ms.openlocfilehash: d362f181921a39d274eaee78e85976522ce4fc15
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43736190"
---
# <a name="lttypeparamgt-visual-basic"></a><span data-ttu-id="78124-102">&lt;typeparam&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="78124-102">&lt;typeparam&gt; (Visual Basic)</span></span>
<span data-ttu-id="78124-103">Définit un nom de paramètre de type et une description.</span><span class="sxs-lookup"><span data-stu-id="78124-103">Defines a type parameter name and description.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="78124-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78124-104">Syntax</span></span>  
  
```xml  
<typeparam name="name">description</typeparam>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="78124-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78124-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="78124-106">Nom du paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="78124-106">The name of the type parameter.</span></span> <span data-ttu-id="78124-107">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="78124-107">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="78124-108">Description du paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="78124-108">A description of the type parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="78124-109">Notes</span><span class="sxs-lookup"><span data-stu-id="78124-109">Remarks</span></span>  
 <span data-ttu-id="78124-110">Utilisez le `<typeparam>` balise dans le commentaire pour un type générique ou une déclaration de membre générique décrire l’un des paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="78124-110">Use the `<typeparam>` tag in the comment for a generic type or generic member declaration to describe one of the type parameters.</span></span>  
  
 <span data-ttu-id="78124-111">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="78124-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="78124-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="78124-112">Example</span></span>  
 <span data-ttu-id="78124-113">Cet exemple utilise le `<typeparam>` balises pour décrire le `id` paramètre.</span><span class="sxs-lookup"><span data-stu-id="78124-113">This example uses the `<typeparam>` tag to describe the `id` parameter.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#8](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/typeparam_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="78124-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78124-114">See Also</span></span>  
 [<span data-ttu-id="78124-115">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="78124-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
