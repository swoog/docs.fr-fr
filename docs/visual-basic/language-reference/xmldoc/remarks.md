---
title: <remarks> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <remarks> XML tag
- remarks XML tag
ms.assetid: c6241773-a7ed-41c9-9a8b-9722a0c606a9
ms.openlocfilehash: 5065d43a0d3262ebe89d25351f791022bfd87077
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57502564"
---
# <a name="remarks-visual-basic"></a>\<remarks > (Visual Basic)
Spécifie une section Notes pour le membre.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<remarks>description</remarks>  
```  
  
## <a name="parameters"></a>Paramètres  
 `description`  
 Description du membre.  
  
## <a name="remarks"></a>Notes  
 Utilisez le `<remarks>` balise à ajouter des informations sur un type et de compléter les informations spécifiées avec [ \<Résumé >](../../../visual-basic/language-reference/xmldoc/summary.md).  
  
 Ces informations s’affichent dans l’Explorateur d’objets. Pour plus d’informations sur l’Explorateur d’objets, consultez [affichage de la Structure du Code](/visualstudio/ide/viewing-the-structure-of-code).  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `<remarks>` balise à expliquer en quoi le `UpdateRecord` méthode effectue.  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a>Voir aussi
- [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
