---
title: Mapper les relations spécifiées pour les éléments imbriqués
ms.date: 03/30/2017
ms.assetid: 24a2d3e5-4af7-4f9a-ab7a-fe6684c9e4fe
ms.openlocfilehash: 0346ba04fd8af6b5abc81fe994dd40f9a6a37c1d
ms.sourcegitcommit: a368166a51e5204c0224fbf5e46476e3ed122817
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2018
ms.locfileid: "43332466"
---
# <a name="map-relations-specified-for-nested-elements"></a><span data-ttu-id="85f1e-102">Mapper les relations spécifiées pour les éléments imbriqués</span><span class="sxs-lookup"><span data-stu-id="85f1e-102">Map Relations Specified for Nested Elements</span></span>
<span data-ttu-id="85f1e-103">Un schéma peut inclure une **msdata : Relationship** annotation à spécifier explicitement le mappage entre les deux éléments quelconques dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="85f1e-103">A schema can include an **msdata:Relationship** annotation to explicitly specify the mapping between any two elements in the schema.</span></span> <span data-ttu-id="85f1e-104">Les deux éléments spécifiés dans **msdata : Relationship** peuvent être imbriqués dans le schéma, mais n’avez pas à être.</span><span class="sxs-lookup"><span data-stu-id="85f1e-104">The two elements specified in **msdata:Relationship** can be nested in the schema, but do not have to be.</span></span> <span data-ttu-id="85f1e-105">Le processus de mappage utilise **msdata : Relationship** dans le schéma pour générer la relation clé primaire/étrangère clé entre les deux colonnes.</span><span class="sxs-lookup"><span data-stu-id="85f1e-105">The mapping process uses **msdata:Relationship** in the schema to generate the primary key/foreign key relationship between the two columns.</span></span>  
  
 <span data-ttu-id="85f1e-106">L’exemple suivant montre un schéma XML dans lequel le **OrderDetail** élément est un élément enfant de **ordre**.</span><span class="sxs-lookup"><span data-stu-id="85f1e-106">The following example shows an XML Schema in which the **OrderDetail** element is a child element of **Order**.</span></span> <span data-ttu-id="85f1e-107">Le **msdata : Relationship** identifie cette relation parent-enfant et spécifie que le **OrderNumber** colonne des résultats de **ordre** table est associée à la **OrderNo** colonne des résultats de **OrderDetail** table.</span><span class="sxs-lookup"><span data-stu-id="85f1e-107">The **msdata:Relationship** identifies this parent-child relationship and specifies that the **OrderNumber** column of the resulting **Order** table is related to the **OrderNo** column of the resulting **OrderDetail** table.</span></span>  
  
```xml  
<xs:schema id="MyDataSet" xmlns=""   
            xmlns:xs="http://www.w3.org/2001/XMLSchema"   
            xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">  
<xs:element name="MyDataSet" msdata:IsDataSet="true">  
 <xs:complexType>  
  <xs:choice maxOccurs="unbounded">  
   <xs:element name="Order">  
    <xs:complexType>  
     <xs:sequence>  
       <xs:element name="OrderNumber" type="xs:string" />  
       <xs:element name="EmpNumber" type="xs:string" />  
       <xs:element name="OrderDetail">  
          <xs:annotation>  
           <xs:appinfo>  
            <msdata:Relationship name="OrdODRelation"   
                                msdata:parent="Order"   
                                msdata:child="OrderDetail"   
                                msdata:parentkey="OrderNumber"   
                                msdata:childkey="OrderNo"/>  
           </xs:appinfo>  
          </xs:annotation>  
          <xs:complexType>  
            <xs:sequence>  
             <xs:element name="OrderNo" type="xs:string" />  
             <xs:element name="ItemNo" type="xs:string" />  
            </xs:sequence>  
         </xs:complexType>  
       </xs:element>  
     </xs:sequence>  
    </xs:complexType>  
   </xs:element>  
  </xs:choice>  
 </xs:complexType>  
</xs:element>  
</xs:schema>  
```  
  
 <span data-ttu-id="85f1e-108">Le processus de mappage du schéma XML crée les éléments suivants dans le <xref:System.Data.DataSet> :</span><span class="sxs-lookup"><span data-stu-id="85f1e-108">The XML Schema mapping process creates the following in the <xref:System.Data.DataSet>:</span></span>  
  
-   <span data-ttu-id="85f1e-109">Un **ordre** et un **OrderDetail** table.</span><span class="sxs-lookup"><span data-stu-id="85f1e-109">An **Order** and an **OrderDetail** table.</span></span>  
  
    ```  
    Order(OrderNumber, EmpNumber)  
    OrderDetail(OrderNo, ItemNo)  
    ```  
  
-   <span data-ttu-id="85f1e-110">Une relation entre la **ordre** et **OrderDetail** tables.</span><span class="sxs-lookup"><span data-stu-id="85f1e-110">A relationship between the **Order** and **OrderDetail** tables.</span></span> <span data-ttu-id="85f1e-111">Le **Nested** propriété pour cette relation est définie sur **True** , car le **ordre** et **OrderDetail** éléments sont imbriqués dans le schéma .</span><span class="sxs-lookup"><span data-stu-id="85f1e-111">The **Nested** property for this relationship is set to **True** because the **Order** and **OrderDetail** elements are nested in the schema.</span></span>  
  
    ```  
    ParentTable: Order  
    ParentColumns: OrderNumber   
    ChildTable: OrderDetail  
    ChildColumns: OrderNo   
    RelationName: OrdODRelation  
    Nested: True  
    ```  
  
 <span data-ttu-id="85f1e-112">Le processus de mappage ne crée aucune contrainte.</span><span class="sxs-lookup"><span data-stu-id="85f1e-112">The mapping process does not create any constraints.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="85f1e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85f1e-113">See Also</span></span>  
 [<span data-ttu-id="85f1e-114">Génération de relations de DataSet à partir du schéma XML (XSD)</span><span class="sxs-lookup"><span data-stu-id="85f1e-114">Generating DataSet Relations from XML Schema (XSD)</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/generating-dataset-relations-from-xml-schema-xsd.md)  
 [<span data-ttu-id="85f1e-115">Mappage des contraintes de schéma XML (XSD) aux contraintes de DataSet</span><span class="sxs-lookup"><span data-stu-id="85f1e-115">Mapping XML Schema (XSD) Constraints to DataSet Constraints</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/mapping-xml-schema-xsd-constraints-to-dataset-constraints.md)  
 [<span data-ttu-id="85f1e-116">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="85f1e-116">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
