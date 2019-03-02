---
title: My.Response (objet) (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.MyWebExtension.Response
- My.Response
helpviewer_keywords:
- My.Response object
ms.assetid: 626359bc-3165-40b4-bfaf-2c610e26eb5b
ms.openlocfilehash: 5677108ac31733577915e15972386d8de5ccba49
ms.sourcegitcommit: 41c0637e894fbcd0713d46d6ef1866f08dc321a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57203348"
---
# <a name="myresponse-object"></a>My.Response, objet
Obtient le <xref:System.Web.HttpResponse> objet associé à la <xref:System.Web.UI.Page>. Cet objet vous permet d’envoyer des données de réponse HTTP à un client et contient des informations relatives à cette réponse.  
  
## <a name="remarks"></a>Notes  
 Le `My.Response` objet contient actuel <xref:System.Web.HttpResponse> objet associé à la page.  
  
 Le `My.Response` objet est disponible uniquement pour [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] applications.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant obtient la collection d’en-têtes à partir de la `My.Request` objet et utilise le `My.Response` objet à écrire dans la page ASP.NET.  
  
 [!code-vb[VbVbalrMyWeb#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyWeb/VB/Default.aspx#1)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Web.HttpResponse>
- [My.Request (objet)](../../../visual-basic/language-reference/objects/my-request-object.md)
