---
title: Créer un projet LINQ to DataSet dans Visual Studio
ms.date: 08/15/2018
ms.assetid: 49ba6cb0-cdd2-4571-aeaa-25bf0f40e9b3
ms.openlocfilehash: 22763d3b9581d09d7bdda0c09480f8d36bb8e2ec
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53154032"
---
# <a name="how-to-create-a-linq-to-dataset-project-in-visual-studio"></a>Procédure : Créer un projet LINQ to DataSet dans Visual Studio

Les différents types de projets LINQ nécessitent certains espaces de noms importés (Visual Basic) et les références d’assembly ou [à l’aide de](../../../csharp/language-reference/keywords/using-directive.md) directives (c#). La configuration minimale requise pour LINQ est une référence à *System.Core.dll* et un `using` directive pour <xref:System.Linq>.

Ces exigences sont fournis par défaut si vous créez un projet d’application de console c# dans Visual Studio 2017. Si vous mettez à niveau un projet à partir d’une version antérieure de Visual Studio, vous devrez peut-être fournir manuellement ces références liées à LINQ.

LINQ to DataSet nécessite deux références supplémentaires à *System.Data.dll* et *System.Data.DataSetExtensions.dll*.

> [!NOTE]
> Si vous générez à partir d’une invite de commandes, vous devez référencer manuellement les DLL liées à LINQ dans *%ProgramFiles%\Reference Assemblies\Microsoft\Framework\v3.5*.

## <a name="to-enable-linq-to-dataset-functionality"></a>Pour activer les fonctionnalités LINQ to DataSet

Suivez ces étapes pour activer LINQ aux fonctionnalités de jeu de données dans un projet existant.

1. Ajouter des références aux **System.Core**, **System.Data**, et **System.Data.DataSetExtensions**.

   Dans **l’Explorateur de solutions**, avec le bouton droit sur le **références** nœud et sélectionnez **ajouter une référence**. Dans le **Gestionnaire de références** boîte de dialogue, sélectionnez **System.Core**, **System.Data**, et **System.Data.DataSetExtensions**. Sélectionnez **OK**.

1. Ajouter [à l’aide de](../../../csharp/language-reference/keywords/using-directive.md) directives (ou [instructions Imports](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) en Visual Basic) pour **System.Data** et **System.Linq**.

   ```csharp
   using System.Data;
   using System.Linq;
   ```

1. Si vous le souhaitez, ajoutez un `using` directive (ou `Imports` instruction) pour **System.Data.Common** ou **System.Data.SqlClient**, en fonction de comment vous connectez à la base de données.

## <a name="see-also"></a>Voir aussi

- [Bien démarrer avec LINQ to DataSet](../../../../docs/framework/data/adonet/getting-started-linq-to-dataset.md)
