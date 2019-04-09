---
title: 'Procédure : Personnaliser les flux avec le fournisseur Entity Framework (WCF Data Services)'
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, customizing
- WCF Data Services, customizing feeds
ms.assetid: fd16272e-36f2-415e-850e-8a81f2b17525
ms.openlocfilehash: 186b921f508b1a4b05e766c4f1a3c9e65de04722
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59089287"
---
# <a name="how-to-customize-feeds-with-the-entity-framework-provider-wcf-data-services"></a>Procédure : Personnaliser les flux avec le fournisseur Entity Framework (WCF Data Services)
[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] vous permet de personnaliser la sérialisation Atom dans une réponse de service de données afin que les propriétés d’une entité puissent être mappées aux éléments inutilisés définis dans le protocole AtomPub. Cette rubrique montre comment définir des attributs de mappage pour les types d’entité dans un modèle de données défini dans un fichier .edmx à l’aide du fournisseur Entity Framework. Pour plus d’informations, consultez [personnalisation de flux](../../../../docs/framework/data/wcf/feed-customization-wcf-data-services.md).  
  
 Dans cette rubrique vous modifierez manuellement le fichier .edmx généré par un outil qui contient le modèle de données. Vous devez modifier manuellement le fichier car les extensions vers le modèle de données ne sont pas prises en charge par le Concepteur d'entités. Pour plus d’informations sur le fichier .edmx qui génèrent les outils Entity Data Model, consultez [présentation (Entity Framework) d’un fichier .edmx](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100)). L'exemple dans cette rubrique utilise l'exemple de service de données Northwind et des classes de service de données clientes générées automatiquement. Ce service et les classes de données client sont créés lorsque vous complétez le [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).  
  
### <a name="to-manually-modify-the-northwindedmx-file-to-add-feed-customization-attributes"></a>Pour modifier manuellement le fichier Northwind.edmx pour ajouter des attributs de personnalisation de flux  
  
1.  Dans **l’Explorateur de solutions**, avec le bouton droit le `Northwind.edmx` de fichiers, puis cliquez sur **ouvrir avec**.  
  
2.  Dans le **ouvrir avec - Northwind.edmx** boîte de dialogue, sélectionnez **éditeur XML**, puis cliquez sur **OK**.  
  
3.  Localisez l'élément `ConceptualModels` et remplacez le type d'entité `Customers` existant par l'élément suivant qui contient des attributs de mappage de personnalisation de flux :  
  
     [!code-xml[Astoria Custom Feeds#EdmFeedCustomers](../../../../samples/snippets/xml/VS_Snippets_Misc/astoria custom feeds/xml/northwind.csdl#edmfeedcustomers)]  
  
4.  Enregistrez les modifications et fermez le fichier Northwind.edmx.  
  
5.  (Facultatif) Cliquez sur le fichier Northwind.edmx, puis cliquez sur **exécuter un outil personnalisé**.  
  
     Cette opération régénère le fichier de couche objet qui peut être obligatoire.  
  
6.  Recompilez le projet.  
  
## <a name="example"></a>Exemple  
 L'exemple précédent retourne le résultat suivant pour l'URI `http://myservice/Northwind.svc/Customers('ALFKI')`.  
  
 [!code-xml[Astoria Custom Feeds#EdmFeedResult](../../../../samples/snippets/xml/VS_Snippets_Misc/astoria custom feeds/xml/edmfeedresult.xml#edmfeedresult)]  
  
## <a name="see-also"></a>Voir aussi

- [Fournisseur Entity Framework](../../../../docs/framework/data/wcf/entity-framework-provider-wcf-data-services.md)
