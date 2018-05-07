---
title: My.Response, objet
ms.date: 07/20/2015
f1_keywords:
- My.MyWebExtension.Response
- My.Response
helpviewer_keywords:
- My.Response object
ms.assetid: 626359bc-3165-40b4-bfaf-2c610e26eb5b
ms.openlocfilehash: 0a907d74112586e7b88c5a0a6f40080455454d7f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="myresponse-object"></a>My.Response, objet
Obtient le <xref:System.Web.HttpResponse> objet associé à la <xref:System.Web.UI.Page>. Cet objet vous permet d’envoyer des données de réponse HTTP à un client et contient des informations relatives à cette réponse.  
  
## <a name="remarks"></a>Notes  
 Le `My.Response` objet contient actuel <xref:System.Web.HttpResponse> objet associé à la page.  
  
 Le `My.Response` objet n’est disponible pour [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] applications.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant obtient la collection d’en-têtes à partir de la `My.Request` objet et utilise le `My.Response` objet à écrire dans la page ASP.NET.  
  
 [!code-vb[VbVbalrMyWeb#1](../../../visual-basic/language-reference/objects/codesnippet/VisualBasic/my-response-object_1.aspx)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Web.HttpResponse>  
 [My.Request (objet)](../../../visual-basic/language-reference/objects/my-request-object.md)
