---
title: Option d'encodage d'instance
ms.date: 03/30/2017
ms.assetid: 89e4b029-4f68-438c-8117-9b21fe094ef4
ms.openlocfilehash: c4de7c45d899f45a7b5b71d563257d9accb8fdbb
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59315619"
---
# <a name="instance-encoding-option"></a>Option d'encodage d'instance
Le **Option d’encodage d’Instance** propriété du Store d’Instance de Workflow SQL vous permet de spécifier si le fournisseur de persistance SQL doit compresser les informations d’état du flux de travail d’instance à l’aide de l’algorithme GZip avant d’enregistrer le informations dans la base de données de persistance. Les valeurs autorisées pour cette propriété sont : GZip et aucun. La valeur par défaut est None. La liste suivante décrit ces trois options.  
  
1. **GZip**. Le fournisseur de persistance encode les informations d'état à l'aide de l'algorithme Gzip avant de rendre les informations d'état persistantes dans la base de données de persistance.  
  
2. **Aucun**. Le fournisseur de persistance n'encode pas les informations d'état avant d'enregistrer les informations dans la base de données de persistance.  
  
 L'encodage des informations de l'état de l'instance du workflow à l'aide du Gzip réduit la consommation de mémoire dans la base de données SQL ainsi que la consommation réseau si la base de données réside sur un autre ordinateur sur le réseau différent de l'ordinateur sur lequel l'hôte du service de workflow s'exécute. Une recommandation générale consiste à définir le **Option d’encodage d’Instance** propriété **aucun** si l’état d’instance de flux de travail est faible.
