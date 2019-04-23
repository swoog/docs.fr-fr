---
title: Procédures stockées CLR
ms.date: 03/30/2017
ms.assetid: fd7eea9b-218a-4988-8c9a-8abcc6031c66
ms.openlocfilehash: 9b31d93c1ebc0af9aa8e41b3a4c328af62da7e23
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59230809"
---
# <a name="clr-stored-procedures"></a><span data-ttu-id="b2a0b-102">Procédures stockées CLR</span><span class="sxs-lookup"><span data-stu-id="b2a0b-102">CLR Stored Procedures</span></span>
<span data-ttu-id="b2a0b-103">Les procédures stockées sont des routines pouvant être utilisées dans les expressions scalaires.</span><span class="sxs-lookup"><span data-stu-id="b2a0b-103">Stored procedures are routines that cannot be used in scalar expressions.</span></span> <span data-ttu-id="b2a0b-104">Elles peuvent retourner des résultats tabulaires et des messages au client, invoquer des instructions DDL (Data Definition Language) et DML (Data Manipulation Language) et retourner des paramètres de sortie.</span><span class="sxs-lookup"><span data-stu-id="b2a0b-104">They can return tabular results and messages to the client, invoke data definition language (DDL) and data manipulation language (DML) statements, and return output parameters.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b2a0b-105">Microsoft Visual Basic ne prend pas en charge les paramètres de sortie de la même manière que Microsoft Visual C#.</span><span class="sxs-lookup"><span data-stu-id="b2a0b-105">Microsoft Visual Basic does not support output parameters in the same way that Microsoft Visual C# does.</span></span> <span data-ttu-id="b2a0b-106">Vous devez spécifier pour passer le paramètre par référence et appliquer le \<Out() > attribut pour représenter un paramètre de sortie, comme suit :</span><span class="sxs-lookup"><span data-stu-id="b2a0b-106">You must specify to pass the parameter by reference and apply the \<Out()> attribute to represent an output parameter, as in the following:</span></span>  
  
```vb
Public Shared Sub ExecuteToClient( <Out()> ByRef number As Integer)  
```
  
<span data-ttu-id="b2a0b-107">Pour plus d’informations, consultez la version de [documentation de SQL Server](/sql) pour la version de SQL Server que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="b2a0b-107">For more detailed information, see the version of [SQL Server documentation](/sql) for the version of SQL Server you're using.</span></span>
  
 <span data-ttu-id="b2a0b-108">**Documentation de SQL Server**</span><span class="sxs-lookup"><span data-stu-id="b2a0b-108">**SQL Server documentation**</span></span>

1. [<span data-ttu-id="b2a0b-109">Procédures stockées CLR</span><span class="sxs-lookup"><span data-stu-id="b2a0b-109">CLR Stored Procedures</span></span>](https://go.microsoft.com/fwlink/?LinkId=115400)  
  
## <a name="see-also"></a><span data-ttu-id="b2a0b-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2a0b-110">See also</span></span>

- <span data-ttu-id="b2a0b-111">[Création d’objets SQL Server 2005 dans le Code managé](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/6s0s2at1(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="b2a0b-111">[Creating SQL Server 2005 Objects In Managed Code](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/6s0s2at1(v=vs.90))</span></span>
- [<span data-ttu-id="b2a0b-112">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="b2a0b-112">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
