---
title: Applications multicouches LINQ to SQL avec ASP.NET
ms.date: 03/30/2017
ms.assetid: f6cc863a-d6a6-4281-ba8b-197c01cf6c6f
ms.openlocfilehash: 85ead36d1d927084c11dca1bd73a192b16e4ab7b
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65880756"
---
# <a name="linq-to-sql-n-tier-with-aspnet"></a>Applications multicouches LINQ to SQL avec ASP.NET
Dans les applications ASP.NET qui utilisent [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], vous utilisez le <xref:System.Web.UI.WebControls.LinqDataSource> contrôle serveur Web. Ce contrôle gère la plus grande part de la logique dont il doit disposer pour exécuter des requêtes sur [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], passer les données au navigateur, les récupérer et les soumettre à [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.DataContext> qui met ensuite à jour la base de données. Vous configurez simplement le contrôle dans le balisage et le contrôle gère tous les transferts de données entre [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] et le navigateur. Étant donné que le contrôle gère les interactions avec la couche de présentation et [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] gère la communication avec la couche de données, votre principal objectif dans les applications ASP.NET à plusieurs niveaux est sur l’écriture de votre logique métier personnalisée.  
  
 Pour plus d’informations sur `LINQDataSource`, consultez [vue d’ensemble du contrôle serveur Web LinqDataSource](https://docs.microsoft.com/previous-versions/aspnet/bb547113(v=vs.100)).  
  
## <a name="see-also"></a>Voir aussi

- [Applications multicouches et distantes avec LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/n-tier-and-remote-applications-with-linq-to-sql.md)
