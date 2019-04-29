---
title: <paramref> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- paramref XML tag
- <paramref> XML tag
ms.assetid: 8979d53b-beb1-41b7-b41e-6bbea1c17a03
ms.openlocfilehash: 3e2bf7990343a325bbecc56f6d3754a77f1e08e2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61940840"
---
# <a name="paramref-visual-basic"></a>\<paramref > (Visual Basic)
Met en forme un mot en tant que paramètre.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<paramref name="name"/>  
```  
  
## <a name="parameters"></a>Paramètres  
 `name`  
 Nom du paramètre auquel faire référence. Mettez le nom entre guillemets doubles (" ").  
  
## <a name="remarks"></a>Notes  
 Le `<paramref>` balise vous donne un moyen d’indiquer qu’un mot est un paramètre. Le fichier XML peut être traité pour mettre en forme ce paramètre d’une manière distincte.  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `<paramref>` balise pour faire référence à la `id` paramètre.  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a>Voir aussi

- [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
