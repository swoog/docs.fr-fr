---
title: Interopérabilité COM dans les applications .NET Framework (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- interoperability, COM and .NET framework objects
- COM interop [Visual Basic]
- shared components
ms.assetid: f5a72143-c268-4dff-a019-974ad940e17d
ms.openlocfilehash: ceef4255321e208911a16db0227890bc6654b8c5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33642921"
---
# <a name="com-interoperability-in-net-framework-applications-visual-basic"></a>Interopérabilité COM dans les applications .NET Framework (Visual Basic)
Lorsque vous souhaitez utiliser les objets COM et .NET Framework dans la même application, vous devez résoudre les différences dans la façon dont les objets existent dans la mémoire. Un objet .NET Framework se trouve dans la mémoire managée, la mémoire contrôlée par le common language runtime et peut être déplacé par le runtime en fonction des besoins. Un objet COM se trouve dans la mémoire non managée et n’est pas censé déplacer vers un autre emplacement de mémoire. Visual Studio et [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] fournissent des outils pour contrôler l’interaction de ces composants managés et. Pour plus d’informations sur le code managé, consultez [Common Language Runtime](../../../standard/clr.md).  
  
 Outre l’utilisation des objets COM dans les applications .NET, vous pouvez souhaiter également utiliser Visual Basic pour développer des objets accessibles à partir de code non managé via COM.  
  
 Les liens de cette page fournissent des détails sur les interactions entre les objets COM et .NET Framework.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [COM Interop](../../../visual-basic/programming-guide/com-interop/index.md)  
 Fournit des liens vers les rubriques traitant l’interopérabilité COM en Visual Basic, y compris les objets COM, les contrôles ActiveX, les DLL Win32, les objets managés et l’héritage d’objets COM.  
  
 [Erreur de Wrapper COM Interop](/cpp/misc/com-interop-wrapper-error)  
 Décrit les conséquences et les options si le système de projet ne peut pas créer un wrapper d’interopérabilité COM pour un composant particulier.  
  
 [Interopération avec du code non managé](../../../framework/interop/index.md)  
 Certains problèmes d’interaction entre du code managé et décrit brièvement et fournit des liens pour approfondir ce sujet.  
  
 [Wrappers COM](../../../framework/interop/com-wrappers.md)  
 Présente les wrappers RCW, qui permettent au code managé d’appeler les méthodes COM, et par COM, qui permettent aux clients COM d’appeler les méthodes d’objet .NET.  
  
 [Interopérabilité COM avancée](../../../framework/interop/index.md)  
 Fournit des liens vers les rubriques traitant l’interopérabilité COM en ce qui concerne les wrappers, exceptions, l’héritage, threads, les événements, les conversions et marshaling.  
  
 [Tlbimp.exe (importateur de bibliothèques de types)](../../../framework/tools/tlbimp-exe-type-library-importer.md)  
 Décrit l’outil que vous pouvez utiliser pour convertir les définitions de type trouvées dans une bibliothèque de types COM en définitions équivalentes dans un assembly du common language runtime.
