---
title: Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor
ms.date: 03/30/2017
ms.topic: reference
api_name:
- Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor
api_location:
- Microsoft.VisualStudio.Activities.dll
api_type:
- Assembly
ms.assetid: 6b44b13c-7a23-4df2-8f9f-45e2b1430002
ms.openlocfilehash: b44b20a83068278fb35345220f45051a7c4177f2
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57498703"
---
# <a name="microsoftvisualstudioactivitiesasrclientactivitybuilderctor"></a>Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor
Crée une instance de la [Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/microsoft-visualstudio-activities-asr-clientactivitybuilder.md) classe.  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp  
public ClientActivityBuilder(OperationDescription operationDescription, string configurationName, string proxyNamespace);  
```  
  
## <a name="parameters"></a>Paramètres  
  
## <a name="parameter-values"></a>Valeurs du paramètre  
 *operationDescription*  
  
 Décrit l'opération à effectuer dans l'activité de workflow qui doit être générée, notamment le nom de l'opération, le type de retour et les informations de paramètre. La valeur de ce paramètre ne doit pas être **null**. Elle doit décrire une opération synchrone qui utilise un contrat de message et prend un argument avec un message. Si ces conditions ne sont pas satisfaites, le résultat d'exécution du constructeur et des autres méthodes de cette classe est indéfini.  
  
 *configurationName*  
  
 Spécifie le nom de configuration du point de terminaison. La valeur de ce paramètre ne doit pas être soit **null** ou vide. Si ces conditions ne sont pas satisfaites, le résultat d'exécution du constructeur et des autres méthodes de cette classe est indéfini.  
  
 *proxyNamespace*  
  
 Spécifie l'espace de noms du service pour l'opération. La valeur de ce paramètre ne doit pas être soit **null** ou vide. Si ces conditions ne sont pas satisfaites, le résultat d'exécution du constructeur et des autres méthodes de cette classe est indéfini.  
  
## <a name="see-also"></a>Voir aussi
- [Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/microsoft-visualstudio-activities-asr-clientactivitybuilder.md)
