---
title: 'Comment : exécuter une requête qui retourne les types complexes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: c2209fdb-70ef-4dea-8bb8-097fe96f5563
ms.openlocfilehash: 013f1980d2ea13927871719aeea293cfce38b4d5
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43861892"
---
# <a name="how-to-execute-a-query-that-returns-complex-types"></a>Comment : exécuter une requête qui retourne les types complexes
Cette rubrique indique comment exécuter une requête [!INCLUDE[esql](../../../../../includes/esql-md.md)] qui retourne des objets de type d'entité qui contiennent une propriété d'un type complexe.  
  
### <a name="to-run-the-code-in-this-example"></a>Pour exécuter le code de cet exemple  
  
1.  Ajouter le [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) à votre projet et configurez votre projet pour utiliser le [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]. Pour plus d’informations, consultez [Comment : utiliser l’Assistant Entity Data Model](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d).  
  
2.  Dans la page de codes de votre application, ajoutez les instructions `using` (`Imports` en Visual Basic) suivantes :  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
3.  Double-cliquez sur le fichier .edmx pour afficher le modèle dans le [fenêtre Explorateur de modèles](https://msdn.microsoft.com/library/94e836e8-a5ea-47ff-aa3e-599d8a02ebfd) du Concepteur d’entités. Sur la surface du Concepteur d’entités, sélectionnez le `Email` et `Phone` propriétés de la `Contact` type d’entité, puis avec le bouton droit et sélectionnez **refactoriser en nouveau Type complexe**.  
  
4.  Un nouveau type complexe avec le texte sélectionné `Email` et `Phone` propriétés est ajouté à la **Explorateur de modèles**. Le type complex est donné un nom par défaut : Renommez le type en `EmailPhone` dans le **propriétés** fenêtre. Une nouvelle propriété `ComplexProperty` est également ajoutée au type d'entité `Contact`. Renommez la propriété en `EmailPhoneComplexType.`.  
  
     Pour plus d’informations sur la création et modification des types complexes à l’aide de l’Assistant Entity Data Model, consultez [Comment : refactoriser des propriétés existantes en propriété de Type complexe](https://msdn.microsoft.com/library/5b2eb3b3-693d-42cb-b43a-405812d677eb) et [Comment : créer et modifier les Types complexes](https://msdn.microsoft.com/library/afb8e206-0ffe-4597-b6d4-6ab566897e1d).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant exécute une requête qui retourne une collection de `Contact` les objets et les affiche deux propriétés de la `Contact` objets : `ContactID` et les valeurs de la `EmailPhoneComplexType` type complexe.  
  
 [!code-csharp[DP EntityServices Concepts#ComplexTypeWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#complextypewithentitycommand)]
 [!code-vb[DP EntityServices Concepts#ComplexTypeWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#complextypewithentitycommand)]
