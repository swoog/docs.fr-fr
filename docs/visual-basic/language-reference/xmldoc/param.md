---
title: '&lt;Param&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- param XML tag
- <param> XML tag
ms.assetid: 4e32e86f-f6f3-4301-b7fc-2f321fb54368
ms.openlocfilehash: c992c96303eb1441eaf667693b7aefb5361b196c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33602919"
---
# <a name="ltparamgt-visual-basic"></a><span data-ttu-id="6bdfb-102">&lt;Param&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6bdfb-102">&lt;param&gt; (Visual Basic)</span></span>
<span data-ttu-id="6bdfb-103">Définit un nom de paramètre et une description.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-103">Defines a parameter name and description.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6bdfb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bdfb-104">Syntax</span></span>  
  
```xml  
<param name="name">description</param>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6bdfb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bdfb-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="6bdfb-106">Nom d’un paramètre de méthode.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-106">The name of a method parameter.</span></span> <span data-ttu-id="6bdfb-107">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="6bdfb-107">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="6bdfb-108">Description du paramètre.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-108">A description for the parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6bdfb-109">Notes</span><span class="sxs-lookup"><span data-stu-id="6bdfb-109">Remarks</span></span>  
 <span data-ttu-id="6bdfb-110">Le `<param>` balise doit être utilisée dans le commentaire pour une déclaration de méthode pour décrire l’un des paramètres de la méthode.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-110">The `<param>` tag should be used in the comment for a method declaration to describe one of the parameters for the method.</span></span>  
  
 <span data-ttu-id="6bdfb-111">Le texte de la `<param>` balise apparaît dans les emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="6bdfb-111">The text for the `<param>` tag will appear in the following locations:</span></span>  
  
-   <span data-ttu-id="6bdfb-112">Informations sur les paramètres d’IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-112">Parameter Info of IntelliSense.</span></span> <span data-ttu-id="6bdfb-113">Pour plus d’informations, consultez [Utilisation d’IntelliSense](/visualstudio/ide/using-intellisense).</span><span class="sxs-lookup"><span data-stu-id="6bdfb-113">For more information, see [Using IntelliSense](/visualstudio/ide/using-intellisense).</span></span>  
  
-   <span data-ttu-id="6bdfb-114">Explorateur d’objets.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-114">Object Browser.</span></span> <span data-ttu-id="6bdfb-115">Pour plus d’informations, consultez [Affichage de la structure du code](/visualstudio/ide/viewing-the-structure-of-code).</span><span class="sxs-lookup"><span data-stu-id="6bdfb-115">For more information, see [Viewing the Structure of Code](/visualstudio/ide/viewing-the-structure-of-code).</span></span>  
  
 <span data-ttu-id="6bdfb-116">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-116">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6bdfb-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="6bdfb-117">Example</span></span>  
 <span data-ttu-id="6bdfb-118">Cet exemple utilise le `<param>` balises pour décrire le `id` paramètre.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-118">This example uses the `<param>` tag to describe the `id` parameter.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/param_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="6bdfb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bdfb-119">See Also</span></span>  
 [<span data-ttu-id="6bdfb-120">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="6bdfb-120">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)
