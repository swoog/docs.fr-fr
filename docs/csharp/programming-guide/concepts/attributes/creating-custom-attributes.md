---
title: Création d’attributs personnalisés (C#)
ms.date: 07/20/2015
ms.assetid: 500e1977-c6de-462d-abce-78a0eb1eda22
ms.openlocfilehash: 0a27924623cc462f6d3339149718a1b29999ac1d
ms.sourcegitcommit: deb9225a55485a5a6e6c7914deb30ccfceb69d3f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2019
ms.locfileid: "54058267"
---
# <a name="creating-custom-attributes-c"></a><span data-ttu-id="364d2-102">Création d’attributs personnalisés (C#)</span><span class="sxs-lookup"><span data-stu-id="364d2-102">Creating Custom Attributes (C#)</span></span>
<span data-ttu-id="364d2-103">Vous pouvez créer vos propres attributs personnalisés en définissant une classe d’attributs. Cette classe dérive directement ou indirectement d’<xref:System.Attribute>, ce qui permet d’identifier rapidement et facilement des définitions d’attributs dans des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="364d2-103">You can create your own custom attributes by defining an attribute class, a class that derives directly or indirectly from <xref:System.Attribute>, which makes identifying attribute definitions in metadata fast and easy.</span></span> <span data-ttu-id="364d2-104">Supposons que vous souhaitiez baliser des types avec le nom du programmeur qui les a écrits.</span><span class="sxs-lookup"><span data-stu-id="364d2-104">Suppose you want to tag types with the name of the programmer who wrote the type.</span></span> <span data-ttu-id="364d2-105">Vous pouvez définir une classe d’attributs `Author` personnalisés :</span><span class="sxs-lookup"><span data-stu-id="364d2-105">You might define a custom `Author` attribute class:</span></span>  
  
```csharp  
[System.AttributeUsage(System.AttributeTargets.Class |  
                       System.AttributeTargets.Struct)  
]  
public class Author : System.Attribute  
{  
    private string name;  
    public double version;  
  
    public Author(string name)  
    {  
        this.name = name;  
        version = 1.0;  
    }  
}  
```  
  
 <span data-ttu-id="364d2-106">Le nom de la classe est le nom de l’attribut, `Author`.</span><span class="sxs-lookup"><span data-stu-id="364d2-106">The class name is the attribute's name, `Author`.</span></span> <span data-ttu-id="364d2-107">Étant dérivée de `System.Attribute`, il s’agit donc d’une classe d’attributs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="364d2-107">It is derived from `System.Attribute`, so it is a custom attribute class.</span></span> <span data-ttu-id="364d2-108">Les paramètres du constructeur sont les paramètres positionnels de l’attribut personnalisé.</span><span class="sxs-lookup"><span data-stu-id="364d2-108">The constructor's parameters are the custom attribute's positional parameters.</span></span> <span data-ttu-id="364d2-109">Dans cet exemple, `name` est un paramètre positionnel.</span><span class="sxs-lookup"><span data-stu-id="364d2-109">In this example, `name` is a positional parameter.</span></span> <span data-ttu-id="364d2-110">Les propriétés ou champs de type public accessibles en lecture/écriture sont des paramètres nommés.</span><span class="sxs-lookup"><span data-stu-id="364d2-110">Any public read-write fields or properties are named parameters.</span></span> <span data-ttu-id="364d2-111">Dans le cas présent, `version` est le seul paramètre nommé.</span><span class="sxs-lookup"><span data-stu-id="364d2-111">In this case, `version` is the only named parameter.</span></span> <span data-ttu-id="364d2-112">Notez l’utilisation de l’attribut `AttributeUsage` pour rendre l’attribut `Author` valide uniquement sur les déclarations de classe et de `struct`.</span><span class="sxs-lookup"><span data-stu-id="364d2-112">Note the use of the `AttributeUsage` attribute to make the `Author` attribute valid only on class and `struct` declarations.</span></span>  
  
 <span data-ttu-id="364d2-113">Vous pouvez utiliser ce nouvel attribut de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="364d2-113">You could use this new attribute as follows:</span></span>  
  
```csharp  
[Author("P. Ackerman", version = 1.1)]  
class SampleClass  
{  
    // P. Ackerman's code goes here...  
}  
```  
  
 <span data-ttu-id="364d2-114">`AttributeUsage` a un paramètre nommé, `AllowMultiple`, qui permet de déclarer un attribut personnalisé comme étant à usage unique ou multiple.</span><span class="sxs-lookup"><span data-stu-id="364d2-114">`AttributeUsage` has a named parameter, `AllowMultiple`, with which you can make a custom attribute single-use or multiuse.</span></span> <span data-ttu-id="364d2-115">Dans l’exemple de code suivant, un attribut à usage multiple est créé.</span><span class="sxs-lookup"><span data-stu-id="364d2-115">In the following code example, a multiuse attribute is created.</span></span>  
  
```csharp  
[System.AttributeUsage(System.AttributeTargets.Class |  
                       System.AttributeTargets.Struct,  
                       AllowMultiple = true)  // multiuse attribute  
]  
public class Author : System.Attribute  
```  
  
 <span data-ttu-id="364d2-116">Dans l’exemple de code suivant, plusieurs attributs du même type sont appliqués à une classe.</span><span class="sxs-lookup"><span data-stu-id="364d2-116">In the following code example, multiple attributes of the same type are applied to a class.</span></span>  
  
```csharp  
[Author("P. Ackerman", version = 1.1)]  
[Author("R. Koch", version = 1.2)]  
class SampleClass  
{  
    // P. Ackerman's code goes here...  
    // R. Koch's code goes here...  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="364d2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="364d2-117">See Also</span></span>

- <xref:System.Reflection>  
- [<span data-ttu-id="364d2-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="364d2-118">C# Programming Guide</span></span>](../../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="364d2-119">Écriture des attributs personnalisés</span><span class="sxs-lookup"><span data-stu-id="364d2-119">Writing Custom Attributes</span></span>](../../../../standard/attributes/writing-custom-attributes.md)  
- [<span data-ttu-id="364d2-120">Réflexion (C#)</span><span class="sxs-lookup"><span data-stu-id="364d2-120">Reflection (C#)</span></span>](../../../../csharp/programming-guide/concepts/reflection.md)  
- [<span data-ttu-id="364d2-121">Attributs (C#)</span><span class="sxs-lookup"><span data-stu-id="364d2-121">Attributes (C#)</span></span>](../../../../csharp/programming-guide/concepts/attributes/index.md)  
- [<span data-ttu-id="364d2-122">Accès à des attributs à l’aide de la réflexion (C#)</span><span class="sxs-lookup"><span data-stu-id="364d2-122">Accessing Attributes by Using Reflection (C#)</span></span>](../../../../csharp/programming-guide/concepts/attributes/accessing-attributes-by-using-reflection.md)  
- [<span data-ttu-id="364d2-123">AttributeUsage (C#)</span><span class="sxs-lookup"><span data-stu-id="364d2-123">AttributeUsage (C#)</span></span>](../../../../csharp/programming-guide/concepts/attributes/attributeusage.md)
