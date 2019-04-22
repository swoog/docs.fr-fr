---
title: <c> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- c XML tag
- <c> XML tag
ms.assetid: 36ad5d1b-11f7-4012-8932-41962ac327d1
ms.openlocfilehash: 9be9f9e96fc1b79ea97d54c54352da63b93ef264
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58838038"
---
# <a name="c-visual-basic"></a>\<c > (Visual Basic)
Indique que le texte d’une description est code.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<c>text</c>  
```  
  
## <a name="parameters"></a>Paramètres  
  
|Paramètre|Description|  
|---|---|  
|`text`|Texte que vous souhaitez indiquer comme étant du code.|  
  
## <a name="remarks"></a>Notes  
 Le `<c>` balise vous donne un moyen d’indiquer que le texte d’une description doit être marqué en tant que code. Utilisez [\<code>](../../../visual-basic/language-reference/xmldoc/code.md) pour indiquer plusieurs lignes comme étant du code.  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `<c>` balise dans la section Résumé pour indiquer que `Counter` est le code.  
  
 [!code-vb[VbVbcnXmlDocComments#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
