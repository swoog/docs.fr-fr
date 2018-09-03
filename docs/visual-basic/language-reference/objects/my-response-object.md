---
title: My.Response (objet) (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.MyWebExtension.Response
- My.Response
helpviewer_keywords:
- My.Response object
ms.assetid: 626359bc-3165-40b4-bfaf-2c610e26eb5b
ms.openlocfilehash: d5f49529a2593093a234babc22f64b591ea3cc61
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43479810"
---
# <a name="myresponse-object"></a>My.Response, objet
Obtient le <xref:System.Web.HttpResponse> objet associé à la <xref:System.Web.UI.Page>. Cet objet vous permet d’envoyer des données de réponse HTTP à un client et contient des informations relatives à cette réponse.  
  
## <a name="remarks"></a>Notes  
 Le `My.Response` objet contient actuel <xref:System.Web.HttpResponse> objet associé à la page.  
  
 Le `My.Response` objet est disponible uniquement pour [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] applications.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant obtient la collection d’en-têtes à partir de la `My.Request` objet et utilise le `My.Response` objet à écrire dans la page ASP.NET.  
  
 [!code-vb[VbVbalrMyWeb#1](../../../visual-basic/language-reference/objects/codesnippet/VisualBasic/my-response-object_1.aspx)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Web.HttpResponse>  
 [My.Request (objet)](../../../visual-basic/language-reference/objects/my-request-object.md)
