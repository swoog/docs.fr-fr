---
title: <seealso> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <seealso> XML tag
- seealso XML tag
ms.assetid: 36050c95-1af2-4284-b9b6-1a70691ed978
ms.openlocfilehash: 9f857be6d0bd46233a49c7d2ff0931670baa95a6
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56965298"
---
# <a name="seealso-visual-basic"></a>\<seealso > (Visual Basic)
Spécifie un lien qui apparaît dans la section Voir aussi.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<seealso cref="member"/>  
```  
  
#### <a name="parameters"></a>Paramètres  
 `member`  
 Référence à un membre ou un champ qu’il est possible d’appeler à partir de l’environnement de compilation actuel. Le compilateur vérifie que l’élément de code donné existe, et qu’il passe `member` au nom d’élément dans le code XML de sortie. `member` doit apparaître entre guillemets doubles (" ").  
  
## <a name="remarks"></a>Notes  
 Utilisez le `<seealso>` balise pour spécifier le texte que vous souhaitez voir apparaître dans une section Voir aussi. Utilisez [\<see>](../../../visual-basic/language-reference/xmldoc/see.md) pour spécifier un lien à partir de l’intérieur du texte.  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `<seealso>` balise dans le `DoesRecordExist` section pour faire référence à la section Notes le `UpdateRecord` (méthode).  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a>Voir aussi
- [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
