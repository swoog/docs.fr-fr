---
title: Réflexion (C#)
ms.date: 07/20/2015
ms.assetid: f80a2362-953b-4e8e-9759-cd5f334190d4
ms.openlocfilehash: fc5c3f6af1a089d824289a55f6781e887b7cfc56
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33340435"
---
# <a name="reflection-c"></a>Réflexion (C#)
La réflexion fournit des objets (de type <xref:System.Type>) qui décrivent des assemblys, des modules et des types. Vous pouvez utiliser la réflexion pour créer dynamiquement une instance d’un type, lier le type à un objet existant ou obtenir le type à partir d’un objet existant et invoquer ses méthodes ou accéder à ses champs et propriétés. Si vous utilisez des attributs dans votre code, la réflexion vous permet d’y accéder. Pour plus d’informations, consultez [Attributs](../../../../docs/standard/attributes/index.md).  
  
 Voici un exemple simple de réflexion utilisant la méthode statique `GetType`, héritée par tous les types à partir de la classe de base `Object`, pour obtenir le type d’une variable :  
  
```csharp  
// Using GetType to obtain type information:  
int i = 42;  
System.Type type = i.GetType();  
System.Console.WriteLine(type);  
```  
  
 La sortie est la suivante :  
  
 `System.Int32`  
  
 L’exemple suivant utilise la réflexion pour obtenir le nom complet de l’assembly chargé.  
  
```csharp  
// Using Reflection to get information from an Assembly:  
System.Reflection.Assembly info = typeof(System.Int32).Assembly;  
System.Console.WriteLine(info);  
```  
  
 La sortie est la suivante :  
  
 `mscorlib, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089`  
  
> [!NOTE]
>  Les mots clés C# `protected` et `internal` n’ont aucune signification en langage intermédiaire et ne sont pas utilisés dans les API de réflexion. Les termes correspondants en langage intermédiaire sont *Family* et *Assembly*. Pour identifier une méthode `internal` à l’aide de la réflexion, utilisez la propriété <xref:System.Reflection.MethodBase.IsAssembly%2A>. Pour identifier une méthode `protected internal`, utilisez <xref:System.Reflection.MethodBase.IsFamilyOrAssembly%2A>.  
  
## <a name="reflection-overview"></a>Vue d’ensemble de la réflexion  
 La réflexion est utile dans les situations suivantes :  
  
-   Lorsque vous devez accéder à des attributs dans les métadonnées de votre programme. Pour plus d’informations, consultez [Récupération des informations stockées dans les attributs](../../../standard/attributes/retrieving-information-stored-in-attributes.md).  
  
-   Pour examiner et instancier des types dans un assembly.  
  
-   Pour créer de nouveaux types au moment de l’exécution. Utilisez des classes dans <xref:System.Reflection.Emit>.  
  
-   Pour effectuer une liaison tardive, en accédant aux méthodes sur les types créés au moment de l’exécution. Consultez la rubrique [Chargement et utilisation dynamiques des types](../../../framework/reflection-and-codedom/dynamically-loading-and-using-types.md).  
  
## <a name="related-sections"></a>Rubriques connexes  
 Pour plus d'informations :  
  
-   [Réflexion](../../../framework/reflection-and-codedom/reflection.md)  
  
-   [Affichage des informations de type](../../../framework/reflection-and-codedom/viewing-type-information.md)  
  
-   [Réflexion et types génériques](../../../framework/reflection-and-codedom/reflection-and-generic-types.md)  
  
-   <xref:System.Reflection.Emit>  
  
-   [Récupération des informations stockées dans les attributs](../../../standard/attributes/retrieving-information-stored-in-attributes.md)  
  
## <a name="see-also"></a>Voir aussi  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Assemblys dans le Common Language Runtime](../../../../docs/framework/app-domains/assemblies-in-the-common-language-runtime.md)
