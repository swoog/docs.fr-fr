---
title: AsymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: 7bd3b6be-8f77-4927-93ae-6fa371893cca
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 09bfaa3ab4f2aceb3e80644953a87686fca9830c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="asymmetricsecuritybindingelement"></a>AsymmetricSecurityBindingElement
AsymmetricSecurityBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```  
class AsymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe AsymmetricSecurityBindingElement ne définit pas de méthodes.  
  
## <a name="properties"></a>Propriétés  
 La classe AsymmetricSecurityBindingElement a les propriétés suivantes :  
  
### <a name="messageprotectionorder"></a>MessageProtectionOrder  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Ordre de chiffrement et de signature des messages de cette liaison.  
  
### <a name="requiresignatureconfirmation"></a>RequireSignatureConfirmation  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Si la liaison requiert la confirmation de signature.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
