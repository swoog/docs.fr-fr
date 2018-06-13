---
title: '&lt;code&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- code XML tag
- <code> XML tag
ms.assetid: 925e5342-be05-45f2-bf66-7398bbd6710e
ms.openlocfilehash: 9ec9d23f1f62358dc272f9764f88e3bb2ba41f78
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33599750"
---
# <a name="ltcodegt-visual-basic"></a>&lt;code&gt; (Visual Basic)
Indique que le texte est plusieurs lignes de code.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<code>content</code>  
```  
  
#### <a name="parameters"></a>Paramètres  
 `content`  
 Texte à marquer comme étant du code.  
  
## <a name="remarks"></a>Notes  
 Utilisez le `<code>` balise pour indiquer plusieurs lignes comme du code. Utilisez [\<c>](../../../visual-basic/language-reference/xmldoc/c.md) pour indiquer que le texte d’une description doit être marqué comme étant du code.  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le \<code > balise à inclure l’exemple de code pour l’utilisation de la `ID` champ.  
  
 [!code-vb[VbVbcnXmlDocComments#2](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/code_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)
