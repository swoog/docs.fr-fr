---
title: Considérations sur l'hébergement d'un contrôle ActiveX dans un Windows Form
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, ActiveX controls
- ActiveX controls [Windows Forms], hosting
- Windows Forms, ActiveX controls
- Windows Forms, hosting ActiveX controls
- ActiveX controls [Windows Forms], adding
ms.assetid: 2509302d-a74e-484f-9890-2acdbfa67a68
ms.openlocfilehash: babae31a3be9775d07ca84c54e1177d297cab5cf
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59108756"
---
# <a name="considerations-when-hosting-an-activex-control-on-a-windows-form"></a>Considérations sur l'hébergement d'un contrôle ActiveX dans un Windows Form
Bien que les Windows Forms aient été optimisés pour héberger des contrôles Windows Forms, vous pouvez néanmoins utiliser des contrôles ActiveX. Gardez à l’esprit les considérations suivantes lors de la planification d’une application qui utilise des contrôles ActiveX :  
  
-   **Sécurité** : le common language runtime a été amélioré en ce qui concerne la sécurité d’accès du code. Les applications recourant aux Windows Forms peuvent fonctionner sans problème dans un environnement totalement fiable et dans un environnement partiellement fiable avec la plupart des fonctionnalités disponibles. Les contrôles Windows Forms peuvent être hébergés dans un navigateur sans aucune complication. Cependant, les contrôles ActiveX dans les Windows Forms ne tirent pas parti de ces améliorations de sécurité. Exécution d’un contrôle ActiveX nécessite une autorisation de code non managé, qui est définie avec la <xref:System.Security.Permissions.SecurityPermissionAttribute.UnmanagedCode%2A?displayProperty=nameWithType> propriété. Pour plus d’informations sur la sécurité et d’autorisation de code non managé, consultez <xref:System.Security.Permissions.SecurityPermissionAttribute>.  
  
-   **Coût total de possession** : les contrôles ActiveX ajoutés à un Windows Form sont déployés dans leur intégralité avec ce Windows Form, ce qui peut accroître considérablement la taille des fichiers créés. En outre, l’utilisation de contrôles ActiveX sur des Windows Forms nécessite l’écriture dans le Registre. Ceci est plus invasif sur l’ordinateur d’un utilisateur que les contrôles Windows Forms, qui ne le nécessitent pas.  
  
    > [!NOTE]
    >  L’utilisation d’un contrôle ActiveX nécessite l’utilisation d’un wrapper COM interop. Pour plus d’informations, consultez [Interopérabilité COM en Visual Basic et Visual C#](~/docs/visual-basic/programming-guide/com-interop/com-interoperability-in-net-framework-applications.md).  
  
    > [!NOTE]
    >  Si le nom d’un membre du contrôle ActiveX correspond à un nom défini dans le [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)], l’importateur de contrôles ActiveX fera précéder le nom du membre avec **Ctl** lorsqu’il crée le <xref:System.Windows.Forms.AxHost> classe dérivée. Par exemple, si votre contrôle ActiveX a un membre nommé **Layout**, il est renommé **CtlLayout** dans la classe dérivée de AxHost, car l’événement **Layout** est défini dans le [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)].  
  
## <a name="see-also"></a>Voir aussi

- [Procédure : ajouter des contrôles ActiveX à des Windows Forms](how-to-add-activex-controls-to-windows-forms.md)
- [Sécurité d'accès du code](../../misc/code-access-security.md)
- [Comparaison des contrôles et des objets programmables dans divers langages et bibliothèques](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/0061wezk(v=vs.100))
- [Placement de contrôles dans les Windows Forms](putting-controls-on-windows-forms.md)
- [contrôles Windows Forms](index.md)
