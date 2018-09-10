---
title: Modification d’arborescences XML (LINQ to XML) (C#)
ms.date: 07/20/2015
ms.assetid: 8ec47e6d-2363-4694-be46-8d5ca4d15fc9
ms.openlocfilehash: 55e75762772a071b97eecb7d6d78e28c3002a179
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43505717"
---
# <a name="modifying-xml-trees-linq-to-xml-c"></a>Modification d’arborescences XML (LINQ to XML) (C#)
[!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] est un magasin en mémoire pour une arborescence XML. Une fois que vous avez chargé ou analysé une arborescence XML à partir d’une source, [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] vous permet de modifier cette arborescence sur place, puis de la sérialiser, par exemple en l’enregistrant dans un fichier ou en l’envoyant vers un serveur distant.  
  
 Lorsque vous modifiez une arborescence sur place, vous utilisez certaines méthodes, telles que <xref:System.Xml.Linq.XContainer.Add%2A>.  
  
 Il existe cependant une autre approche, qui consiste à utiliser la construction fonctionnelle pour générer une nouvelle arborescence avec une forme différente. Cette approche peut s'avérer plus robuste et plus facile à développer, selon les types de modifications que vous devez apporter à votre arborescence XML et selon la taille de l'arborescence. La première rubrique dans cette section compare ces deux approches.  
  
## <a name="in-this-section"></a>Dans cette section  
  
|Rubrique|Description|  
|-----------|-----------------|  
|[Comparaison de la modification d’arborescence XML en mémoire et de la Construction fonctionnelle (LINQ to XML) (C#)](../../../../csharp/programming-guide/concepts/linq/in-memory-xml-tree-modification-vs-functional-construction-linq-to-xml.md)|Compare la modification d’une arborescence XML en mémoire à la construction fonctionnelle.|  
|[Ajout d’éléments, d’attributs et de nœuds à une arborescence XML (C#)](../../../../csharp/programming-guide/concepts/linq/adding-elements-attributes-and-nodes-to-an-xml-tree.md)|Fournit des informations sur l’ajout d’éléments, d’attributs ou de nœuds à une arborescence XML.|  
|[Modification d’éléments, d’attributs et de nœuds dans une arborescence XML](../../../../csharp/programming-guide/concepts/linq/modifying-elements-attributes-and-nodes-in-an-xml-tree.md)|Fournit des informations sur la modification d'éléments, d'attributs ou de nœuds existants.|  
|[Suppression d’éléments, d’attributs et de nœuds d’une arborescence XML (C#)](../../../../csharp/programming-guide/concepts/linq/removing-elements-attributes-and-nodes-from-an-xml-tree.md)|Fournit des informations sur la suppression d’éléments, d’attributs ou de nœuds d’une arborescence XML.|  
|[Gestion des paires nom/valeur (C#)](../../../../csharp/programming-guide/concepts/linq/maintaining-name-value-pairs.md)|Décrit comment maintenir des informations d'applications qu'il est préférable de conserver sous la forme de paires nom/valeur, telles que des informations de configuration ou des paramètres globaux.|  
|[Guide pratique pour modifier l’espace de noms pour toute une arborescence XML (C#)](../../../../csharp/programming-guide/concepts/linq/how-to-change-the-namespace-for-an-entire-xml-tree.md)|Montre comment déplacer une arborescence XML d’un espace de noms à un autre.|  
  
## <a name="see-also"></a>Voir aussi

- [Guide de programmation (LINQ to XML) (C#)](../../../../csharp/programming-guide/concepts/linq/programming-guide-linq-to-xml.md)
