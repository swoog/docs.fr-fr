---
title: Utilisation d'objets dynamiques (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- dynamic objects [Visual Basic]
ms.assetid: bdee2a00-07ff-46f9-86dd-fdac9b99cc97
ms.openlocfilehash: 78b17a379ea219cc24842322703caaa9d29eeb2e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33647347"
---
# <a name="working-with-dynamic-objects-visual-basic"></a>Utilisation d'objets dynamiques (Visual Basic)
Objets dynamiques fournissent une autre manière, autre que le `Object` type, à liaison tardive à un objet en cours d’exécution. Un objet dynamique expose des membres tels que les propriétés et méthodes au moment de l’exécution à l’aide des interfaces dynamiques qui sont définies dans le <xref:System.Dynamic> espace de noms. Vous pouvez utiliser les classes dans le <xref:System.Dynamic> espace de noms pour créer des objets qui fonctionnent avec des structures de données qui ne correspondent pas à un format ou le type statique. Vous pouvez également utiliser les objets dynamiques qui sont définies dans les langages dynamiques tels que IronPython et IronRuby. Pour obtenir des exemples qui montrent comment créer des objets dynamiques ou utiliser un objet dynamique défini dans un langage dynamique, consultez [procédure pas à pas : création et à l’aide d’objets dynamiques](../../../../csharp/programming-guide/types/walkthrough-creating-and-using-dynamic-objects.md), <xref:System.Dynamic.DynamicObject>, ou <xref:System.Dynamic.ExpandoObject>.  
  
 Visual Basic crée une liaison à des objets le dynamic language runtime et les langages dynamiques tels que IronPython et IronRuby à l’aide de la <xref:System.Dynamic.IDynamicMetaObjectProvider> interface. Exemples de classes qui implémentent la `IDynamicMetaObjectProvider` interface sont les <xref:System.Dynamic.DynamicObject> et <xref:System.Dynamic.ExpandoObject> classes.  
  
 Si un appel à liaison tardive est apportée à un objet qui implémente le `IDynamicMetaObjectProvider` de l’interface, lie Visual Basic à l’objet dynamique à l’aide de cette interface. Si un appel à liaison tardive à un objet qui n’implémente pas le `IDynamicMetaObjectProvider` interface, ou si l’appel à la `IDynamicMetaObjectProvider` interface échoue, Visual Basic lie à l’objet en utilisant les fonctionnalités de liaison tardive du runtime Visual Basic.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Dynamic.DynamicObject>  
 <xref:System.Dynamic.ExpandoObject>  
 [Procédure pas à pas : création et utilisation d’objets dynamiques](../../../../csharp/programming-guide/types/walkthrough-creating-and-using-dynamic-objects.md)  
 [Liaison anticipée et liaison tardive](../../../../visual-basic/programming-guide/language-features/early-late-binding/index.md)
