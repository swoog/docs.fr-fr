---
title: "Comment : obtenir les propriétés de l'objet de système d'impression sans réflexion"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- PrintSystemObject [WPF], getting properties
ms.assetid: 43560f28-183d-41c1-b9d1-de7c2552273e
ms.openlocfilehash: 1fa8029b8245aef5e10e9082a1038fd89fc1c84e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33544728"
---
# <a name="how-to-get-print-system-object-properties-without-reflection"></a>Comment : obtenir les propriétés de l'objet de système d'impression sans réflexion
À l’aide de la réflexion pour détailler les propriétés (et les types de ces propriétés) sur un objet peut ralentir les performances de l’application. Le <xref:System.Printing.IndexedProperties> espace de noms fournit un moyen d’obtenir ces informations à l’aide de la réflexion.  
  
## <a name="example"></a>Exemple  
 Les étapes de cette procédure sont les suivantes.  
  
1.  Créez une instance du type. Dans l’exemple ci-dessous, le type est le <xref:System.Printing.PrintQueue> type qui est fourni avec Microsoft .NET Framework, mais un code presque identique doit fonctionner pour les types que vous dérivez de <xref:System.Printing.PrintSystemObject>.  
  
2.  Créer un <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> à partir du type <xref:System.Printing.PrintSystemObject.PropertiesCollection%2A>. Le <xref:System.Collections.DictionaryEntry.Value%2A> propriété de chaque entrée de ce dictionnaire est un objet de l’un des types dérivés de <xref:System.Printing.IndexedProperties.PrintProperty>.  
  
3.  Énumérer les membres du dictionnaire. Pour chacun d’eux, procédez comme suit.  
  
4.  Cast jusqu'à la valeur de chaque entrée à <xref:System.Printing.IndexedProperties.PrintProperty> et l’utiliser pour créer un <xref:System.Printing.IndexedProperties.PrintProperty> objet.  
  
5.  Obtenir le type de la <xref:System.Printing.IndexedProperties.PrintProperty.Value%2A> de chacune de la <xref:System.Printing.IndexedProperties.PrintProperty> objet.  
  
 [!code-csharp[GetPrintObjectPropertyTypesWithoutReflection#ShowPropertyTypesWithoutReflection](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GetPrintObjectPropertyTypesWithoutReflection/CSharp/Program.cs#showpropertytypeswithoutreflection)]
 [!code-vb[GetPrintObjectPropertyTypesWithoutReflection#ShowPropertyTypesWithoutReflection](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/GetPrintObjectPropertyTypesWithoutReflection/visualbasic/program.vb#showpropertytypeswithoutreflection)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Printing.IndexedProperties.PrintProperty>  
 <xref:System.Printing.PrintSystemObject>  
 <xref:System.Printing.IndexedProperties>  
 <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>  
 <xref:System.Printing.LocalPrintServer>  
 <xref:System.Printing.PrintQueue>  
 <xref:System.Collections.DictionaryEntry>  
 [Documents dans WPF](../../../../docs/framework/wpf/advanced/documents-in-wpf.md)  
 [Vue d’ensemble de l’impression](../../../../docs/framework/wpf/advanced/printing-overview.md)
