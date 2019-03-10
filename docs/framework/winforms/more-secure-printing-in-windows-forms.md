---
title: Impression plus sécurisée dans les Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, printing
- PrintingPermission class [Windows Forms], Windows Forms security
- printing [Windows Forms], security
- security [Windows Forms], printing
ms.assetid: 48fd36ac-872f-4de0-902a-e52969cd4367
ms.openlocfilehash: 2fd61ea1c56ee2dbe7ff725d9f9f79df6b6cdfd8
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57723034"
---
# <a name="more-secure-printing-in-windows-forms"></a>Impression plus sécurisée dans les Windows Forms
Les applications Windows Forms incluent souvent des fonctionnalités d’impression. Le [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] utilise le <xref:System.Drawing.Printing.PrintingPermission> classe pour contrôler l’accès aux fonctionnalités d’impression et associé <xref:System.Drawing.Printing.PrintingPermissionLevel> valeur d’énumération pour indiquer le niveau d’accès. Par défaut, l’impression est activée par défaut dans les zones Intranet Local et Internet ; Toutefois, le niveau d’accès est limité dans les deux zones. Si votre application peut imprimer, nécessite une interaction utilisateur, ou ne peut pas imprimer dépend de la valeur de l’autorisation accordée à l’application. Par défaut, la zone Intranet locale reçoit <xref:System.Drawing.Printing.PrintingPermissionLevel.DefaultPrinting> accès et la zone Intranet reçoit <xref:System.Drawing.Printing.PrintingPermissionLevel.SafePrinting> accès.  
  
 Le tableau suivant présente les fonctionnalités disponibles à chaque niveau d’autorisation d’impression.  
  
|PrintingPermissionLevel|Description|  
|-----------------------------|-----------------|  
|<xref:System.Drawing.Printing.PrintingPermissionLevel.AllPrinting>|Fournit un accès complet à toutes les imprimantes installées.|  
|<xref:System.Drawing.Printing.PrintingPermissionLevel.DefaultPrinting>|Permet l’impression par programmation à l’imprimante par défaut et impression plus sécurisée via une boîte de dialogue d’impression restrictive. <xref:System.Drawing.Printing.PrintingPermissionLevel.DefaultPrinting> est un sous-ensemble de <xref:System.Drawing.Printing.PrintingPermissionLevel.AllPrinting>.|  
|<xref:System.Drawing.Printing.PrintingPermissionLevel.SafePrinting>|Fournit une impression uniquement à partir d’une boîte de dialogue plus restrictive. <xref:System.Drawing.Printing.PrintingPermissionLevel.SafePrinting> est un sous-ensemble de <xref:System.Drawing.Printing.PrintingPermissionLevel.DefaultPrinting>.|  
|<xref:System.Drawing.Printing.PrintingPermissionLevel.NoPrinting>|Empêche l’accès aux imprimantes. <xref:System.Drawing.Printing.PrintingPermissionLevel.NoPrinting> est un sous-ensemble de <xref:System.Drawing.Printing.PrintingPermissionLevel.SafePrinting>.|  
  
## <a name="see-also"></a>Voir aussi
- [Accès plus sécurisé aux fichiers et aux données dans les Windows Forms](more-secure-file-and-data-access-in-windows-forms.md)
- [Considérations supplémentaires sur la sécurité des Windows Forms](additional-security-considerations-in-windows-forms.md)
- [Vue d’ensemble de la sécurité dans les Windows Forms](security-in-windows-forms-overview.md)
- [Sécurité de Windows Forms](windows-forms-security.md)
