---
title: '&lt;code&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- code XML tag
- <code> XML tag
ms.assetid: 925e5342-be05-45f2-bf66-7398bbd6710e
ms.openlocfilehash: 8a4708a7b50b0e221c1ebe7f95d4f8ff80cd1ebe
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54566305"
---
# <a name="ltcodegt-visual-basic"></a>&lt;code&gt; (Visual Basic)
Indique que le texte est plusieurs lignes de code.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<code>content</code>  
```  
  
#### <a name="parameters"></a>Paramètres  
 `content`  
 Texte à marquer en tant que code.  
  
## <a name="remarks"></a>Notes  
 Utilisez le `<code>` balise pour indiquer plusieurs lignes comme étant du code. Utilisez [\<c>](../../../visual-basic/language-reference/xmldoc/c.md) pour indiquer que le texte d’une description doit être marqué comme étant du code.  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le \<code > balise pour inclure l’exemple de code pour l’utilisation de la `ID` champ.  
  
 [!code-vb[VbVbcnXmlDocComments#2](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/code_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
