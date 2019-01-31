---
title: L'expression de type '<type>' ne peut pas être interrogée
ms.date: 07/20/2015
f1_keywords:
- bc36593
- vbc36593
helpviewer_keywords:
- BC36593
ms.assetid: 6f1f5860-bf97-4885-9ebb-bc87d028095c
ms.openlocfilehash: 06b2a7f5c6bd838d09fd39f31778462c364fb8bd
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261254"
---
# <a name="expression-of-type-type-is-not-queryable"></a>Expression de type \<type > ne peut pas être interrogée
Expression de type \<type > ne peut pas être interrogée. Assurez-vous que vous ne manque une importation d’espace de noms de référence ou d’assembly pour le fournisseur LINQ.  
  
 Types requêtables sont définies dans le <xref:System.Linq>, <xref:System.Data.Linq>, et <xref:System.Xml.Linq> espaces de noms. Vous devez importer un ou plusieurs de ces espaces de noms pour effectuer des requêtes LINQ.  
  
 Le <xref:System.Linq> espace de noms vous permet aux objets de requête tels que les collections et tableaux à l’aide de LINQ.  
  
 Le <xref:System.Data.Linq> espace de noms vous permet d’interroger des jeux de données ADO.NET et des bases de données SQL Server à l’aide de LINQ.  
  
 Le <xref:System.Xml.Linq> espace de noms vous permet d’interroger XML à l’aide de LINQ et à utiliser les fonctionnalités XML dans Visual Basic.  
  
 **ID d’erreur :** BC36593  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Ajouter un `Import` instruction pour la <xref:System.Linq>, <xref:System.Data.Linq>, ou <xref:System.Xml.Linq> espace de noms à votre fichier de code. Vous pouvez également importer des espaces de noms pour votre projet à l’aide de la **références** page du Concepteur de projets (**mon projet**).  
  
2.  Vérifiez que le type que vous avez identifié comme source de votre requête est un type requêtable. Autrement dit, un type qui implémente <xref:System.Collections.Generic.IEnumerable%601> ou <xref:System.Linq.IQueryable%601>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Linq>
- <xref:System.Data.Linq>
- <xref:System.Xml.Linq>
- [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [LINQ](../../../visual-basic/programming-guide/language-features/linq/index.md)
- [XML](../../../visual-basic/programming-guide/language-features/xml/index.md)
- [Références et l’instruction Imports](../../../visual-basic/programming-guide/program-structure/references-and-the-imports-statement.md)
- [Imports (instruction) (espace de noms et type .NET)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)
- [Page Références, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/references-page-project-designer-visual-basic)
