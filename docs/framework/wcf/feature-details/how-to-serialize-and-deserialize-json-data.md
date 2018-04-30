---
title: 'Comment : sérialiser et désérialiser des données JSON'
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 88abc1fb-8196-4ee3-a23b-c6934144d1dd
caps.latest.revision: 13
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 9152e0047102661664f9b158aa26f83fb1d3c25c
ms.sourcegitcommit: 94d33cadc5ff81d2ac389bf5f26422c227832052
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2018
---
# <a name="how-to-serialize-and-deserialize-json-data"></a><span data-ttu-id="e4178-102">Comment : sérialiser et désérialiser des données JSON</span><span class="sxs-lookup"><span data-stu-id="e4178-102">How to: Serialize and Deserialize JSON Data</span></span>
<span data-ttu-id="e4178-103">JSON (JavaScript Object Notation) est un format d'encodage de données efficace qui permet l'échange rapide de petites quantités de données entre les navigateurs clients et les services Web compatibles AJAX.</span><span class="sxs-lookup"><span data-stu-id="e4178-103">JSON (JavaScript Object Notation) is an efficient data encoding format that enables fast exchanges of small amounts of data between client browsers and AJAX-enabled Web services.</span></span>  
  
 <span data-ttu-id="e4178-104">Cette rubrique décrit comment sérialiser des objets de type .NET dans des données encodées JSON et ensuite désérialiser les données au format JSON en instances de type .NET à l'aide de <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>.</span><span class="sxs-lookup"><span data-stu-id="e4178-104">This topic demonstrates how to serialize .NET type objects into JSON-encoded data and then deserialize data in the JSON format back into instances of .NET types using the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>.</span></span> <span data-ttu-id="e4178-105">Cet exemple utilise un contrat de données pour montrer la sérialisation et la désérialisation d'un type `Person` défini par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e4178-105">This example uses a data contract to demonstrate serialization and deserialization of a user-defined `Person` type.</span></span>  
  
 <span data-ttu-id="e4178-106">Normalement, la sérialisation et la désérialisation JSON sont contrôlées automatiquement par [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] lorsque vous utilisez les types de contrats de données dans les opérations de service exposées sur des points de terminaison compatibles AJAX.</span><span class="sxs-lookup"><span data-stu-id="e4178-106">Normally, JSON serialization and deserialization is handled automatically by [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] when you use data contract types in service operations that are exposed over AJAX-enabled endpoints.</span></span> <span data-ttu-id="e4178-107">Toutefois, dans certains cas, vous devez travailler directement avec les données JSON ; c'est le scénario abordé dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e4178-107">However, in some cases you may need to work with JSON data directly - this is the scenario that this topic demonstrates.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e4178-108">Si une erreur se produit pendant la sérialisation d'une réponse sortante sur le serveur ou si l'opération de réponse lève une quelconque exception, il se peut qu'elle ne soit pas retournée au client sous forme d'erreur.</span><span class="sxs-lookup"><span data-stu-id="e4178-108">If an error occurs during serialization of an outgoing reply on the server or the reply operation throws an exception for some other reason, it may not get returned to the client as a fault.</span></span>  
  
 <span data-ttu-id="e4178-109">Cette rubrique est basée sur le [sérialisation JSON](../../../../docs/framework/wcf/samples/json-serialization.md) exemple.</span><span class="sxs-lookup"><span data-stu-id="e4178-109">This topic is based on the [JSON Serialization](../../../../docs/framework/wcf/samples/json-serialization.md) sample.</span></span>  
  
### <a name="to-define-the-data-contract-for-a-person"></a><span data-ttu-id="e4178-110">Pour définir le contrat de données pour une personne</span><span class="sxs-lookup"><span data-stu-id="e4178-110">To define the data contract for a Person</span></span>  
  
1.  <span data-ttu-id="e4178-111">Définissez le contrat de données pour `Person` en joignant <xref:System.Runtime.Serialization.DataContractAttribute> à la classe et l'attribut <xref:System.Runtime.Serialization.DataMemberAttribute> aux membres que vous souhaitez sérialiser.</span><span class="sxs-lookup"><span data-stu-id="e4178-111">Define the data contract for `Person` by attaching the <xref:System.Runtime.Serialization.DataContractAttribute> to the class and <xref:System.Runtime.Serialization.DataMemberAttribute> attribute to the members you want to serialize.</span></span> <span data-ttu-id="e4178-112">Pour plus d’informations sur les contrats de données, consultez [concevoir des contrats de Service](../../../../docs/framework/wcf/designing-service-contracts.md).</span><span class="sxs-lookup"><span data-stu-id="e4178-112">For more information about data contracts, see [Designing Service Contracts](../../../../docs/framework/wcf/designing-service-contracts.md).</span></span>  
  
    ```csharp  
    [DataContract]  
    internal class Person  
    {  
        [DataMember]  
        internal string name;  
  
        [DataMember]  
        internal int age;  
    }  
    ```  
  
### <a name="to-serialize-an-instance-of-type-person-to-json"></a><span data-ttu-id="e4178-113">Pour sérialiser une instance de type Person à JSON</span><span class="sxs-lookup"><span data-stu-id="e4178-113">To serialize an instance of type Person to JSON</span></span>  
  
1.  <span data-ttu-id="e4178-114">Créez une instance du type `Person`.</span><span class="sxs-lookup"><span data-stu-id="e4178-114">Create an instance of the `Person` type.</span></span>  
  
    ```csharp  
    Person p = new Person();  
    p.name = "John";  
    p.age = 42;  
    ```  
  
2.  <span data-ttu-id="e4178-115">Sérialisez l'objet `Person` à un flux de données de mémoire à l'aide de <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>.</span><span class="sxs-lookup"><span data-stu-id="e4178-115">Serialize the `Person` object to a memory stream using the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>.</span></span>  
  
    ```csharp  
    MemoryStream stream1 = new MemoryStream();  
    DataContractJsonSerializer ser = new DataContractJsonSerializer(typeof(Person));  
    ```  
  
3.  <span data-ttu-id="e4178-116">Utilisez la méthode <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject%2A> pour écrire les données JSON dans le flux.</span><span class="sxs-lookup"><span data-stu-id="e4178-116">Use the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject%2A> method to write JSON data to the stream.</span></span>  
  
    ```csharp  
    ser.WriteObject(stream1, p);  
    ```  
  
4.  <span data-ttu-id="e4178-117">Affichez la sortie JSON.</span><span class="sxs-lookup"><span data-stu-id="e4178-117">Show the JSON output.</span></span>  
  
    ```csharp  
    stream1.Position = 0;  
    StreamReader sr = new StreamReader(stream1);  
    Console.Write("JSON form of Person object: ");  
    Console.WriteLine(sr.ReadToEnd());  
    ```  
  
### <a name="to-deserialize-an-instance-of-type-person-from-json"></a><span data-ttu-id="e4178-118">Pour désérialiser une instance de type Person depuis JSON</span><span class="sxs-lookup"><span data-stu-id="e4178-118">To deserialize an instance of type Person from JSON</span></span>  
  
1.  <span data-ttu-id="e4178-119">Désérialisez les données encodées JSON dans une nouvelle instance de `Person` à l'aide de la méthode <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.ReadObject%2A> de <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>.</span><span class="sxs-lookup"><span data-stu-id="e4178-119">Deserialize the JSON-encoded data into a new instance of `Person` by using the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.ReadObject%2A> method of the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>.</span></span>  
  
    ```csharp  
    stream1.Position = 0;  
    Person p2 = (Person)ser.ReadObject(stream1);  
    ```  
  
2.  <span data-ttu-id="e4178-120">Affichez les résultats.</span><span class="sxs-lookup"><span data-stu-id="e4178-120">Show the results.</span></span>  
  
    ```csharp  
    Console.WriteLine($"Deserialized back, got name={p2.name}, age={p2.age}");  
    ```  
  
## <a name="example"></a><span data-ttu-id="e4178-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="e4178-121">Example</span></span>  
  
```csharp  
// Create a User object and serialize it to a JSON stream.  
public static string WriteFromObject()  
{  
    //Create User object.  
    User user = new User("Bob", 42);  
  
    //Create a stream to serialize the object to.  
    MemoryStream ms = new MemoryStream();  
  
    // Serializer the User object to the stream.  
    DataContractJsonSerializer ser = new DataContractJsonSerializer(typeof(User));  
    ser.WriteObject(ms, user);  
    byte[] json = ms.ToArray();  
    ms.Close();  
    return Encoding.UTF8.GetString(json, 0, json.Length);  
}  
  
// Deserialize a JSON stream to a User object.  
public static User ReadToObject(string json)  
{  
    User deserializedUser = new User();  
    MemoryStream ms = new MemoryStream(Encoding.UTF8.GetBytes(json));  
    DataContractJsonSerializer ser = new DataContractJsonSerializer(deserializedUser.GetType());  
    deserializedUser = ser.ReadObject(ms) as User;  
    ms.Close();  
    return deserializedUser;  
}  
```  
  
> [!NOTE]
>  <span data-ttu-id="e4178-122">Le sérialiseur JSON lève une exception de sérialisation pour les contrats de données dont plusieurs membres portent le même nom, comme illustré dans l'exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="e4178-122">The JSON serializer throws a serialization exception for data contracts that have multiple members with the same name, as shown in the following sample code.</span></span>  
  
```csharp  
[DataContract]  
public class TestDuplicateDataBase  
{  
    [DataMember]  
    public int field1 = 123;  
}

[DataContract]  
public class TestDuplicateDataDerived : TestDuplicateDataBase  
{  
    [DataMember]  
    public new int field1 = 999;  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="e4178-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4178-123">See Also</span></span>  
 [<span data-ttu-id="e4178-124">Sérialisation JSON autonome</span><span class="sxs-lookup"><span data-stu-id="e4178-124">Stand-Alone JSON Serialization</span></span>](../../../../docs/framework/wcf/feature-details/stand-alone-json-serialization.md)  
 [<span data-ttu-id="e4178-125">Prise en charge du format JSON et d’autres formats de transfert de données</span><span class="sxs-lookup"><span data-stu-id="e4178-125">Support for JSON and Other Data Transfer Formats</span></span>](../../../../docs/framework/wcf/feature-details/support-for-json-and-other-data-transfer-formats.md)
