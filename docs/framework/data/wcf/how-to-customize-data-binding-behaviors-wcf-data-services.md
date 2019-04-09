---
title: 'Procédure : Personnaliser les comportements (WCF Data Services) de liaison de données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, customizing
- WCF Data Services, data binding
ms.assetid: 40476b89-8941-4771-8d21-2fe430c85a9d
ms.openlocfilehash: e00f46dfd9b2d1446f2c2a1ba1fdd2e5b0405c1b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59111007"
---
# <a name="how-to-customize-data-binding-behaviors-wcf-data-services"></a>Procédure : Personnaliser les comportements (WCF Data Services) de liaison de données
Avec [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)], vous pouvez fournir une logique personnalisée appelée par <xref:System.Data.Services.Client.DataServiceCollection%601> lorsqu’un objet est ajouté ou supprimé de la collection de liaisons ou lorsqu’une modification de propriété est détectée. Cette logique personnalisée est fournie en tant que méthodes, référencées sous la forme <xref:System.Func%602> les délégués qui retournent une valeur de `false` lorsque le comportement par défaut doit toujours être effectué lorsque la méthode personnalisée est terminée et `true` quand d’autres le traitement de la événement doit être arrêté.  
  
 Les exemples dans cette rubrique fournissent des méthodes personnalisées pour les paramètres `entityChanged` et `entityCollectionChanged` de <xref:System.Data.Services.Client.DataServiceCollection%601>. Les exemples dans cette rubrique utilisent l'exemple de service de données Northwind et des classes de service de données client générées automatiquement. Ce service et les classes de données client sont créés lorsque vous complétez le [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).  
  
## <a name="example"></a>Exemple  
 La page code-behind suivante du fichier XAML crée une <xref:System.Data.Services.Client.DataServiceCollection%601> avec des méthodes personnalisées appelées lorsque des modifications sont apportées aux données liées à la collection de liaisons. Lorsque l’événement <xref:System.Collections.ObjectModel.ObservableCollection%601.CollectionChanged> se produit, la méthode fournie empêche un élément ayant été supprimé de la collection de liaisons d’être supprimé du service de données. Lorsque l'événement <xref:System.Collections.ObjectModel.ObservableCollection%601.PropertyChanged> se produit, la valeur `ShipDate` est validée pour vérifier que les modifications ne sont pas apportées aux ordres déjà livrés.  
  
 [!code-csharp[Astoria Northwind Client#WpfDataBindingCustom](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind client/cs/customerorderscustom.xaml.cs#wpfdatabindingcustom)]
 [!code-vb[Astoria Northwind Client#WpfDataBindingCustom](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind client/vb/customerorderscustom.xaml.vb#wpfdatabindingcustom)]
 [!code-vb[Astoria Northwind Client#WpfDataBindingCustom](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind client/vb/customerorderscustom2.xaml.vb#wpfdatabindingcustom)]  
  
## <a name="example"></a>Exemple  
 Le code XAML suivant définit la fenêtre de l'exemple précédent.  
  
 [!code-xaml[Astoria Northwind Client#WpfDataBindingCustomXaml](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind client/vb/customerorderscustom.xaml#wpfdatabindingcustomxaml)]  
  
## <a name="see-also"></a>Voir aussi

- [Bibliothèque client services de données WCF](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)
