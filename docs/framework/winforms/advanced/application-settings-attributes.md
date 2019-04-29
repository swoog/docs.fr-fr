---
title: Attributs des paramètres d'application
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], attributes
- attributes [Windows Forms], application settings
- wrapper classes [Windows Forms], application settings
ms.assetid: 53caa66c-a9fb-43a5-953c-ad092590098d
ms.openlocfilehash: f945d8e6918c271eeb5fdf3cf9c357b1c2bbca66
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61699725"
---
# <a name="application-settings-attributes"></a>Attributs des paramètres d'application
L’architecture de paramètres d’Application fournit beaucoup d’attributs qui peut être appliqués à la classe wrapper de paramètres des applications ou à ses propriétés individuelles. Ces attributs sont examinées au moment de l’exécution par l’infrastructure de paramètres d’application, souvent en particulier le fournisseur de paramètres, afin d’adapter son fonctionnement aux besoins énoncés du wrapper personnalisé.  
  
 Le tableau suivant répertorie les attributs qui peuvent être appliqués à la classe wrapper de paramètres application, les propriétés individuelles de cette classe ou les deux. Par définition, uniquement un attribut d’étendue unique —**UserScopedSettingAttribute** ou **ApplicationScopedSettingAttribute**— doit être appliqué à chaque propriété de paramètres.  
  
> [!NOTE]
>  Un fournisseur de paramètres personnalisés, dérivée de la <xref:System.Configuration.SettingsProvider> de classe, n’est nécessaire pour reconnaître les trois attributs suivants : **ApplicationScopedSettingAttribute**, **UserScopedSettingAttribute**, and **DefaultSettingValueAttribute**.  
  
|Attribut|une cible|Description|  
|---------------|------------|-----------------|  
|<xref:System.Configuration.SettingsProviderAttribute>|Les deux|Spécifie le nom court du fournisseur de paramètres à utiliser pour la persistance.<br /><br /> Si cet attribut n’est pas fourni, le fournisseur par défaut, <xref:System.Configuration.LocalFileSettingsProvider>, est supposé.|  
|<xref:System.Configuration.UserScopedSettingAttribute>|Les deux|Définit une propriété comme un paramètre d’application de portée utilisateur.|  
|<xref:System.Configuration.ApplicationScopedSettingAttribute>|Les deux|Définit une propriété comme paramètre d’application de portée application.|  
|<xref:System.Configuration.DefaultSettingValueAttribute>|Propriété|Spécifie une chaîne qui peut être désérialisée par le fournisseur dans la valeur par défaut codées en dur pour cette propriété.<br /><br /> Le <xref:System.Configuration.LocalFileSettingsProvider> ne nécessite pas de cet attribut et remplace toute valeur fournie par cet attribut s’il existe déjà une valeur persistante.|  
|<xref:System.Configuration.SettingsDescriptionAttribute>|Propriété|Fournit le test descriptif d’un paramètre spécifique, principalement utilisé par les outils d’exécution et au moment du design.|  
|<xref:System.Configuration.SettingsGroupNameAttribute>|Classe|Fournit un nom explicite pour un groupe de paramètres. Si cet attribut est absent, <xref:System.Configuration.ApplicationSettingsBase> utilise le nom de la classe wrapper.|  
|<xref:System.Configuration.SettingsGroupDescriptionAttribute>|Classe|Fournit le test descriptif d’un groupe de paramètres, principalement utilisé par les outils d’exécution et au moment du design.|  
|<xref:System.Configuration.SettingsManageabilityAttribute>|Les deux|Spécifie zéro ou plusieurs services de gestion qui doivent être fournies pour le groupe de paramètres ou la propriété. Les services disponibles sont décrits par le <xref:System.Configuration.SettingsManageability> énumération.|  
|<xref:System.Configuration.SpecialSettingAttribute>|Propriété|Indique qu’un paramètre appartient à une catégorie spécifique, prédéfinie, telle qu’une chaîne de connexion, ce qui suggère un traitement spécial par le fournisseur de paramètres. Les catégories prédéfinies pour cet attribut sont définies par le <xref:System.Configuration.SpecialSetting> énumération.|  
|<xref:System.Configuration.SettingsSerializeAsAttribute>|Les deux|Spécifie un mécanisme de sérialisation par défaut pour une propriété ou un groupe de paramètres. Les mécanismes de sérialisation disponibles sont définis par le <xref:System.Configuration.SettingsSerializeAs> énumération.|  
|<xref:System.Configuration.NoSettingsVersionUpgradeAttribute>|Propriété|Spécifie qu’un fournisseur de paramètres doit désactiver toutes les fonctionnalités de mise à niveau d’application pour la propriété marquée.|  
  
 *Classe* indique que l’attribut peut être appliqué uniquement à une classe wrapper de paramètres application. *Propriété* indique que l’attribut peut être appliqué uniquement aux propriétés de paramètres. *Les deux* indique que l’attribut peut être appliqué à tout niveau.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Configuration.ApplicationSettingsBase>
- <xref:System.Configuration.SettingsProvider>
- [Architecture des paramètres d'application](application-settings-architecture.md)
- [Guide pratique pour Créer des paramètres d’Application](how-to-create-application-settings.md)
