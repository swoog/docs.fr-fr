---
title: "Procédure : Implémenter des événements d'interface - Guide de programmation C#"
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- interfaces [C#], event implementation in classes
- events [C#], in interfaces
ms.assetid: 63527447-9535-4880-8e95-35e2075827df
ms.openlocfilehash: d52d4d5140e96f81377733e39d1c36886718b706
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236438"
---
# <a name="how-to-implement-interface-events-c-programming-guide"></a><span data-ttu-id="094b6-102">Procédure : Implémenter des événements d'interface (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="094b6-102">How to: Implement Interface Events (C# Programming Guide)</span></span>
<span data-ttu-id="094b6-103">Une [interface](../../../csharp/language-reference/keywords/interface.md) peut déclarer un [événement](../../../csharp/language-reference/keywords/event.md).</span><span class="sxs-lookup"><span data-stu-id="094b6-103">An [interface](../../../csharp/language-reference/keywords/interface.md) can declare an [event](../../../csharp/language-reference/keywords/event.md).</span></span> <span data-ttu-id="094b6-104">L’exemple suivant montre comment implémenter des événements d’interface dans une classe.</span><span class="sxs-lookup"><span data-stu-id="094b6-104">The following example shows how to implement interface events in a class.</span></span> <span data-ttu-id="094b6-105">En gros, les règles sont les mêmes que quand vous implémentez une propriété ou une méthode d’interface.</span><span class="sxs-lookup"><span data-stu-id="094b6-105">Basically the rules are the same as when you implement any interface method or property.</span></span>  
  
## <a name="to-implement-interface-events-in-a-class"></a><span data-ttu-id="094b6-106">Pour implémenter des événements d’interface dans une classe</span><span class="sxs-lookup"><span data-stu-id="094b6-106">To implement interface events in a class</span></span>  
  
<span data-ttu-id="094b6-107">Déclarez l’événement dans votre classe, puis appelez-le aux emplacements appropriés.</span><span class="sxs-lookup"><span data-stu-id="094b6-107">Declare the event in your class and then invoke it in the appropriate areas.</span></span>  
  
```csharp
namespace ImplementInterfaceEvents  
{  
    public interface IDrawingObject  
    {  
        event EventHandler ShapeChanged;  
    }  
    public class MyEventArgs : EventArgs   
    {  
        // class members  
    }  
    public class Shape : IDrawingObject  
    {  
        public event EventHandler ShapeChanged;  
        void ChangeShape()  
        {  
            // Do something here before the event…  

            OnShapeChanged(new MyEventArgs(/*arguments*/));  

            // or do something here after the event.   
        }  
        protected virtual void OnShapeChanged(MyEventArgs e)  
        {  
            ShapeChanged?.Invoke(this, e);  
        }  
    }  

}  
```  
  
## <a name="example"></a><span data-ttu-id="094b6-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="094b6-108">Example</span></span>  
<span data-ttu-id="094b6-109">L’exemple suivant montre comment gérer la situation peu courante dans laquelle votre classe hérite de plusieurs interfaces et chaque interface a un événement ayant le même nom.</span><span class="sxs-lookup"><span data-stu-id="094b6-109">The following example shows how to handle the less-common situation in which your class inherits from two or more interfaces and each interface has an event with the same name.</span></span> <span data-ttu-id="094b6-110">Dans ce cas, vous devez fournir une implémentation d’interface explicite pour au moins l’un des événements.</span><span class="sxs-lookup"><span data-stu-id="094b6-110">In this situation, you must provide an explicit interface implementation for at least one of the events.</span></span> <span data-ttu-id="094b6-111">Quand vous écrivez une implémentation d’interface explicite pour un événement, vous devez également écrire les accesseurs d’événement `add` et `remove`.</span><span class="sxs-lookup"><span data-stu-id="094b6-111">When you write an explicit interface implementation for an event, you must also write the `add` and `remove` event accessors.</span></span> <span data-ttu-id="094b6-112">Normalement, ces éléments sont fournis par le compilateur, mais dans le cas en question le compilateur ne peut pas les fournir.</span><span class="sxs-lookup"><span data-stu-id="094b6-112">Normally these are provided by the compiler, but in this case the compiler cannot provide them.</span></span>  
  
<span data-ttu-id="094b6-113">En fournissant vos propres accesseurs, vous pouvez spécifier si les deux événements sont représentés par le même événement dans votre classe ou par des événements différents.</span><span class="sxs-lookup"><span data-stu-id="094b6-113">By providing your own accessors, you can specify whether the two events are represented by the same event in your class, or by different events.</span></span> <span data-ttu-id="094b6-114">Par exemple, si les événements doivent être déclenchés à des moments différents en fonction des spécifications de l’interface, vous pouvez associer chaque événement à une implémentation distincte dans votre classe.</span><span class="sxs-lookup"><span data-stu-id="094b6-114">For example, if the events should be raised at different times according to the interface specifications, you can associate each event with a separate implementation in your class.</span></span> <span data-ttu-id="094b6-115">Dans l’exemple suivant, les abonnés déterminent l’événement `OnDraw` qu’il recevront en effectuant un cast de la référence de la forme en `IShape` ou `IDrawingObject`.</span><span class="sxs-lookup"><span data-stu-id="094b6-115">In the following example, subscribers determine which `OnDraw` event they will receive by casting the shape reference to either an `IShape` or an `IDrawingObject`.</span></span>  
  
 [!code-csharp[WrapTwoInterfaceEvents](../../../csharp/programming-guide/events/codesnippet/CSharp/how-to-implement-interface-events_1.cs#everything)]
  
## <a name="see-also"></a><span data-ttu-id="094b6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="094b6-116">See Also</span></span>

- [<span data-ttu-id="094b6-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="094b6-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="094b6-118">Événements</span><span class="sxs-lookup"><span data-stu-id="094b6-118">Events</span></span>](../../../csharp/programming-guide/events/index.md)  
- [<span data-ttu-id="094b6-119">Délégués</span><span class="sxs-lookup"><span data-stu-id="094b6-119">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)  
- [<span data-ttu-id="094b6-120">Implémentation d’interface explicite</span><span class="sxs-lookup"><span data-stu-id="094b6-120">Explicit Interface Implementation</span></span>](../../../csharp/programming-guide/interfaces/explicit-interface-implementation.md)  
- [<span data-ttu-id="094b6-121">Guide pratique pour déclencher les événements de la classe de base dans les classes dérivées</span><span class="sxs-lookup"><span data-stu-id="094b6-121">How to: Raise Base Class Events in Derived Classes</span></span>](../../../csharp/programming-guide/events/how-to-raise-base-class-events-in-derived-classes.md)
