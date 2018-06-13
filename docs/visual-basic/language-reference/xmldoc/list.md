---
title: '&lt;liste&gt; (Visual Basic)'
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
ms.openlocfilehash: f03924217393e1e909b086b282f1c62ddb471522
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33603611"
---
# <a name="ltlistgt-visual-basic"></a>&lt;liste&gt; (Visual Basic)
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
  
#### <a name="parameters"></a>Paramètres  
 `type`  
 Le type de la liste. Doivent être des « puce » pour une liste à puces, le « nombre » pour une liste numérotée, ou « table » pour une table à deux colonnes.  
  
 `term`  
 Utilisé uniquement lorsque `type` est « table ». Un terme à définir, qui est défini dans la balise de description.  
  
 `description`  
 Lorsque `type` est « puce » ou « number », `description` est un élément dans la liste lorsque `type` est « table », `description` est la définition de `term`.  
  
## <a name="remarks"></a>Notes  
 Le `<listheader>` bloc définit le titre d’une table ou une définition de liste. Lorsque vous définissez une table, il vous suffit de fournir une entrée pour `term` dans l’en-tête.  
  
 Chaque élément dans la liste est spécifié avec un `<item>` bloc. Lorsque vous créez une liste de définitions, vous devez spécifier les deux `term` et `description`. Toutefois, pour une table, une liste à puces ou une liste numérotée, il vous suffit de fournir une entrée pour `description`.  
  
 Une liste ou une table peut comporter autant `<item>` bloque en fonction des besoins.  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `<list>` balise pour définir une liste à puces dans la section Notes.  
  
 [!code-vb[VbVbcnXmlDocComments#5](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/list_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)
