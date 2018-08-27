---
title: Procédures stockées CLR
ms.date: 03/30/2017
ms.assetid: fd7eea9b-218a-4988-8c9a-8abcc6031c66
ms.openlocfilehash: df323e2d1b50dcd1b2087141deefa1c86723b346
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42930110"
---
# <a name="clr-stored-procedures"></a>Procédures stockées CLR
Les procédures stockées sont des routines pouvant être utilisées dans les expressions scalaires. Elles peuvent retourner des résultats tabulaires et des messages au client, invoquer des instructions DDL (Data Definition Language) et DML (Data Manipulation Language) et retourner des paramètres de sortie.  
  
> [!NOTE]
>  Microsoft Visual Basic ne prend pas en charge les paramètres de sortie de la même manière que Microsoft Visual C#. Vous devez spécifier pour passer le paramètre par référence et appliquer le \<Out() > attribut pour représenter un paramètre de sortie, comme suit :  
  
```vb
Public Shared Sub ExecuteToClient( <Out()> ByRef number As Integer)  
```
  
Pour plus d’informations, consultez la version de [documentation de SQL Server](/sql) pour la version de SQL Server que vous utilisez.
  
 **Documentation de SQL Server**

1. [Procédures stockées CLR](http://go.microsoft.com/fwlink/?LinkId=115400)  
  
## <a name="see-also"></a>Voir aussi  
 [Création d’objets SQL Server 2005 dans le Code managé](http://msdn.microsoft.com/library/5358a825-e19b-49aa-8214-674ce5fed1da)  
 [Fournisseurs managés ADO.NET et centre de développement DataSet](http://go.microsoft.com/fwlink/?LinkId=217917)
