---
title: <typeparam> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- typeparam XML tag
- <typeparam> XML tag
ms.assetid: 1bb5ba78-f060-478c-905c-77a2e43639af
ms.openlocfilehash: 014623be84f9d7eb8a25ac4aadcce450f158c154
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58827235"
---
# <a name="typeparam-visual-basic"></a><span data-ttu-id="54981-102">\<typeparam > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="54981-102">\<typeparam> (Visual Basic)</span></span>
<span data-ttu-id="54981-103">Définit un nom de paramètre de type et une description.</span><span class="sxs-lookup"><span data-stu-id="54981-103">Defines a type parameter name and description.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="54981-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54981-104">Syntax</span></span>  
  
```xml  
<typeparam name="name">description</typeparam>  
```  
  
## <a name="parameters"></a><span data-ttu-id="54981-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54981-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="54981-106">Nom du paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="54981-106">The name of the type parameter.</span></span> <span data-ttu-id="54981-107">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="54981-107">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="54981-108">Description du paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="54981-108">A description of the type parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="54981-109">Notes</span><span class="sxs-lookup"><span data-stu-id="54981-109">Remarks</span></span>  
 <span data-ttu-id="54981-110">Utilisez le `<typeparam>` balise dans le commentaire pour un type générique ou une déclaration de membre générique décrire l’un des paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="54981-110">Use the `<typeparam>` tag in the comment for a generic type or generic member declaration to describe one of the type parameters.</span></span>  
  
 <span data-ttu-id="54981-111">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="54981-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="54981-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="54981-112">Example</span></span>  
 <span data-ttu-id="54981-113">Cet exemple utilise le `<typeparam>` balises pour décrire le `id` paramètre.</span><span class="sxs-lookup"><span data-stu-id="54981-113">This example uses the `<typeparam>` tag to describe the `id` parameter.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#8)]  
  
## <a name="see-also"></a><span data-ttu-id="54981-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54981-114">See also</span></span>

- [<span data-ttu-id="54981-115">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="54981-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
