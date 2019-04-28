---
title: Création d'un modèle de chiffrement
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- encryption [.NET Framework], creating cryptographic schemes
- cryptography [.NET Framework], creating cryptographic schemes
ms.assetid: d40c509f-5a5e-46cc-94cb-a951e9ab6843
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3ef3741ef5cec720c2fb285c9aa60d610acc0be9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61909387"
---
# <a name="creating-a-cryptographic-scheme"></a>Création d'un modèle de chiffrement
Les composants de chiffrement de .NET Framework peuvent être combinés pour créer différents modèles permettant de chiffrer et de déchiffrer des données.  
  
 Un simple modèle de chiffrement pour chiffrer et déchiffrer des données peut spécifier les étapes suivantes :  
  
1. Chaque partie génère une paire de clés publique/privée.  
  
2. Les parties échangent leurs clés publiques.  
  
3. Chaque partie génère une clé secrète pour le chiffrement TripleDES (par exemple), et chiffre la clé nouvellement créée à l'aide de la clé publique de l'autre.  
  
4. Chaque partie envoie les données à l'autre et combine la clé secrète de l'autre avec la sienne, dans un ordre spécifique, pour créer une clé secrète.  
  
5. Les parties lancent ensuite une conversation à l'aide du chiffrement symétrique.  
  
 La création d’un modèle de chiffrement n’est pas une tâche facile.
  
## <a name="see-also"></a>Voir aussi

- [Cryptographic Services](../../../docs/standard/security/cryptographic-services.md)
