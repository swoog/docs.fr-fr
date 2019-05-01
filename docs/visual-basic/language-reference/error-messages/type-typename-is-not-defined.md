---
title: Type '<typename>' non défini
ms.date: 07/20/2015
f1_keywords:
- vbc30002
- bc30002
helpviewer_keywords:
- BC30002
ms.assetid: b0faf204-57fd-44de-8c05-9db027eea663
ms.openlocfilehash: c2675d61307d92da1710368668f43af3559060a3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62032095"
---
# <a name="type-typename-is-not-defined"></a>Type '\<nom_type >' n’est pas défini
L’instruction a fait référence à un type qui n’a pas été défini. Vous pouvez définir un type dans une instruction de déclaration, tel que `Enum`, `Structure`, `Class`, ou `Interface`.  
  
 **ID d’erreur :** BC30002  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Vérifiez que la définition de type et sa référence utilisent tous deux la même orthographe.  
  
- Vérifiez que la définition de type est accessible à la référence. Par exemple, si le type est dans un autre module et a été déclaré `Private`, déplacez la définition de type vers le module de référence ou déclarez-le `Public`.  
  
- Assurez-vous que l’espace de noms du type n’est pas redéfini au sein de votre projet. Si tel est le cas, utilisez le `Global` mot clé pour qualifier le nom de type. Par exemple, si un projet définit un espace de noms nommé `System`, le <xref:System.Object?displayProperty=nameWithType> type n’est pas accessible sauf s’il est qualifié avec le `Global` mot clé : `Global.System.Object`.  
  
- Si le type est défini, mais la bibliothèque d’objets ou la bibliothèque de type dans lequel elle est définie n’est pas inscrit dans Visual Basic, cliquez sur **ajouter une référence** sur le **projet** menu et sélectionnez l’objet approprié bibliothèque ou bibliothèque de types.  
  
- Assurez-vous que le type est dans un assembly qui fait partie du profil .NET Framework ciblé. Pour plus d’informations, consultez [Dépannage des erreurs de ciblage du .NET Framework](/visualstudio/msbuild/troubleshooting-dotnet-framework-targeting-errors).  
  
## <a name="see-also"></a>Voir aussi

- [Espaces de noms dans Visual Basic](../../../visual-basic/programming-guide/program-structure/namespaces.md)
- [Enum (instruction)](../../../visual-basic/language-reference/statements/enum-statement.md)
- [Structure (instruction)](../../../visual-basic/language-reference/statements/structure-statement.md)
- [Class (instruction)](../../../visual-basic/language-reference/statements/class-statement.md)
- [Interface (instruction)](../../../visual-basic/language-reference/statements/interface-statement.md)
- [Gestion des références dans un projet](/visualstudio/ide/managing-references-in-a-project)
