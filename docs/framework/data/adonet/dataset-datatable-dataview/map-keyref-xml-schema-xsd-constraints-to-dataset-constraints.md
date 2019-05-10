---
title: Mapper les contraintes keyref de schéma XML (XSD) aux contraintes de DataSet
ms.date: 03/30/2017
ms.assetid: 5b634fea-cc1e-4f6b-9454-10858105b1c8
ms.openlocfilehash: 4cc4cb530b7252f35469fd4bb43bf6da9c1a3e24
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64604020"
---
# <a name="map-keyref-xml-schema-xsd-constraints-to-dataset-constraints"></a><span data-ttu-id="c2d1a-102">Mapper les contraintes keyref de schéma XML (XSD) aux contraintes de DataSet</span><span class="sxs-lookup"><span data-stu-id="c2d1a-102">Map keyref XML Schema (XSD) Constraints to DataSet Constraints</span></span>
<span data-ttu-id="c2d1a-103">Le **keyref** élément vous permet d’établir des liens entre les éléments dans un document.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-103">The **keyref** element allows you to establish links between elements within a document.</span></span> <span data-ttu-id="c2d1a-104">Le résultat est similaire à une relation de clé étrangère dans une base de données relationnelle.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-104">This is similar to a foreign key relationship in a relational database.</span></span> <span data-ttu-id="c2d1a-105">Si un schéma spécifie le **keyref** élément, l’élément est converti pendant le processus de mappage de schéma pour une contrainte de clé étrangère correspondante sur les colonnes dans les tables de la <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-105">If a schema specifies the **keyref** element, the element is converted during the schema mapping process to a corresponding foreign key constraint on the columns in the tables of the <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="c2d1a-106">Par défaut, le **keyref** élément génère aussi une relation, avec le **ParentTable**, **ChildTable**, **ParentColumn**et  **ChildColumn** propriétés spécifiées sur la relation.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-106">By default, the **keyref** element also generates a relation, with the **ParentTable**, **ChildTable**, **ParentColumn**, and **ChildColumn** properties specified on the relation.</span></span>  
  
 <span data-ttu-id="c2d1a-107">Le tableau suivant présente le **msdata** attributs que vous pouvez spécifier dans le **keyref** élément.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-107">The following table outlines the **msdata** attributes you can specify in the **keyref** element.</span></span>  
  
|<span data-ttu-id="c2d1a-108">Nom d'attribut</span><span class="sxs-lookup"><span data-stu-id="c2d1a-108">Attribute name</span></span>|<span data-ttu-id="c2d1a-109">Description</span><span class="sxs-lookup"><span data-stu-id="c2d1a-109">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="c2d1a-110">**msdata:ConstraintOnly**</span><span class="sxs-lookup"><span data-stu-id="c2d1a-110">**msdata:ConstraintOnly**</span></span>|<span data-ttu-id="c2d1a-111">Si **ConstraintOnly = « true »** est spécifié sur le **keyref** élément dans le schéma, une contrainte est créée, mais aucune relation est créée.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-111">If **ConstraintOnly="true"** is specified on the **keyref** element in the schema, a constraint is created, but no relation is created.</span></span> <span data-ttu-id="c2d1a-112">Si cet attribut n’est pas spécifié (ou a la valeur **False**), la contrainte et la relation sont créés dans le **DataSet**.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-112">If this attribute is not specified (or is set to **False**), both the constraint and the relation are created in the **DataSet**.</span></span>|  
|<span data-ttu-id="c2d1a-113">**msdata:ConstraintName**</span><span class="sxs-lookup"><span data-stu-id="c2d1a-113">**msdata:ConstraintName**</span></span>|<span data-ttu-id="c2d1a-114">Si le **ConstraintName** attribut est spécifié, sa valeur est utilisée comme nom de la contrainte.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-114">If the **ConstraintName** attribute is specified, its value is used as the name of the constraint.</span></span> <span data-ttu-id="c2d1a-115">Sinon, le **nom** attribut de la **keyref** élément dans le schéma fournit le nom de la contrainte dans le **DataSet**.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-115">Otherwise, the **name** attribute of the **keyref** element in the schema provides the constraint name in the **DataSet**.</span></span>|  
|<span data-ttu-id="c2d1a-116">**msdata:UpdateRule**</span><span class="sxs-lookup"><span data-stu-id="c2d1a-116">**msdata:UpdateRule**</span></span>|<span data-ttu-id="c2d1a-117">Si le **UpdateRule** attribut est spécifié dans le **keyref** élément dans le schéma, sa valeur est assignée à la **UpdateRule** propriété contrainte dans le  **Jeu de données**.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-117">If the **UpdateRule** attribute is specified in the **keyref** element in the schema, its value is assigned to the **UpdateRule** constraint property in the **DataSet**.</span></span> <span data-ttu-id="c2d1a-118">Sinon le **UpdateRule** propriété est définie sur **Cascade**.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-118">Otherwise the **UpdateRule** property is set to **Cascade**.</span></span>|  
|<span data-ttu-id="c2d1a-119">**msdata:DeleteRule**</span><span class="sxs-lookup"><span data-stu-id="c2d1a-119">**msdata:DeleteRule**</span></span>|<span data-ttu-id="c2d1a-120">Si le **DeleteRule** attribut est spécifié dans le **keyref** élément dans le schéma, sa valeur est assignée à la **DeleteRule** propriété contrainte dans le  **Jeu de données**.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-120">If the **DeleteRule** attribute is specified in the **keyref** element in the schema, its value is assigned to the **DeleteRule** constraint property in the **DataSet**.</span></span> <span data-ttu-id="c2d1a-121">Sinon le **DeleteRule** propriété est définie sur **Cascade**.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-121">Otherwise the **DeleteRule** property is set to **Cascade**.</span></span>|  
|<span data-ttu-id="c2d1a-122">**msdata:AcceptRejectRule**</span><span class="sxs-lookup"><span data-stu-id="c2d1a-122">**msdata:AcceptRejectRule**</span></span>|<span data-ttu-id="c2d1a-123">Si le **AcceptRejectRule** attribut est spécifié dans le **keyref** élément dans le schéma, sa valeur est assignée à la **AcceptRejectRule** propriété contrainte dans le  **Jeu de données**.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-123">If the **AcceptRejectRule** attribute is specified in the **keyref** element in the schema, its value is assigned to the **AcceptRejectRule** constraint property in the **DataSet**.</span></span> <span data-ttu-id="c2d1a-124">Sinon le **AcceptRejectRule** propriété est définie sur **aucun**.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-124">Otherwise the **AcceptRejectRule** property is set to **None**.</span></span>|  
  
 <span data-ttu-id="c2d1a-125">L’exemple suivant contient un schéma qui spécifie le **clé** et **keyref** relations entre les **OrderNumber** élément enfant de le **ordre**  élément et le **OrderNo** élément enfant de le **OrderDetail** élément.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-125">The following example contains a schema that specifies the **key** and **keyref** relationships between the **OrderNumber** child element of the **Order** element and the **OrderNo** child element of the **OrderDetail** element.</span></span>  
  
 <span data-ttu-id="c2d1a-126">Dans l’exemple, le **OrderNumber** élément enfant de le **OrderDetail** élément fait référence à la **OrderNo** élément enfant clé de la **ordre**élément.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-126">In the example, the **OrderNumber** child element of the **OrderDetail** element refers to the **OrderNo** key child element of the **Order** element.</span></span>  
  
```xml  
<xs:schema id="MyDataSet" xmlns=""   
            xmlns:xs="http://www.w3.org/2001/XMLSchema"   
            xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">  
  
 <xs:element name="MyDataSet" msdata:IsDataSet="true">  
  <xs:complexType>  
    <xs:choice maxOccurs="unbounded">  
      <xs:element name="OrderDetail">  
       <xs:complexType>  
         <xs:sequence>  
           <xs:element name="OrderNo" type="xs:integer" />  
           <xs:element name="ItemNo" type="xs:string" />  
         </xs:sequence>  
       </xs:complexType>  
      </xs:element>  
      <xs:element name="Order">  
        <xs:complexType>  
          <xs:sequence>  
            <xs:element name="OrderNumber" type="xs:integer" />  
            <xs:element name="EmpNumber" type="xs:integer" />  
          </xs:sequence>  
        </xs:complexType>  
      </xs:element>  
    </xs:choice>  
  </xs:complexType>  
  
  <xs:key name="OrderNumberKey"  >  
    <xs:selector xpath=".//Order" />  
    <xs:field xpath="OrderNumber" />  
  </xs:key>  
  
  <xs:keyref name="OrderNoRef" refer="OrderNumberKey">  
    <xs:selector xpath=".//OrderDetail" />  
    <xs:field xpath="OrderNo" />  
  </xs:keyref>  
 </xs:element>  
</xs:schema>  
```  
  
 <span data-ttu-id="c2d1a-127">Le processus de mappage de schéma XML Schema definition langage (XSD XML) produit la suivante **DataSet** avec deux tables :</span><span class="sxs-lookup"><span data-stu-id="c2d1a-127">The XML Schema definition language (XSD) schema mapping process produces the following **DataSet** with two tables:</span></span>  
  
```  
OrderDetail(OrderNo, ItemNo) and  
Order(OrderNumber, EmpNumber)  
```  
  
 <span data-ttu-id="c2d1a-128">En outre, le **DataSet** définit les contraintes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c2d1a-128">In addition, the **DataSet** defines the following constraints:</span></span>  
  
- <span data-ttu-id="c2d1a-129">Une contrainte unique sur la **ordre** table.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-129">A unique constraint on the **Order** table.</span></span>  
  
    ```  
              Table: Order  
    Columns: OrderNumber   
    ConstraintName: OrderNumberKey  
    Type: UniqueConstraint  
    IsPrimaryKey: False  
    ```  
  
- <span data-ttu-id="c2d1a-130">Une relation entre la **ordre** et **OrderDetail** tables.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-130">A relationship between the **Order** and **OrderDetail** tables.</span></span> <span data-ttu-id="c2d1a-131">Le **Nested** propriété est définie sur **False** , car les deux éléments ne sont pas imbriqués dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-131">The **Nested** property is set to **False** because the two elements are not nested in the schema.</span></span>  
  
    ```  
              ParentTable: Order  
    ParentColumns: OrderNumber   
    ChildTable: OrderDetail  
    ChildColumns: OrderNo   
    ParentKeyConstraint: OrderNumberKey  
    ChildKeyConstraint: OrderNoRef  
    RelationName: OrderNoRef  
    Nested: False  
    ```  
  
- <span data-ttu-id="c2d1a-132">Une contrainte de clé étrangère sur la **OrderDetail** table.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-132">A foreign key constraint on the **OrderDetail** table.</span></span>  
  
    ```  
              ConstraintName: OrderNoRef  
    Type: ForeignKeyConstraint  
    Table: OrderDetail  
    Columns: OrderNo   
    RelatedTable: Order  
    RelatedColumns: OrderNumber   
    ```  
  
## <a name="see-also"></a><span data-ttu-id="c2d1a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2d1a-133">See also</span></span>

- [<span data-ttu-id="c2d1a-134">Mappage des contraintes de schéma XML (XSD) aux contraintes de DataSet</span><span class="sxs-lookup"><span data-stu-id="c2d1a-134">Mapping XML Schema (XSD) Constraints to DataSet Constraints</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/mapping-xml-schema-xsd-constraints-to-dataset-constraints.md)
- [<span data-ttu-id="c2d1a-135">Génération de relations de DataSet à partir du schéma XML (XSD)</span><span class="sxs-lookup"><span data-stu-id="c2d1a-135">Generating DataSet Relations from XML Schema (XSD)</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/generating-dataset-relations-from-xml-schema-xsd.md)
- [<span data-ttu-id="c2d1a-136">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="c2d1a-136">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
