---
title: 'Procédure : Désérialiser un objet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- deserializing objects
- objects, deserializing steps
ms.assetid: 287129c8-035a-4fea-b7b3-4790057ca076
ms.openlocfilehash: d0b953e4f570f349edeb80fc2316530494905ec0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54583309"
---
# <a name="how-to-deserialize-an-object"></a><span data-ttu-id="c780d-102">Procédure : Désérialiser un objet</span><span class="sxs-lookup"><span data-stu-id="c780d-102">How to: Deserialize an Object</span></span>
<span data-ttu-id="c780d-103">Lorsque vous désérialisez un objet, le format de transport vous permet de déterminer si vous créez un flux de données ou un objet de fichier.</span><span class="sxs-lookup"><span data-stu-id="c780d-103">When you deserialize an object, the transport format determines whether you will create a stream or file object.</span></span> <span data-ttu-id="c780d-104">Après avoir déterminé le format de transport, vous pouvez appeler la méthode <xref:System.Xml.Serialization.XmlSerializer.Serialize%2A> ou <xref:System.Xml.Serialization.XmlSerializer.Deserialize%2A>, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c780d-104">After the transport format is determined, you can call the <xref:System.Xml.Serialization.XmlSerializer.Serialize%2A> or <xref:System.Xml.Serialization.XmlSerializer.Deserialize%2A> methods, as required.</span></span>  
  
### <a name="to-deserialize-an-object"></a><span data-ttu-id="c780d-105">Pour désérialiser un objet</span><span class="sxs-lookup"><span data-stu-id="c780d-105">To deserialize an object</span></span>  
  
1.  <span data-ttu-id="c780d-106">Construisez un <xref:System.Xml.Serialization.XmlSerializer> à l'aide du type d'objet à désérialiser.</span><span class="sxs-lookup"><span data-stu-id="c780d-106">Construct a <xref:System.Xml.Serialization.XmlSerializer> using the type of the object to deserialize.</span></span>  
  
2.  <span data-ttu-id="c780d-107">Appelez la méthode <xref:System.Xml.Serialization.XmlSerializer.Deserialize%2A> pour produire un réplica de l'objet.</span><span class="sxs-lookup"><span data-stu-id="c780d-107">Call the <xref:System.Xml.Serialization.XmlSerializer.Deserialize%2A> method to produce a replica of the object.</span></span> <span data-ttu-id="c780d-108">Lorsque vous effectuez une désérialisation, vous devez exécuter un transtypage de l'objet retourné au type d'origine (comme illustré dans l'exemple suivant). Celui-ci désérialise l'objet dans un fichier (bien qu'il puisse également être désérialisé dans un flux de données).</span><span class="sxs-lookup"><span data-stu-id="c780d-108">When deserializing, you must cast the returned object to the type of the original, as shown in the following example, which deserializes the object into a file (although it could also be deserialized into a stream).</span></span>  
  
    ```vb  
    Dim myObject As MySerializableClass  
    ' Construct an instance of the XmlSerializer with the type  
    ' of object that is being deserialized.  
    Dim mySerializer As XmlSerializer = New XmlSerializer(GetType(MySerializableClass))  
    ' To read the file, create a FileStream.  
    Dim myFileStream As FileStream = _  
    New FileStream("myFileName.xml", FileMode.Open)  
    ' Call the Deserialize method and cast to the object type.  
    myObject = CType( _  
    mySerializer.Deserialize(myFileStream), MySerializableClass)  
    ```  
  
    ```csharp  
    MySerializableClass myObject;  
    // Construct an instance of the XmlSerializer with the type  
    // of object that is being deserialized.  
    XmlSerializer mySerializer =   
    new XmlSerializer(typeof(MySerializableClass));  
    // To read the file, create a FileStream.  
    FileStream myFileStream =   
    new FileStream("myFileName.xml", FileMode.Open);  
    // Call the Deserialize method and cast to the object type.  
    myObject = (MySerializableClass)   
    mySerializer.Deserialize(myFileStream)  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="c780d-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c780d-109">See also</span></span>

- [<span data-ttu-id="c780d-110">Introduction à la sérialisation XML</span><span class="sxs-lookup"><span data-stu-id="c780d-110">Introducing XML Serialization</span></span>](../../../docs/standard/serialization/introducing-xml-serialization.md)
- [<span data-ttu-id="c780d-111">Guide pratique pour Sérialiser un objet</span><span class="sxs-lookup"><span data-stu-id="c780d-111">How to: Serialize an Object</span></span>](../../../docs/standard/serialization/how-to-serialize-an-object.md)
