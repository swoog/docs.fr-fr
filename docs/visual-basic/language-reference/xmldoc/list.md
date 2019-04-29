---
title: <list> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- listheader XML tag
- <item> XML tag
- <list> XML tag
- <listheader> XML tag
- term XML tag
- list XML tag
- <description> XML tag
- description XML tag
- item XML tag
- <term> XML tag
ms.assetid: ec35fced-d58e-4520-a764-0691256e014b
ms.openlocfilehash: 7d7b85867f4c701322c5e6c31f2d89ab38fad05d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61940872"
---
# <a name="list-visual-basic"></a>\<liste > (Visual Basic)
Définit une liste ou une table.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<list type="type">  
   <listheader>  
      <term>term</term>  
      <description>description</description>  
   </listheader>  
   <item>  
      <term>term</term>  
      <description>description</description>  
   </item>  
</list>  
```  
  
## <a name="parameters"></a>Paramètres  
 `type`  
 Le type de la liste. Doit être un « bullet » pour une liste à puces, le « nombre » pour une liste numérotée, ou « table » pour une table de deux colonnes.  
  
 `term`  
 Utilisé uniquement lorsque `type` est « table ». Terme à définir, qui est défini dans la balise de description.  
  
 `description`  
 Lorsque `type` est « puce » ou « numéro », `description` est un élément dans la liste lorsque `type` est « table », `description` est la définition de `term`.  
  
## <a name="remarks"></a>Notes  
 Le `<listheader>` bloc définit le titre d’une table ou une définition de liste. Lorsque vous définissez une table, il vous suffit de fournir une entrée pour `term` dans l’en-tête.  
  
 Chaque élément dans la liste est spécifié avec un `<item>` bloc. Lorsque vous créez une liste de définitions, vous devez spécifier les `term` et `description`. Toutefois, pour une table, une liste à puces ou une liste numérotée, il vous suffit de fournir une entrée pour `description`.  
  
 Une liste ou une table peut avoir autant `<item>` bloque en fonction des besoins.  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `<list>` balise pour définir une liste à puces dans la section Notes.  
  
 [!code-vb[VbVbcnXmlDocComments#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#5)]  
  
## <a name="see-also"></a>Voir aussi

- [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
