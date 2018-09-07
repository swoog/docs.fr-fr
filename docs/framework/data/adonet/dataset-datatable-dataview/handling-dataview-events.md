---
title: Gestion des événements de DataView
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e5675663-fc91-4e0d-87a9-481b25b64c0f
ms.openlocfilehash: 2f30a578c5233e8b86a165dd220efd45348c5042
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44088009"
---
# <a name="handling-dataview-events"></a>Gestion des événements de DataView
Vous pouvez utiliser l'événement <xref:System.Data.DataView.ListChanged> du <xref:System.Data.DataView> pour déterminer si une vue a été mise à jour. Les mises à jour qui déclenchent l'événement incluent l'ajout, la suppression ou la modification d'une ligne dans la table sous-jacente, l'ajout ou la suppression d'une colonne dans le schéma de la table sous-jacente et une modification d'une relation parente ou enfant. Le **ListChanged** événement vous avertit aussi si la liste des lignes que vous affichez a changé de manière significative en raison de l’application d’un nouvel ordre de tri ou un filtre.  
  
 Le **ListChanged** événement implémente le **ListChangedEventHandler** délégué de la <xref:System.ComponentModel> espace de noms et accepte comme entrée un <xref:System.ComponentModel.ListChangedEventArgs> objet. Vous pouvez déterminer quel type de modification s’est produite à l’aide de la <xref:System.ComponentModel.ListChangedType> valeur d’énumération dans le **ListChangedType** propriété de la **ListChangedEventArgs** objet. Pour les modifications qui impliquent l’ajout, suppression ou déplacement de lignes, le nouvel index de la ligne ajoutée ou déplacée et l’index précédent de la ligne supprimée sont accessibles à l’aide de la **NewIndex** propriété de la **ListChangedEventArgs** objet. Dans le cas d’une ligne déplacée, l’index précédent de la ligne déplacée est accessible à l’aide de la **OldIndex** propriété de la **ListChangedEventArgs** objet.  
  
 Le **DataViewManager** expose également une **ListChanged** événement pour vous avertir lorsqu’une table a été ajoutée ou supprimée, ou si une modification a été apportée à la **Relations** collection de la sous-jacent **DataSet**.  
  
 L’exemple de code suivant montre comment ajouter un **ListChanged** Gestionnaire d’événements.  
  
```vb  
AddHandler custView.ListChanged, _  
  New System.ComponentModel.ListChangedEventHandler( _  
  AddressOf OnListChanged)  
  
Private Shared Sub OnListChanged( _  
  sender As Object, args As System.ComponentModel.ListChangedEventArgs)  
  Console.WriteLine("ListChanged:")  
  Console.WriteLine(vbTab & "    Type = " & _  
    System.Enum.GetName(args.ListChangedType.GetType(), _  
    args.ListChangedType))  
  Console.WriteLine(vbTab & "OldIndex = " & args.OldIndex)  
  Console.WriteLine(vbTab & "NewIndex = " & args.NewIndex)  
End Sub  
```  
  
```csharp  
custView.ListChanged  += new   
  System.ComponentModel.ListChangedEventHandler(OnListChanged);  
  
protected static void OnListChanged(object sender,   
  System.ComponentModel.ListChangedEventArgs args)  
{  
  Console.WriteLine("ListChanged:");  
  Console.WriteLine("\t    Type = " + args.ListChangedType);  
  Console.WriteLine("\tOldIndex = " + args.OldIndex);  
  Console.WriteLine("\tNewIndex = " + args.NewIndex);  
}  
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Data.DataView>  
 <xref:System.ComponentModel.ListChangedEventHandler>  
 [DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/dataviews.md)  
 [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
