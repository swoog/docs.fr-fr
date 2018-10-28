---
title: LINQ to SQL
ms.date: 03/30/2017
ms.assetid: 73d13345-eece-471a-af40-4cc7a2f11655
ms.openlocfilehash: 141505eed8e76bb5f9811b5d2bdc166885905cde
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50034180"
---
# <a name="linq-to-sql"></a>LINQ to SQL
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] est un composant de la version 3.5 du [!INCLUDE[dnprdnshort](../../../../../../includes/dnprdnshort-md.md)] qui fournit une infrastructure runtime pour gérer les données relationnelles comme des objets.  
  
> [!NOTE]
>  Les données relationnelles apparaissent comme une collection de tables à deux dimensions (*relations* ou *fichiers plats*) où des colonnes communes relient les tables entre elles. Pour utiliser efficacement [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], vous devez posséder quelques connaissances des principes sous-jacents des bases de données relationnelles.  
  
 Dans [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], le modèle de données d’une base de données relationnelle est mappé à un modèle objet exprimé dans le langage de programmation du développeur. Lors de l'exécution de l'application, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] traduit des requêtes LINQ dans le modèle objet en SQL et les envoie à la base de données pour exécution. Lorsque la base de données retourne les résultats, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] les traduit en objets que vous pouvez utiliser dans votre propre langage de programmation.  
  
 Les développeurs qui utilisent Visual Studio généralement utilisent le [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)], qui fournit une interface utilisateur pour l’implémentation de nombreuses fonctionnalités de [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].  
  
 La documentation incluse avec cette mise en production de [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] décrit les blocs de construction de base, les processus et les techniques dont vous avez besoin pour générer des applications [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]. Vous pouvez également rechercher Microsoft Docs des problèmes spécifiques, et vous pouvez participer à la [Forum LINQ](https://go.microsoft.com/fwlink/?LinkId=76488), où vous pourrez aborder des sujets plus complexes avec des experts. Enfin, le [LINQ to SQL : Language-Integrated Query pour les données relationnelles](https://go.microsoft.com/fwlink/?LinkId=93205) détails du livre blanc [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] technologie, obtenir des exemples de code Visual Basic et c#.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Prise en main](../../../../../../docs/framework/data/adonet/sql/linq/getting-started.md)  
 Fournit une vue d’ensemble de [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] et des informations pour se familiariser avec l’utilisation de [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].  
  
 [Guide de programmation](../../../../../../docs/framework/data/adonet/sql/linq/programming-guide.md)  
 Explique comment effectuer les tâches de mappage, d’interrogation, de mise à jour, de débogage et d’autres tâches de ce type.  
  
 [Référence](../../../../../../docs/framework/data/adonet/sql/linq/reference.md)  
 Fournit des informations de référence sur plusieurs aspects de [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]. Les rubriques incluent le mappage de type CLR-SQL, la traduction d'opérateur de requête standard, etc.  
  
 [Exemples](../../../../../../docs/framework/data/adonet/sql/linq/samples.md)  
 Fournit des liens vers des exemples Visual Basic et c#.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [LINQ (Language Integrated Query)](https://msdn.microsoft.com/library/a73c4aec-5d15-4e98-b962-1274021ea93d)  
 Fournit une vue d'ensemble des technologies [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)].  
  
 [LINQ](../../../../../visual-basic/programming-guide/language-features/linq/index.md)  
 Décrit [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)] technologies pour les utilisateurs de Visual Basic.  
  
 [LINQ et ADO.NET](../../../../../../docs/framework/data/adonet/linq-and-ado-net.md)  
 Fournit des liens vers le portail d'[!INCLUDE[vstecado](../../../../../../includes/vstecado-md.md)].  
  
 [Procédures pas à pas LINQ to SQL](https://msdn.microsoft.com/library/308e66ac-f704-4e00-9b4e-7af0045a2374)  
 Répertorie les procédures pas à pas disponibles pour [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].  
  
 [Téléchargement d’exemples de base de données](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)  
 Explique comment télécharger les exemples de base de données utilisés dans la documentation.  
  
 [Vue d’ensemble de la technologie LinqDataSource](https://msdn.microsoft.com/library/104cfc3f-7385-47d3-8a51-830dfa791136)  
 Décrit comment le contrôle <xref:System.Web.UI.WebControls.LinqDataSource> expose [!INCLUDE[vbteclinqext](../../../../../../includes/vbteclinqext-md.md)] aux développeurs de sites Web via l'architecture de contrôle de source de données d'[!INCLUDE[vstecasp](../../../../../../includes/vstecasp-md.md)].
