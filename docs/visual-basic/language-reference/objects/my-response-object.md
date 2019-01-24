---
title: My.Response (objet) (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.MyWebExtension.Response
- My.Response
helpviewer_keywords:
- My.Response object
ms.assetid: 626359bc-3165-40b4-bfaf-2c610e26eb5b
ms.openlocfilehash: c133e46b1adff0c100d49c4bfe5e17db4314a0bb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54738811"
---
# <a name="myresponse-object"></a><span data-ttu-id="3eef3-102">My.Response, objet</span><span class="sxs-lookup"><span data-stu-id="3eef3-102">My.Response Object</span></span>
<span data-ttu-id="3eef3-103">Obtient le <xref:System.Web.HttpResponse> objet associé à la <xref:System.Web.UI.Page>.</span><span class="sxs-lookup"><span data-stu-id="3eef3-103">Gets the <xref:System.Web.HttpResponse> object associated with the <xref:System.Web.UI.Page>.</span></span> <span data-ttu-id="3eef3-104">Cet objet vous permet d’envoyer des données de réponse HTTP à un client et contient des informations relatives à cette réponse.</span><span class="sxs-lookup"><span data-stu-id="3eef3-104">This object allows you to send HTTP response data to a client and contains information about that response.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3eef3-105">Notes</span><span class="sxs-lookup"><span data-stu-id="3eef3-105">Remarks</span></span>  
 <span data-ttu-id="3eef3-106">Le `My.Response` objet contient actuel <xref:System.Web.HttpResponse> objet associé à la page.</span><span class="sxs-lookup"><span data-stu-id="3eef3-106">The `My.Response` object contains the current <xref:System.Web.HttpResponse> object associated with the page.</span></span>  
  
 <span data-ttu-id="3eef3-107">Le `My.Response` objet est disponible uniquement pour [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] applications.</span><span class="sxs-lookup"><span data-stu-id="3eef3-107">The `My.Response` object is only available for [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] applications.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3eef3-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="3eef3-108">Example</span></span>  
 <span data-ttu-id="3eef3-109">L’exemple suivant obtient la collection d’en-têtes à partir de la `My.Request` objet et utilise le `My.Response` objet à écrire dans la page ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="3eef3-109">The following example gets the header collection from the `My.Request` object and uses the `My.Response` object to write it to the ASP.NET page.</span></span>  
  
 [!code-vb[VbVbalrMyWeb#1](../../../visual-basic/language-reference/objects/codesnippet/VisualBasic/my-response-object_1.aspx)]  
  
## <a name="see-also"></a><span data-ttu-id="3eef3-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3eef3-110">See also</span></span>
- <xref:System.Web.HttpResponse>
- [<span data-ttu-id="3eef3-111">My.Request (objet)</span><span class="sxs-lookup"><span data-stu-id="3eef3-111">My.Request Object</span></span>](../../../visual-basic/language-reference/objects/my-request-object.md)
