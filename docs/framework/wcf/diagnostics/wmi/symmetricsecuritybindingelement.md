---
title: SymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: b2e182b6-c041-4d80-a926-6058068d9f79
ms.openlocfilehash: 618899c80d1b22aaabc3c13fe1079137eaf10a93
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50182500"
---
# <a name="symmetricsecuritybindingelement"></a>SymmetricSecurityBindingElement
SymmetricSecurityBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class SymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe SymmetricSecurityBindingElement ne définit pas de méthodes.  
  
## <a name="properties"></a>Properties  
 La classe SymmetricSecurityBindingElement a les propriétés suivantes :  
  
### <a name="messageprotectionorder"></a>MessageProtectionOrder  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Ordre de chiffrement et de signature des messages de cette liaison.  
  
### <a name="requiresignatureconfirmation"></a>RequireSignatureConfirmation  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Si la liaison requiert la confirmation de signature.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
