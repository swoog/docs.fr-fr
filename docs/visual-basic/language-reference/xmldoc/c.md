---
title: '&lt;c&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- c XML tag
- <c> XML tag
ms.assetid: 36ad5d1b-11f7-4012-8932-41962ac327d1
ms.openlocfilehash: 0e3ed08a62e9a52efa231c573a8061ff92d3cee0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54604155"
---
# <a name="ltcgt-visual-basic"></a>&lt;c&gt; (Visual Basic)
Indique que le texte d’une description est code.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<c>text</c>  
```  
  
#### <a name="parameters"></a>Paramètres  
  
|Paramètre|Description|  
|---|---|  
|`text`|Texte que vous souhaitez indiquer comme étant du code.|  
  
## <a name="remarks"></a>Notes  
 Le `<c>` balise vous donne un moyen d’indiquer que le texte d’une description doit être marqué en tant que code. Utilisez [\<code>](../../../visual-basic/language-reference/xmldoc/code.md) pour indiquer plusieurs lignes comme étant du code.  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `<c>` balise dans la section Résumé pour indiquer que `Counter` est le code.  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/c_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
