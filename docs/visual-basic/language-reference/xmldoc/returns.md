---
title: '&lt;Retourne&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- returns XML tag
- <returns> XML tag
ms.assetid: a03a6469-d907-425d-882f-083187950e7e
ms.openlocfilehash: 47debcef2c6ce56fda4c4a0818c8e813b41ebad1
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2018
ms.locfileid: "42925016"
---
# <a name="ltreturnsgt-visual-basic"></a>&lt;Retourne&gt; (Visual Basic)
Spécifie la valeur de retour de la propriété ou la fonction.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<returns>description</returns>  
```  
  
#### <a name="parameters"></a>Paramètres  
 `description`  
 Description de la valeur de retour.  
  
## <a name="remarks"></a>Notes  
 Utilisez le `<returns>` balise dans le commentaire pour une déclaration de méthode décrire la valeur de retour.  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `<returns>` balise à expliquer en quoi le `DoesRecordExist` fonction renvoie.  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/returns_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
