---
title: <summary> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <summary> XML tag
- summary XML tag
ms.assetid: 861c847d-dd94-478a-aa23-bf4899cdc848
ms.openlocfilehash: 3f40177b717452f316672c29c6455faf33e01b4d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55282709"
---
# <a name="summary-visual-basic"></a>\<Résumé > (Visual Basic)
Spécifie le résumé du membre.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<summary>description</summary>  
```  
  
#### <a name="parameters"></a>Paramètres  
 `description`  
 Résumé de l’objet.  
  
## <a name="remarks"></a>Notes  
 Utilisez le `<summary>` balise pour décrire un type ou un membre de type. Utilisez [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md) pour ajouter des informations supplémentaires à une description de type.  
  
 Le texte pour le `<summary>` balise est la seule source d’informations sur le type dans IntelliSense et s’affiche également dans l’Explorateur d’objets. Pour plus d’informations sur l’Explorateur d’objets, consultez [affichage de la Structure du Code](/visualstudio/ide/viewing-the-structure-of-code).  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `<summary>` balises pour décrire le `ResetCounter` méthode et `Counter` propriété.  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/summary_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
