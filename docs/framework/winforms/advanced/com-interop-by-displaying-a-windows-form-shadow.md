---
title: 'Procédure : prendre en charge COM Interop en affichant un formulaire Windows avec la méthode ShowDialog'
ms.date: 03/30/2017
helpviewer_keywords:
- COM [Windows Forms]
- Windows Forms, unmanaged
- COM interop [Windows Forms], calling methods
- ActiveX controls [Windows Forms], COM interop
- Windows Forms, interop
ms.assetid: 87aac8ad-3c04-43b3-9b0c-d0b00df9ee74
ms.openlocfilehash: 81220ad4c0bf00a38abfe7257d5fc61e92e8d885
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59206445"
---
# <a name="how-to-support-com-interop-by-displaying-a-windows-form-with-the-showdialog-method"></a>Procédure : prendre en charge COM Interop en affichant un formulaire Windows avec la méthode ShowDialog
Vous pouvez résoudre les problèmes d’interopérabilité COM en affichant votre formulaire Windows sur une boucle de message [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] , qui est créée en utilisant la méthode <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType> .  
  
 Pour qu’un formulaire fonctionne correctement à partir d’une application cliente COM, vous devez l’exécuter sur une boucle de messages Windows Forms. Pour cela, utilisez l'une des approches suivantes :  
  
-   Utilisez la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> pour afficher le formulaire Windows.  
  
-   Affichez chaque Windows Form sur un thread séparé. Pour plus d'informations, voir [Procédure : Prise en charge COM Interop en affichant chaque formulaire Windows sur son propre Thread](how-to-support-com-interop-by-displaying-each-windows-form-on-its-own-thread.md).  
  
## <a name="procedure"></a>Procédure  
 L’utilisation de la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> peut être le moyen le plus simple pour afficher un formulaire sur une boucle de messages [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] car, de toutes les approches, c’est elle qui nécessite le moins de code à implémenter.  
  
 La méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> interrompt la boucle de messages de l’application non managée et affiche le formulaire comme une boîte de dialogue. Comme la boucle de messages de l’application hôte a été interrompue, la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> crée une nouvelle boucle de messages [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] pour traiter les messages du formulaire.  
  
 L’inconvénient de l’utilisation de la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> est que le formulaire est ouvert comme boîte de dialogue modale. Ce comportement bloque toute interface utilisateur dans l’application appelante tant que le formulaire Windows est ouvert. Quand l’utilisateur quitte le formulaire, la boucle de messages [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] ferme la boucle et la boucle de messages antérieure de l’application reprend son exécution.  
  
 Vous pouvez créer une bibliothèque de classes dans Windows Forms qui a une méthode pour afficher le formulaire, puis créer la bibliothèque de classes pour COM interop. Vous pouvez utiliser ce fichier DLL depuis Visual Basic 6.0 ou Microsoft Foundation Classes (MFC) et, depuis ces deux environnements, vous pouvez appeler la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> pour afficher le formulaire.  
  
#### <a name="to-support-com-interop-by-displaying-a-windows-form-with-the-showdialog-method"></a>Pour prendre en charge COM Interop en affichant un formulaire Windows avec la méthode ShowDialog  
  
-   Remplacez tous les appels à la méthode <xref:System.Windows.Forms.Form.Show%2A?displayProperty=nameWithType> par des appels à la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> dans votre composant [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] .  
  
## <a name="see-also"></a>Voir aussi

- [Exposition de composants .NET Framework à COM](../../interop/exposing-dotnet-components-to-com.md)
- [Procédure : prendre en charge COM Interop en affichant chaque formulaire Windows sur son propre thread](how-to-support-com-interop-by-displaying-each-windows-form-on-its-own-thread.md)
- [Applications Windows Forms et non managées](windows-forms-and-unmanaged-applications.md)
