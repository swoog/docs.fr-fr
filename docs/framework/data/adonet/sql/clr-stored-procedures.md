---
title: Procédures stockées CLR
ms.date: 03/30/2017
ms.assetid: fd7eea9b-218a-4988-8c9a-8abcc6031c66
ms.openlocfilehash: 1f8aa6fb9243706d07caa4527af0c4c880aa70a6
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43424332"
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

1. [Procédures stockées CLR](https://go.microsoft.com/fwlink/?LinkId=115400)  
  
## <a name="see-also"></a>Voir aussi  
 [Création d’objets SQL Server 2005 dans le Code managé](https://msdn.microsoft.com/library/5358a825-e19b-49aa-8214-674ce5fed1da)  
 [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
