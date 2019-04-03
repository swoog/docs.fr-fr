---
title: My.Request (objet) (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.MyWebExtension.Request
- My.Request
helpviewer_keywords:
- My.Request object
ms.assetid: 93d5f0e2-6b60-4a2c-8652-d90216f6ad10
ms.openlocfilehash: 08212dc5fe563ce84be02ab706b56195a0636894
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58836621"
---
# <a name="myrequest-object"></a>My.Request, objet
Obtient l’objet <xref:System.Web.HttpRequest> pour la page demandée.  
  
## <a name="remarks"></a>Notes  
 L’objet `My.Request` contient des informations sur la requête HTTP en cours.  
  
 L’objet `My.Request` est disponible uniquement pour les applications ASP.NET.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant obtient la collection d’en-têtes à partir de la `My.Request` objet et utilise le `My.Response` objet à écrire dans la page ASP.NET.  
  
 [!code-vb[VbVbalrMyWeb#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyWeb/VB/Default.aspx#1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Web.HttpRequest>
- [My.Response (objet)](../../../visual-basic/language-reference/objects/my-response-object.md)
