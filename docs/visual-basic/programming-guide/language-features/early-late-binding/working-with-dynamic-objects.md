---
title: Utilisation d'objets dynamiques (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- dynamic objects [Visual Basic]
ms.assetid: bdee2a00-07ff-46f9-86dd-fdac9b99cc97
ms.openlocfilehash: 14bd78f2897edc9f2092e062fda16ba5a7d04c37
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54640860"
---
# <a name="working-with-dynamic-objects-visual-basic"></a>Utilisation d'objets dynamiques (Visual Basic)
Objets dynamiques fournissent une autre manière, autre que le `Object` type, à liaison tardive à un objet en cours d’exécution. Un objet dynamique expose des membres tels que les propriétés et méthodes au moment de l’exécution à l’aide des interfaces dynamiques qui sont définies dans le <xref:System.Dynamic> espace de noms. Vous pouvez utiliser les classes dans le <xref:System.Dynamic> espace de noms pour créer des objets qui fonctionnent avec des structures de données qui ne correspondent pas à un format ou le type statique. Vous pouvez également utiliser les objets dynamiques qui sont définies dans les langages dynamiques comme IronPython et IronRuby. Pour obtenir des exemples qui montrent comment créer des objets dynamiques ou utiliser un objet dynamique défini dans un langage dynamique, consultez [procédure pas à pas : Création et utilisation d’objets dynamiques](../../../../csharp/programming-guide/types/walkthrough-creating-and-using-dynamic-objects.md), <xref:System.Dynamic.DynamicObject>, ou <xref:System.Dynamic.ExpandoObject>.  
  
 Visual Basic crée une liaison à des objets depuis le dynamic language runtime et les langages dynamiques comme IronPython et IronRuby à l’aide de la <xref:System.Dynamic.IDynamicMetaObjectProvider> interface. Exemples de classes qui implémentent le `IDynamicMetaObjectProvider` interface sont les <xref:System.Dynamic.DynamicObject> et <xref:System.Dynamic.ExpandoObject> classes.  
  
 Si un appel à liaison tardive est effectué vers un objet qui implémente le `IDynamicMetaObjectProvider` interface, lie Visual Basic à l’objet dynamique à l’aide de cette interface. Si un appel à liaison tardive est effectué vers un objet qui n’implémente pas le `IDynamicMetaObjectProvider` interface, ou si l’appel à la `IDynamicMetaObjectProvider` interface échoue, Visual Basic lie à l’objet en utilisant les fonctionnalités de liaison tardive du runtime Visual Basic.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Dynamic.DynamicObject>
- <xref:System.Dynamic.ExpandoObject>
- [Procédure pas à pas : Création et utilisation d’objets dynamiques](../../../../csharp/programming-guide/types/walkthrough-creating-and-using-dynamic-objects.md)
- [Liaison anticipée et liaison tardive](../../../../visual-basic/programming-guide/language-features/early-late-binding/index.md)
