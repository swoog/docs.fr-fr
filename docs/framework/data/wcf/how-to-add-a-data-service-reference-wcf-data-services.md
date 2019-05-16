---
title: 'Procédure : Ajouter une référence de Service de données (WCF Data Services)'
ms.date: 08/24/2018
helpviewer_keywords:
- WCF Data Services, configuring
ms.assetid: 62c6f318-3ee1-433a-b7a3-efa234c3034c
ms.openlocfilehash: 8bf623ec74c3bd165f63f60e883bfcb532d6900b
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65633956"
---
# <a name="how-to-add-a-data-service-reference-wcf-data-services"></a>Procédure : Ajouter une référence de service de données (WCF Data Services)

Vous pouvez utiliser la **ajouter une référence de Service** boîte de dialogue dans Visual Studio pour ajouter une référence à WCF Data Services. De cette manière, vous pouvez accéder plus facilement à un service de données dans une application cliente que vous développez dans Visual Studio. Lorsque vous complétez cette procédure, les classes de données sont générées selon les métadonnées obtenues auprès du service de données. Pour plus d’informations, consultez [génération de la bibliothèque de Client de Service de données](../../../../docs/framework/data/wcf/generating-the-data-service-client-library-wcf-data-services.md).

## <a name="add-a-data-service-reference"></a>Ajouter une référence de service de données

1. (Facultatif) Si le service de données n'appartient pas à la solution et n'est pas déjà en cours d'exécution, démarrez le service de données et notez l'URI du service de données.

2. Dans Visual Studio, dans **l’Explorateur de solutions**, cliquez sur le projet client, puis sélectionnez **ajouter** > **une référence de Service**.

3. Si le service de données fait partie de la solution actuelle, cliquez sur **Discover**.

     ou

     Dans le **adresse** zone de texte, tapez l’URL de base du service de données, telles que `http://localhost:1234/Northwind.svc`, puis cliquez sur **accédez**.

4. Sélectionnez **OK**.

     Un nouveau fichier de code qui contient les classes de données qui peuvent accéder et interagir avec les ressources de service de données est ajouté au projet.

## <a name="see-also"></a>Voir aussi

- [Démarrage rapide](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md)
