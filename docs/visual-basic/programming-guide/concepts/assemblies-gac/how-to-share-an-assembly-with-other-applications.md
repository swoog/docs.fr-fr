---
title: 'Procédure : Partager un Assembly avec d’autres Applications (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: 5388aedc-cb42-4622-8b70-8e701eee057a
ms.openlocfilehash: d0e1dafc700b55a63342331b3280337d2c93cbd1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631826"
---
# <a name="how-to-share-an-assembly-with-other-applications-visual-basic"></a>Procédure : Partager un Assembly avec d’autres Applications (Visual Basic)
Les assemblys peuvent être privés ou partagés. Par défaut, la plupart des programmes simples se composent d’un assembly privé, car ils ne sont pas destinés à être utilisés par d’autres applications.  
  
 Pour partager un assembly avec d’autres applications, celui-ci doit être placé dans le [Global Assembly Cache](../../../../framework/app-domains/gac.md) (GAC).  
  
### <a name="sharing-an-assembly"></a>Partage d’un assembly  
  
1.  Créez votre assembly. Pour plus d’informations, consultez [Création d’assemblys](../../../../framework/app-domains/create-assemblies.md).  
  
2.  Attribuez un nom fort à votre assembly. Pour plus d'informations, voir [Procédure : signer un assembly avec un nom fort](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).  
  
3.  Assignez des informations de version à votre assembly. Pour plus d’informations, consultez [Versioning des assemblys](../../../../framework/app-domains/assembly-versioning.md).  
  
4.  Ajoutez votre assembly au Global Assembly Cache. Pour plus d'informations, voir [Procédure : Installer un Assembly dans le Global Assembly Cache](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md).  
  
5.  Accédez aux types contenus dans l’assembly à partir d’autres applications. Pour plus d'informations, voir [Procédure : Référencer un Assembly avec nom fort](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md).  
  
## <a name="see-also"></a>Voir aussi

- [Concepts de programmation](../../../../visual-basic/programming-guide/concepts/index.md)
- [Assemblys et le Global Assembly Cache (Visual Basic)](../../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)
- [Programmation à l’aide d’assemblys](../../../../framework/app-domains/programming-with-assemblies.md)
