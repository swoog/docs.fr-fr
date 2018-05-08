---
title: 'Comment : rendre les entités sérialisables'
ms.date: 03/30/2017
ms.assetid: a6c5bf6e-064a-4f77-b74c-76b3a5dec309
ms.openlocfilehash: c3b877df9707e0f98dbc2238d910842649def07f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-make-entities-serializable"></a>Comment : rendre les entités sérialisables
Vous pouvez rendre des entités sérialisables lorsque vous générez votre code. Les classes d'entité sont décorées avec l'attribut <xref:System.Runtime.Serialization.DataContractAttribute> et les colonnes avec l'attribut <xref:System.Runtime.Serialization.DataMemberAttribute>.  
  
 Les développeurs à l’aide de Visual Studio peuvent utiliser le [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] à cet effet.  
  
 Si vous utilisez l’outil de ligne de commande SQLMetal, utilisez le **/serialization** option avec la `unidirectional` argument. Pour plus d’informations, consultez [SqlMetal.exe (outil de génération de code)](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md).  
  
## <a name="example"></a>Exemple  
 Les lignes de commande SQLMetal suivantes produisent des fichiers qui ont des entités sérialisables.  
  
```  
sqlmetal /code:nwserializable.vb /language:vb "c:\northwnd.mdf" /sprocs /functions /pluralize /serialization:unidirectional  
```  
  
```  
sqlmetal /code:nwserializable.cs /language:csharp "c:\northwnd.mdf" /sprocs /functions /pluralize /serialization:unidirectional  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Sérialisation](../../../../../../docs/framework/data/adonet/sql/linq/serialization.md)  
 [Création du modèle objet](../../../../../../docs/framework/data/adonet/sql/linq/creating-the-object-model.md)
