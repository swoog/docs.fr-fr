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
ms.openlocfilehash: f2fb48e07243694b14904b240bdcb0739175c2fc
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65593527"
---
# <a name="how-to-support-com-interop-by-displaying-a-windows-form-with-the-showdialog-method"></a>Procédure : prendre en charge COM Interop en affichant un formulaire Windows avec la méthode ShowDialog
Vous pouvez résoudre les problèmes d’interopérabilité de composant COM (Object Model) en affichant votre formulaire Windows sur une boucle de messages de .NET Framework, qui est créée à l’aide de la <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType> (méthode).  
  
 Pour qu’un formulaire fonctionne correctement à partir d’une application cliente COM, vous devez l’exécuter sur une boucle de messages Windows Forms. Pour cela, utilisez l'une des approches suivantes :  
  
- Utilisez la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> pour afficher le formulaire Windows.  
  
- Affichez chaque Windows Form sur un thread séparé. Pour plus d'informations, voir [Procédure : Prise en charge COM Interop en affichant chaque formulaire Windows sur son propre Thread](how-to-support-com-interop-by-displaying-each-windows-form-on-its-own-thread.md).  
  
## <a name="procedure"></a>Procédure  
 À l’aide de la <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> méthode peut être le moyen le plus simple pour afficher un formulaire sur une boucle de message de .NET Framework, car, de toutes les approches, elle nécessite le moins de code à implémenter.  
  
 La méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> interrompt la boucle de messages de l’application non managée et affiche le formulaire comme une boîte de dialogue. Étant donné que la boucle de message de l’application hôte a été interrompue, le <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> méthode crée une nouvelle boucle de message de .NET Framework pour traiter les messages du formulaire.  
  
 L’inconvénient de l’utilisation de la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> est que le formulaire est ouvert comme boîte de dialogue modale. Ce comportement bloque toute interface utilisateur dans l’application appelante tant que le formulaire Windows est ouvert. Lorsque l’utilisateur quitte le formulaire, la boucle de message de .NET Framework se ferme et boucle de messages antérieure de l’application commence à s’exécuter à nouveau.  
  
 Vous pouvez créer une bibliothèque de classes dans Windows Forms qui a une méthode pour afficher le formulaire, puis créer la bibliothèque de classes pour COM interop. Vous pouvez utiliser ce fichier DLL depuis Visual Basic 6.0 ou Microsoft Foundation Classes (MFC) et, depuis ces deux environnements, vous pouvez appeler la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> pour afficher le formulaire.  
  
#### <a name="to-support-com-interop-by-displaying-a-windows-form-with-the-showdialog-method"></a>Pour prendre en charge COM Interop en affichant un formulaire Windows avec la méthode ShowDialog  
  
- Remplacez tous les appels à la <xref:System.Windows.Forms.Form.Show%2A?displayProperty=nameWithType> méthode avec les appels à la <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> méthode dans votre composant .NET Framework.  
  
## <a name="see-also"></a>Voir aussi

- [Exposition de composants .NET Framework à COM](../../interop/exposing-dotnet-components-to-com.md)
- [Guide pratique pour Prennent en charge COM Interop en affichant chaque formulaire Windows sur son propre Thread](how-to-support-com-interop-by-displaying-each-windows-form-on-its-own-thread.md)
- [Applications Windows Forms et non managées](windows-forms-and-unmanaged-applications.md)
