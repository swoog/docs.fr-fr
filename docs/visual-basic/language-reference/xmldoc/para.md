---
title: <para> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <para> XML tag
- para XML tag
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
ms.openlocfilehash: de0387298f6ff505b286db35047065ef88541a62
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55280447"
---
# <a name="para-visual-basic"></a>\<para > (Visual Basic)
Spécifie que le contenu est mis en forme comme un paragraphe.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<para>content</para>  
```  
  
#### <a name="parameters"></a>Paramètres  
 `content`  
 Texte du paragraphe.  
  
## <a name="remarks"></a>Notes  
 Le `<para>` balise est destinée à l’intérieur d’une balise, tel que [ \<Résumé >](../../../visual-basic/language-reference/xmldoc/summary.md), [ \<remarks >](../../../visual-basic/language-reference/xmldoc/remarks.md), ou [ \<retourne >](../../../visual-basic/language-reference/xmldoc/returns.md), et vous permet d’ajouter une structure au texte.  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `<para>` balise pour fractionner la section Notes pour la `UpdateRecord` méthode en deux paragraphes.  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/para_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
