---
title: 'Procédure : Rendre les entités sérialisables'
ms.date: 03/30/2017
ms.assetid: a6c5bf6e-064a-4f77-b74c-76b3a5dec309
ms.openlocfilehash: bbe40ec448bef5f62d4182d96f82c6308639e27f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59086765"
---
# <a name="how-to-make-entities-serializable"></a><span data-ttu-id="bb369-102">Procédure : Rendre les entités sérialisables</span><span class="sxs-lookup"><span data-stu-id="bb369-102">How to: Make Entities Serializable</span></span>
<span data-ttu-id="bb369-103">Vous pouvez rendre des entités sérialisables lorsque vous générez votre code.</span><span class="sxs-lookup"><span data-stu-id="bb369-103">You can make entities serializable when you generate your code.</span></span> <span data-ttu-id="bb369-104">Les classes d'entité sont décorées avec l'attribut <xref:System.Runtime.Serialization.DataContractAttribute> et les colonnes avec l'attribut <xref:System.Runtime.Serialization.DataMemberAttribute>.</span><span class="sxs-lookup"><span data-stu-id="bb369-104">Entity classes are decorated with the <xref:System.Runtime.Serialization.DataContractAttribute> attribute, and columns with the <xref:System.Runtime.Serialization.DataMemberAttribute> attribute.</span></span>  
  
 <span data-ttu-id="bb369-105">Les développeurs à l’aide de Visual Studio peuvent utiliser le [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] à cet effet.</span><span class="sxs-lookup"><span data-stu-id="bb369-105">Developers using Visual Studio can use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] for this purpose.</span></span>  
  
 <span data-ttu-id="bb369-106">Si vous utilisez l’outil de ligne de commande SQLMetal, utilisez le **/serialization** option avec la `unidirectional` argument.</span><span class="sxs-lookup"><span data-stu-id="bb369-106">If you are using the SQLMetal command-line tool, use the **/serialization** option with the `unidirectional` argument.</span></span> <span data-ttu-id="bb369-107">Pour plus d’informations, consultez [SqlMetal.exe (outil de génération de code)](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="bb369-107">For more information, see [SqlMetal.exe (Code Generation Tool)](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="bb369-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="bb369-108">Example</span></span>  
 <span data-ttu-id="bb369-109">Les lignes de commande SQLMetal suivantes produisent des fichiers qui ont des entités sérialisables.</span><span class="sxs-lookup"><span data-stu-id="bb369-109">The following SQLMetal command lines produce files that have serializable entities.</span></span>  
  
```  
sqlmetal /code:nwserializable.vb /language:vb "c:\northwnd.mdf" /sprocs /functions /pluralize /serialization:unidirectional  
```  
  
```  
sqlmetal /code:nwserializable.cs /language:csharp "c:\northwnd.mdf" /sprocs /functions /pluralize /serialization:unidirectional  
```  
  
## <a name="see-also"></a><span data-ttu-id="bb369-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb369-110">See also</span></span>

- [<span data-ttu-id="bb369-111">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="bb369-111">Serialization</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/serialization.md)
- [<span data-ttu-id="bb369-112">Création du modèle objet</span><span class="sxs-lookup"><span data-stu-id="bb369-112">Creating the Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/creating-the-object-model.md)
