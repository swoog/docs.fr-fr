---
title: 'Comment : partager un Assembly avec d’autres Applications (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: 5388aedc-cb42-4622-8b70-8e701eee057a
ms.openlocfilehash: 3d29a3558a64c02fc8c59035f2fee5c64c4a776f
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48025453"
---
# <a name="how-to-share-an-assembly-with-other-applications-visual-basic"></a>Comment : partager un Assembly avec d’autres Applications (Visual Basic)
Les assemblys peuvent être privés ou partagés. Par défaut, la plupart des programmes simples se composent d’un assembly privé, car ils ne sont pas destinés à être utilisés par d’autres applications.  
  
 Pour partager un assembly avec d’autres applications, celui-ci doit être placé dans le [Global Assembly Cache](../../../../framework/app-domains/gac.md) (GAC).  
  
### <a name="sharing-an-assembly"></a>Partage d’un assembly  
  
1.  Créez votre assembly. Pour plus d’informations, consultez [Création d’assemblys](../../../../framework/app-domains/create-assemblies.md).  
  
2.  Attribuez un nom fort à votre assembly. Pour plus d’informations, consultez [Guide pratique pour signer un assembly avec un nom fort](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).  
  
3.  Assignez des informations de version à votre assembly. Pour plus d’informations, consultez [Versioning des assemblys](../../../../framework/app-domains/assembly-versioning.md).  
  
4.  Ajoutez votre assembly au Global Assembly Cache. Pour plus d’informations, consultez [Guide pratique pour installer un assembly dans le Global Assembly Cache](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md).  
  
5.  Accédez aux types contenus dans l’assembly à partir d’autres applications. Pour plus d’informations, consultez [Guide pratique pour référencer un assembly avec un nom fort](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md).  
  
## <a name="see-also"></a>Voir aussi

- [Concepts de programmation](../../../../visual-basic/programming-guide/concepts/index.md)
- [Assemblys et le Global Assembly Cache (Visual Basic)](../../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)  
- [Programmation à l’aide d’assemblys](../../../../framework/app-domains/programming-with-assemblies.md)
