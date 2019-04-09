---
title: 'Procédure : Cloner une imprimante'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- print queues [WPF]
- cloning printers [WPF]
- printers [WPF], cloning
- print queues [WPF], cloning
- cloning print queues [WPF]
ms.assetid: dd6997c9-fe04-40f8-88a6-92e3ac0889eb
ms.openlocfilehash: f654c9f1431a0ab8aa4df568b405dabf881bb1bc
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59104089"
---
# <a name="how-to-clone-a-printer"></a>Procédure : Cloner une imprimante
La plupart des entreprises achètera, à un moment donné, plusieurs imprimantes du même modèle. En règle générale, celles-ci sont toutes installées avec les paramètres de configuration quasiment identiques. L’installation de chaque imprimante peut être fastidieuse et sujette aux erreurs. Le <xref:System.Printing.IndexedProperties?displayProperty=nameWithType> espace de noms et le <xref:System.Printing.PrintServer.InstallPrintQueue%2A> classe qui sont exposés avec Microsoft .NET Framework rend possible d’installer instantanément n’importe quel nombre de files d’attente à l’impression supplémentaires qui sont clonés à partir d’une file d’attente d’impression existante.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple ci-dessous, la deuxième file d’impression est cloné à partir d’une file d’attente d’impression existante. La deuxième est différent de la première uniquement dans son nom, un emplacement, un port et un état partagé. Voici les principales étapes pour y parvenir.  
  
1.  Créer un <xref:System.Printing.PrintQueue> objet pour l’imprimante existante qui va être clonée.  
  
2.  Créer un <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> à partir de la <xref:System.Printing.PrintSystemObject.PropertiesCollection%2A> de la <xref:System.Printing.PrintQueue>. Le <xref:System.Collections.DictionaryEntry.Value%2A> propriété de chaque entrée dans ce dictionnaire est un objet d’un des types dérivés de <xref:System.Printing.IndexedProperties.PrintProperty>. Il existe deux façons de définir la valeur d’une entrée dans ce dictionnaire.  
  
    -   Utiliser le dictionnaire **supprimer** et <xref:System.Printing.IndexedProperties.PrintPropertyDictionary.Add%2A> méthodes pour supprimer l’entrée, puis ajoutez-le à nouveau avec la valeur souhaitée.  
  
    -   Utiliser le dictionnaire <xref:System.Printing.IndexedProperties.PrintPropertyDictionary.SetProperty%2A> (méthode).  
  
     L’exemple ci-dessous illustre les deux sens.  
  
3.  Créer un <xref:System.Printing.IndexedProperties.PrintBooleanProperty> de l’objet et définissez son <xref:System.Printing.IndexedProperties.PrintProperty.Name%2A> « IsShared » et ses <xref:System.Printing.IndexedProperties.PrintBooleanProperty.Value%2A> à `true`.  
  
4.  Utilisez le <xref:System.Printing.IndexedProperties.PrintBooleanProperty> objet à la valeur de la <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>de saisie de « IsShared ».  
  
5.  Créer un <xref:System.Printing.IndexedProperties.PrintStringProperty> de l’objet et définissez son <xref:System.Printing.IndexedProperties.PrintProperty.Name%2A> « ShareName » et ses <xref:System.Printing.IndexedProperties.PrintStringProperty.Value%2A> un appropriés <xref:System.String>.  
  
6.  Utilisez le <xref:System.Printing.IndexedProperties.PrintStringProperty> objet à la valeur de la <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>d’entrée « ShareName ».  
  
7.  Créer un autre <xref:System.Printing.IndexedProperties.PrintStringProperty> de l’objet et définissez son <xref:System.Printing.IndexedProperties.PrintProperty.Name%2A> à « Location » et ses <xref:System.Printing.IndexedProperties.PrintStringProperty.Value%2A> un appropriés <xref:System.String>.  
  
8.  Utilisez la deuxième <xref:System.Printing.IndexedProperties.PrintStringProperty> objet à la valeur de la <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>d’entrée de « Location ».  
  
9. Créer un tableau de <xref:System.String>s. Chaque élément est le nom d’un port sur le serveur.  
  
10. Utilisez <xref:System.Printing.PrintServer.InstallPrintQueue%2A> pour installer la nouvelle imprimante avec les nouvelles valeurs.  
  
 Il est un exemple ci-dessous.  
  
 [!code-csharp[ClonePrinter#ClonePrinter](~/samples/snippets/csharp/VS_Snippets_Wpf/ClonePrinter/CSharp/Program.cs#cloneprinter)]
 [!code-vb[ClonePrinter#ClonePrinter](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ClonePrinter/visualbasic/program.vb#cloneprinter)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Printing.IndexedProperties>
- <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>
- <xref:System.Printing.LocalPrintServer>
- <xref:System.Printing.PrintQueue>
- <xref:System.Collections.DictionaryEntry>
- [Documents dans WPF](documents-in-wpf.md)
- [Vue d'ensemble de l'impression](printing-overview.md)
