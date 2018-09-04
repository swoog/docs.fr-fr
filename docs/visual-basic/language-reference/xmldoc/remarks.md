---
title: '&lt;Remarques&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <remarks> XML tag
- remarks XML tag
ms.assetid: c6241773-a7ed-41c9-9a8b-9722a0c606a9
ms.openlocfilehash: 97fca8758d9c21ac0b8f15bf9d5831750fbabe77
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43557074"
---
# <a name="ltremarksgt-visual-basic"></a>&lt;Remarques&gt; (Visual Basic)
Spécifie une section Notes pour le membre.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<remarks>description</remarks>  
```  
  
#### <a name="parameters"></a>Paramètres  
 `description`  
 Description du membre.  
  
## <a name="remarks"></a>Notes  
 Utilisez le `<remarks>` balise à ajouter des informations sur un type et de compléter les informations spécifiées avec [ \<Résumé >](../../../visual-basic/language-reference/xmldoc/summary.md).  
  
 Ces informations s’affichent dans l’Explorateur d’objets. Pour plus d’informations sur l’Explorateur d’objets, consultez [affichage de la Structure du Code](/visualstudio/ide/viewing-the-structure-of-code).  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `<remarks>` balise à expliquer en quoi le `UpdateRecord` méthode effectue.  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/remarks_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
