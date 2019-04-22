---
title: Les littéraux XML et les propriétés XML ne sont pas pris en charge dans du code incorporé au sein d'ASP.NET
ms.date: 07/20/2015
f1_keywords:
- vbc31200
- bc31200
helpviewer_keywords:
- BC31200
ms.assetid: 053e8cba-8584-45cc-9fa0-43d122779772
ms.openlocfilehash: 79be695478983055ae1f016cf841d733d3f4c430
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58813923"
---
# <a name="xml-literals-and-xml-properties-are-not-supported-in-embedded-code-within-aspnet"></a><span data-ttu-id="16c2a-102">Les littéraux XML et les propriétés XML ne sont pas pris en charge dans du code incorporé au sein d'ASP.NET</span><span class="sxs-lookup"><span data-stu-id="16c2a-102">XML literals and XML properties are not supported in embedded code within ASP.NET</span></span>
<span data-ttu-id="16c2a-103">Littéraux XML et les propriétés XML ne sont pas pris en charge dans du code incorporé au sein d’ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="16c2a-103">XML literals and XML properties are not supported in embedded code within ASP.NET.</span></span> <span data-ttu-id="16c2a-104">Pour utiliser les fonctionnalités XML, déplacez le code au code-behind.</span><span class="sxs-lookup"><span data-stu-id="16c2a-104">To use XML features, move the code to code-behind.</span></span>  
  
 <span data-ttu-id="16c2a-105">Un littéral XML ou une propriété d’axe XML est définie dans le code incorporé (`<%= =>`) dans un fichier ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="16c2a-105">An XML literal or XML axis property is defined within embedded code (`<%= =>`) in an ASP.NET file.</span></span>  
  
 <span data-ttu-id="16c2a-106">**ID d’erreur :** BC31200</span><span class="sxs-lookup"><span data-stu-id="16c2a-106">**Error ID:** BC31200</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="16c2a-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="16c2a-107">To correct this error</span></span>  
  
-   <span data-ttu-id="16c2a-108">Déplacer le code qui inclut le littéral XML ou une propriété d’axe XML vers un fichier de code-behind ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="16c2a-108">Move the code that includes the XML literal or XML axis property to an ASP.NET code-behind file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="16c2a-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16c2a-109">See also</span></span>

- [<span data-ttu-id="16c2a-110">Littéraux XML</span><span class="sxs-lookup"><span data-stu-id="16c2a-110">XML Literals</span></span>](../../../visual-basic/language-reference/xml-literals/index.md)
- [<span data-ttu-id="16c2a-111">Propriétés d’axe XML</span><span class="sxs-lookup"><span data-stu-id="16c2a-111">XML Axis Properties</span></span>](../../../visual-basic/language-reference/xml-axis/index.md)
- [<span data-ttu-id="16c2a-112">XML</span><span class="sxs-lookup"><span data-stu-id="16c2a-112">XML</span></span>](../../../visual-basic/programming-guide/language-features/xml/index.md)
