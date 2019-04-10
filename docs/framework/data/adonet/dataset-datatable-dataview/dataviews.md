---
title: DataViews
ms.date: 03/30/2017
ms.assetid: 0fe5dfa2-c1cd-435f-90b6-b4dd2e3ef34b
ms.openlocfilehash: aff4d6f648fa091130bfd9951f2a5001947b09a1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59215909"
---
# <a name="dataviews"></a>DataViews
Un objet <xref:System.Data.DataView> vous permet de créer différentes vues des données stockées dans un objet <xref:System.Data.DataTable>, possibilité qui est souvent utilisée dans les applications de liaison de données. À l’aide un **DataView**, vous pouvez exposer les données dans une table avec différents ordres de tri, et vous pouvez filtrer les données par état de ligne ou en fonction d’une expression de filtre.  
  
 Un **DataView** fournit une vue dynamique des données dans sous-jacent **DataTable**: le contenu, classement et l’appartenance reflètent les modifications qu’ils se produisent. Ce comportement diffère la **sélectionnez** méthode de la **DataTable**, qui retourne un <xref:System.Data.DataRow> tableau à partir d’une table selon un ordre de filtre et/ou de tri particulier : ce contenu reflète les modifications apportées à la sous-jacent de table, mais son appartenance et l’ordre restent statiques. Les fonctionnalités dynamiques de la **DataView** rendent idéal pour les applications de liaison de données.  
  
 Un **DataView** vous offre une vue dynamique d’un ensemble unique de données, similaire à une vue de base de données, à laquelle vous pouvez appliquer différents de tri et de critères de filtrage. Contrairement à une vue de base de données, toutefois, un **DataView** ne peut pas être traité comme une table et ne peut pas fournir une vue de tables jointes. Vous ne pouvez pas non plus exclure des colonnes si elles existent dans la table source, ou ajouter des colonnes, telles que des colonnes de calcul qui n'existent pas dans la table source.  
  
 Vous pouvez utiliser un <xref:System.Data.DataView.DataViewManager%2A> pour gérer les paramètres de vue pour toutes les tables dans un **DataSet**. Le **DataViewManager** vous offre un moyen pratique pour gérer les paramètres d’affichage par défaut pour chaque table. Lorsque vous liez un contrôle à plusieurs tables d’un **DataSet**, liaison avec un **DataViewManager** est le choix idéal.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Création d'un DataView](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/creating-a-dataview.md)  
 Décrit comment créer un **DataView** pour un **DataTable**.  
  
 [Tri et filtre de données](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/sorting-and-filtering-data.md)  
 Décrit comment définir les propriétés d’un **DataView** pour retourner des sous-ensembles de lignes de données de critères de filtre spécifiques de réunion, ou pour retourner des données dans un ordre de tri particulier.  
  
 [DataRows et DataRowViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datarows-and-datarowviews.md)  
 Décrit comment accéder aux données exposées par le **DataView**.  
  
 [Recherche de lignes](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/finding-rows.md)  
 Explique comment rechercher une ligne particulière dans un **DataView**.  
  
 [ChildView et relations](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/childviews-and-relations.md)  
 Décrit comment créer des vues de données à partir d’une relation parent-enfant à l’aide un **DataView**.  
  
 [Modification des DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/modifying-dataviews.md)  
 Décrit comment modifier les données sous-jacentes **DataTable** via la **DataView**, y compris l’activation ou désactivation des mises à jour.  
  
 [Gestion des événements de DataView](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/handling-dataview-events.md)  
 Décrit comment utiliser le **ListChanged** événement pour recevoir une notification lorsque le contenu ou l’ordre d’un **DataView** est en cours de mise à jour.  
  
 [Gestion des DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/managing-dataviews.md)  
 Décrit comment utiliser un **DataViewManager** pour gérer les **DataView** paramètres pour chaque table dans un **DataSet**.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Applications Web ASP.NET](https://docs.microsoft.com/previous-versions/655cec97(v=vs.100))  
 Propose des vues d'ensemble et des procédures détaillées qui vous aident, étape par étape, à créer des applications ASP.NET, des Web Forms et des services Web.  
  
 [Applications Windows](https://docs.microsoft.com/previous-versions/ms184421(v=vs.100))  
 Fournit des informations détaillées sur l'utilisation de Windows Forms et d'applications console.  
  
 [DataSets, DataTables et DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)  
 Décrit le **DataSet** objet et comment vous pouvez l’utiliser pour gérer les données d’application.  
  
 [DataTables](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatables.md)  
 Décrit le **DataTable** objet et comment vous pouvez l’utiliser pour gérer les données d’application autonome ou comme partie d’un **DataSet**.  
  
 [ADO.NET](../../../../../docs/framework/data/adonet/index.md)  
 Décrit l'architecture et les composants d'ADO.NET ainsi que la façon d'utiliser ADO.NET pour accéder à des sources de données existantes et gérer des données d'application.  
  
## <a name="see-also"></a>Voir aussi

- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
