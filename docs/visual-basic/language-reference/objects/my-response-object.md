---
title: My.Response (objet) (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.MyWebExtension.Response
- My.Response
helpviewer_keywords:
- My.Response object
ms.assetid: 626359bc-3165-40b4-bfaf-2c610e26eb5b
ms.openlocfilehash: 0e49a3b5732ee1a3626666ce06e366c4940eca05
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65881963"
---
# <a name="myresponse-object"></a><span data-ttu-id="01c35-102">My.Response, objet</span><span class="sxs-lookup"><span data-stu-id="01c35-102">My.Response Object</span></span>
<span data-ttu-id="01c35-103">Obtient le <xref:System.Web.HttpResponse> objet associé à la <xref:System.Web.UI.Page>.</span><span class="sxs-lookup"><span data-stu-id="01c35-103">Gets the <xref:System.Web.HttpResponse> object associated with the <xref:System.Web.UI.Page>.</span></span> <span data-ttu-id="01c35-104">Cet objet vous permet d’envoyer des données de réponse HTTP à un client et contient des informations relatives à cette réponse.</span><span class="sxs-lookup"><span data-stu-id="01c35-104">This object allows you to send HTTP response data to a client and contains information about that response.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="01c35-105">Notes</span><span class="sxs-lookup"><span data-stu-id="01c35-105">Remarks</span></span>  
 <span data-ttu-id="01c35-106">Le `My.Response` objet contient actuel <xref:System.Web.HttpResponse> objet associé à la page.</span><span class="sxs-lookup"><span data-stu-id="01c35-106">The `My.Response` object contains the current <xref:System.Web.HttpResponse> object associated with the page.</span></span>  
  
 <span data-ttu-id="01c35-107">Le `My.Response` objet est uniquement disponible pour les applications ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="01c35-107">The `My.Response` object is only available for ASP.NET applications.</span></span>  
  
## <a name="example"></a><span data-ttu-id="01c35-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="01c35-108">Example</span></span>  
 <span data-ttu-id="01c35-109">L’exemple suivant obtient la collection d’en-têtes à partir de la `My.Request` objet et utilise le `My.Response` objet à écrire dans la page ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="01c35-109">The following example gets the header collection from the `My.Request` object and uses the `My.Response` object to write it to the ASP.NET page.</span></span>  
  
 [!code-vb[VbVbalrMyWeb#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyWeb/VB/Default.aspx#1)]  
  
## <a name="see-also"></a><span data-ttu-id="01c35-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01c35-110">See also</span></span>

- <xref:System.Web.HttpResponse>
- [<span data-ttu-id="01c35-111">My.Request (objet)</span><span class="sxs-lookup"><span data-stu-id="01c35-111">My.Request Object</span></span>](../../../visual-basic/language-reference/objects/my-request-object.md)
