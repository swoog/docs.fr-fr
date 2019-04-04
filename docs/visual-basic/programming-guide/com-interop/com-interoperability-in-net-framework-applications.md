---
title: Interopérabilité COM dans les applications .NET Framework (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- interoperability, COM and .NET framework objects
- COM interop [Visual Basic]
- shared components
ms.assetid: f5a72143-c268-4dff-a019-974ad940e17d
ms.openlocfilehash: 6e8b4eba40cc1872cb289ca120679bb951f2652a
ms.sourcegitcommit: a3db1a9eafca89f95ccf361bc1833b47fbb2bb30
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/04/2019
ms.locfileid: "58920803"
---
# <a name="com-interoperability-in-net-framework-applications-visual-basic"></a>Interopérabilité COM dans les applications .NET Framework (Visual Basic)

Lorsque vous souhaitez utiliser des objets COM et des objets .NET Framework dans la même application, vous devez résoudre les différences dans la façon dont les objets existent dans la mémoire. Un objet .NET Framework se trouve dans la mémoire managée, la mémoire contrôlée par le common language runtime et peut être déplacé par le runtime en fonction des besoins. Un objet COM se trouve dans la mémoire non managée et n’est pas prévu de passer à un autre emplacement de mémoire. Visual Studio et le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] fournissent des outils pour contrôler l’interaction de ces composants managés et. Pour plus d’informations sur le code managé, consultez [Common Language Runtime](../../../standard/clr.md).

Outre l’utilisation des objets COM dans les applications .NET, vous souhaiterez également utiliser Visual Basic pour développer des objets accessibles à partir de code non managé via COM.

Les liens sur cette page fournissent des détails sur les interactions entre les objets COM et .NET Framework.

## <a name="related-sections"></a>Rubriques connexes

| | |
|---------|---------|
| [COM Interop](../../../visual-basic/programming-guide/com-interop/index.md) | Fournit des liens vers des rubriques traitant de l’interopérabilité COM en Visual Basic, y compris les objets COM, les contrôles ActiveX, les DLL Win32, des objets gérés et l’héritage des objets COM. |
| [Interopération avec du code non managé](../../../framework/interop/index.md) | Certains problèmes d’interaction entre du code managé et décrit brièvement et fournit des liens pour approfondir ce sujet. |
| [Wrappers COM](../../../framework/interop/com-wrappers.md) | Traite des wrappers RCW, qui permettent au code managé d’appeler les méthodes COM, et par COM, qui permettent aux clients COM d’appeler les méthodes d’objet .NET. |
| [Interopérabilité COM avancée](../../../framework/interop/index.md) | Fournit des liens vers des rubriques traitant de l’interopérabilité COM en ce qui concerne les wrappers, exceptions, l’héritage, threading, événements, les conversions et marshaling. |
| [Tlbimp.exe (Type Library Importer)](../../../framework/tools/tlbimp-exe-type-library-importer.md) | Traite de l’outil que vous pouvez utiliser pour convertir les définitions de type trouvées dans une bibliothèque de types COM en définitions équivalentes dans un assembly du common language runtime. |