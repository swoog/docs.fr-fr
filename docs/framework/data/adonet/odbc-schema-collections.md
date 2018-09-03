---
title: Collections de schémas ODBC
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: bdedbb11960f02b99dcca6388abf663635238f74
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43479978"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="764e6-102">Collections de schémas ODBC</span><span class="sxs-lookup"><span data-stu-id="764e6-102">ODBC Schema Collections</span></span>
<span data-ttu-id="764e6-103">Cette section traite de la prise en charge des collections de schémas pour les pilotes ODBC Microsoft SQL Server, Oracle et Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="764e6-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="764e6-104">Pilote Microsoft SQL Server ODBC</span><span class="sxs-lookup"><span data-stu-id="764e6-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="764e6-105">Le pilote ODBC de Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="764e6-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="764e6-106">Tables</span><span class="sxs-lookup"><span data-stu-id="764e6-106">Tables</span></span>  
  
-   <span data-ttu-id="764e6-107">Index</span><span class="sxs-lookup"><span data-stu-id="764e6-107">Indexes</span></span>  
  
-   <span data-ttu-id="764e6-108">Columns</span><span class="sxs-lookup"><span data-stu-id="764e6-108">Columns</span></span>  
  
-   <span data-ttu-id="764e6-109">Procédures</span><span class="sxs-lookup"><span data-stu-id="764e6-109">Procedures</span></span>  
  
-   <span data-ttu-id="764e6-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="764e6-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="764e6-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="764e6-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="764e6-112">Vues</span><span class="sxs-lookup"><span data-stu-id="764e6-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="764e6-113">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="764e6-113">Tables and Views</span></span>  
  
|<span data-ttu-id="764e6-114">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-114">ColumnName</span></span>|<span data-ttu-id="764e6-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="764e6-116">TABLE_CAT</span></span>|<span data-ttu-id="764e6-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-117">String</span></span>|  
|<span data-ttu-id="764e6-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="764e6-118">TABLE_SCHEM</span></span>|<span data-ttu-id="764e6-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-119">String</span></span>|  
|<span data-ttu-id="764e6-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-120">TABLE_NAME</span></span>|<span data-ttu-id="764e6-121">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-121">String</span></span>|  
|<span data-ttu-id="764e6-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-122">TABLE_TYPE</span></span>|<span data-ttu-id="764e6-123">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-123">String</span></span>|  
|<span data-ttu-id="764e6-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-124">REMARKS</span></span>|<span data-ttu-id="764e6-125">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="764e6-126">Index</span><span class="sxs-lookup"><span data-stu-id="764e6-126">Indexes</span></span>  
  
|<span data-ttu-id="764e6-127">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-127">ColumnName</span></span>|<span data-ttu-id="764e6-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="764e6-129">TABLE_CAT</span></span>|<span data-ttu-id="764e6-130">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-130">String</span></span>|  
|<span data-ttu-id="764e6-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="764e6-131">TABLE_SCHEM</span></span>|<span data-ttu-id="764e6-132">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-132">String</span></span>|  
|<span data-ttu-id="764e6-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-133">TABLE_NAME</span></span>|<span data-ttu-id="764e6-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-134">String</span></span>|  
|<span data-ttu-id="764e6-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="764e6-135">NON_UNIQUE</span></span>|<span data-ttu-id="764e6-136">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-136">Int16</span></span>|  
|<span data-ttu-id="764e6-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="764e6-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="764e6-138">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-138">String</span></span>|  
|<span data-ttu-id="764e6-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-139">INDEX_NAME</span></span>|<span data-ttu-id="764e6-140">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-140">String</span></span>|  
|<span data-ttu-id="764e6-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-141">TYPE</span></span>|<span data-ttu-id="764e6-142">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-142">Int16</span></span>|  
|<span data-ttu-id="764e6-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="764e6-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="764e6-144">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-144">Int16</span></span>|  
|<span data-ttu-id="764e6-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-145">COLUMN_NAME</span></span>|<span data-ttu-id="764e6-146">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-146">String</span></span>|  
|<span data-ttu-id="764e6-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="764e6-147">ASC_OR_DESC</span></span>|<span data-ttu-id="764e6-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-148">String</span></span>|  
|<span data-ttu-id="764e6-149">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="764e6-149">CARDINATLITY</span></span>|<span data-ttu-id="764e6-150">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-150">Int32</span></span>|  
|<span data-ttu-id="764e6-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="764e6-151">PAGES</span></span>|<span data-ttu-id="764e6-152">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-152">Int32</span></span>|  
|<span data-ttu-id="764e6-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="764e6-153">FILTER_CONDITION</span></span>|<span data-ttu-id="764e6-154">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-154">String</span></span>|  
|<span data-ttu-id="764e6-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="764e6-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="764e6-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-156">String</span></span>|  
|<span data-ttu-id="764e6-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="764e6-158">Byte</span><span class="sxs-lookup"><span data-stu-id="764e6-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="764e6-159">Columns</span><span class="sxs-lookup"><span data-stu-id="764e6-159">Columns</span></span>  
  
|<span data-ttu-id="764e6-160">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-160">ColumnName</span></span>|<span data-ttu-id="764e6-161">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="764e6-162">TABLE_CAT</span></span>|<span data-ttu-id="764e6-163">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-163">String</span></span>|  
|<span data-ttu-id="764e6-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="764e6-164">TABLE_SCHEM</span></span>|<span data-ttu-id="764e6-165">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-165">String</span></span>|  
|<span data-ttu-id="764e6-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-166">TABLE_NAME</span></span>|<span data-ttu-id="764e6-167">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-167">String</span></span>|  
|<span data-ttu-id="764e6-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-168">COLUMN_NAME</span></span>|<span data-ttu-id="764e6-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-169">String</span></span>|  
|<span data-ttu-id="764e6-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-170">DATA_TYPE</span></span>|<span data-ttu-id="764e6-171">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-171">Int16</span></span>|  
|<span data-ttu-id="764e6-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-172">TYPE_NAME</span></span>|<span data-ttu-id="764e6-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-173">String</span></span>|  
|<span data-ttu-id="764e6-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="764e6-174">COLUMN_SIZE</span></span>|<span data-ttu-id="764e6-175">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-175">Int32</span></span>|  
|<span data-ttu-id="764e6-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="764e6-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="764e6-177">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-177">Int32</span></span>|  
|<span data-ttu-id="764e6-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="764e6-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="764e6-179">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-179">Int16</span></span>|  
|<span data-ttu-id="764e6-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="764e6-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="764e6-181">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-181">Int16</span></span>|  
|<span data-ttu-id="764e6-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="764e6-182">NULLABLE</span></span>|<span data-ttu-id="764e6-183">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-183">Int16</span></span>|  
|<span data-ttu-id="764e6-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-184">REMARKS</span></span>|<span data-ttu-id="764e6-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-185">String</span></span>|  
|<span data-ttu-id="764e6-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="764e6-186">COLUMN_DEF</span></span>|<span data-ttu-id="764e6-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-187">String</span></span>|  
|<span data-ttu-id="764e6-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="764e6-189">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-189">Int16</span></span>|  
|<span data-ttu-id="764e6-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="764e6-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="764e6-191">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-191">Int16</span></span>|  
|<span data-ttu-id="764e6-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="764e6-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="764e6-193">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-193">Int32</span></span>|  
|<span data-ttu-id="764e6-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="764e6-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="764e6-195">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-195">Int32</span></span>|  
|<span data-ttu-id="764e6-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="764e6-196">IS_NULLABLE</span></span>|<span data-ttu-id="764e6-197">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-197">String</span></span>|  
|<span data-ttu-id="764e6-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="764e6-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="764e6-199">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-199">String</span></span>|  
|<span data-ttu-id="764e6-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="764e6-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="764e6-201">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-201">String</span></span>|  
|<span data-ttu-id="764e6-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="764e6-203">Byte</span><span class="sxs-lookup"><span data-stu-id="764e6-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="764e6-204">Procédures</span><span class="sxs-lookup"><span data-stu-id="764e6-204">Procedures</span></span>  
  
|<span data-ttu-id="764e6-205">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-205">ColumnName</span></span>|<span data-ttu-id="764e6-206">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="764e6-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="764e6-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-208">String</span></span>|  
|<span data-ttu-id="764e6-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="764e6-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="764e6-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-210">String</span></span>|  
|<span data-ttu-id="764e6-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="764e6-212">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-212">String</span></span>|  
|<span data-ttu-id="764e6-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="764e6-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="764e6-214">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-214">Int32</span></span>|  
|<span data-ttu-id="764e6-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="764e6-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="764e6-216">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-216">Int32</span></span>|  
|<span data-ttu-id="764e6-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="764e6-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="764e6-218">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-218">Int32</span></span>|  
|<span data-ttu-id="764e6-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-219">REMARKS</span></span>|<span data-ttu-id="764e6-220">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-220">String</span></span>|  
|<span data-ttu-id="764e6-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="764e6-222">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="764e6-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="764e6-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="764e6-224">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-224">ColumnName</span></span>|<span data-ttu-id="764e6-225">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="764e6-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="764e6-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-227">String</span></span>|  
|<span data-ttu-id="764e6-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="764e6-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="764e6-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-229">String</span></span>|  
|<span data-ttu-id="764e6-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="764e6-231">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-231">String</span></span>|  
|<span data-ttu-id="764e6-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-232">COLUMN_NAME</span></span>|<span data-ttu-id="764e6-233">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-233">String</span></span>|  
|<span data-ttu-id="764e6-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-234">COLUMN_TYPE</span></span>|<span data-ttu-id="764e6-235">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-235">Int16</span></span>|  
|<span data-ttu-id="764e6-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-236">DATA_TYPE</span></span>|<span data-ttu-id="764e6-237">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-237">Int16</span></span>|  
|<span data-ttu-id="764e6-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-238">TYPE_NAME</span></span>|<span data-ttu-id="764e6-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-239">String</span></span>|  
|<span data-ttu-id="764e6-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="764e6-240">COLUMN_SIZE</span></span>|<span data-ttu-id="764e6-241">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-241">Int32</span></span>|  
|<span data-ttu-id="764e6-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="764e6-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="764e6-243">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-243">Int32</span></span>|  
|<span data-ttu-id="764e6-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="764e6-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="764e6-245">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-245">Int16</span></span>|  
|<span data-ttu-id="764e6-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="764e6-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="764e6-247">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-247">Int16</span></span>|  
|<span data-ttu-id="764e6-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="764e6-248">NULLABLE</span></span>|<span data-ttu-id="764e6-249">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-249">Int16</span></span>|  
|<span data-ttu-id="764e6-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-250">REMARKS</span></span>|<span data-ttu-id="764e6-251">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-251">String</span></span>|  
|<span data-ttu-id="764e6-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="764e6-252">COLUMN_DEF</span></span>|<span data-ttu-id="764e6-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-253">String</span></span>|  
|<span data-ttu-id="764e6-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="764e6-255">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-255">Int16</span></span>|  
|<span data-ttu-id="764e6-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="764e6-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="764e6-257">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-257">Int16</span></span>|  
|<span data-ttu-id="764e6-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="764e6-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="764e6-259">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-259">Int32</span></span>|  
|<span data-ttu-id="764e6-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="764e6-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="764e6-261">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-261">Int32</span></span>|  
|<span data-ttu-id="764e6-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="764e6-262">IS_NULLABLE</span></span>|<span data-ttu-id="764e6-263">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-263">String</span></span>|  
|<span data-ttu-id="764e6-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="764e6-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="764e6-265">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-265">String</span></span>|  
|<span data-ttu-id="764e6-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="764e6-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="764e6-267">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-267">String</span></span>|  
|<span data-ttu-id="764e6-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="764e6-269">Byte</span><span class="sxs-lookup"><span data-stu-id="764e6-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="764e6-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="764e6-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="764e6-271">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-271">ColumnName</span></span>|<span data-ttu-id="764e6-272">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="764e6-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="764e6-274">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-274">String</span></span>|  
|<span data-ttu-id="764e6-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="764e6-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="764e6-276">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-276">String</span></span>|  
|<span data-ttu-id="764e6-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="764e6-278">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-278">String</span></span>|  
|<span data-ttu-id="764e6-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-279">COLUMN_NAME</span></span>|<span data-ttu-id="764e6-280">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-280">String</span></span>|  
|<span data-ttu-id="764e6-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-281">COLUMN_TYPE</span></span>|<span data-ttu-id="764e6-282">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-282">Int16</span></span>|  
|<span data-ttu-id="764e6-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-283">DATA_TYPE</span></span>|<span data-ttu-id="764e6-284">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-284">Int16</span></span>|  
|<span data-ttu-id="764e6-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-285">TYPE_NAME</span></span>|<span data-ttu-id="764e6-286">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-286">String</span></span>|  
|<span data-ttu-id="764e6-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="764e6-287">COLUMN_SIZE</span></span>|<span data-ttu-id="764e6-288">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-288">Int32</span></span>|  
|<span data-ttu-id="764e6-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="764e6-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="764e6-290">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-290">Int32</span></span>|  
|<span data-ttu-id="764e6-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="764e6-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="764e6-292">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-292">Int16</span></span>|  
|<span data-ttu-id="764e6-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="764e6-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="764e6-294">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-294">Int16</span></span>|  
|<span data-ttu-id="764e6-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="764e6-295">NULLABLE</span></span>|<span data-ttu-id="764e6-296">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-296">Int16</span></span>|  
|<span data-ttu-id="764e6-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-297">REMARKS</span></span>|<span data-ttu-id="764e6-298">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-298">String</span></span>|  
|<span data-ttu-id="764e6-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="764e6-299">COLUMN_DEF</span></span>|<span data-ttu-id="764e6-300">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-300">String</span></span>|  
|<span data-ttu-id="764e6-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="764e6-302">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-302">Int16</span></span>|  
|<span data-ttu-id="764e6-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="764e6-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="764e6-304">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-304">Int16</span></span>|  
|<span data-ttu-id="764e6-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="764e6-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="764e6-306">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-306">Int32</span></span>|  
|<span data-ttu-id="764e6-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="764e6-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="764e6-308">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-308">Int32</span></span>|  
|<span data-ttu-id="764e6-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="764e6-309">IS_NULLABLE</span></span>|<span data-ttu-id="764e6-310">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-310">String</span></span>|  
|<span data-ttu-id="764e6-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="764e6-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="764e6-312">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-312">String</span></span>|  
|<span data-ttu-id="764e6-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="764e6-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="764e6-314">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-314">String</span></span>|  
|<span data-ttu-id="764e6-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="764e6-316">Byte</span><span class="sxs-lookup"><span data-stu-id="764e6-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="764e6-317">Pilote Microsoft Oracle ODBC</span><span class="sxs-lookup"><span data-stu-id="764e6-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="764e6-318">Le pilote Microsoft SQL Server Oracle ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="764e6-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="764e6-319">Tables</span><span class="sxs-lookup"><span data-stu-id="764e6-319">Tables</span></span>  
  
-   <span data-ttu-id="764e6-320">Columns</span><span class="sxs-lookup"><span data-stu-id="764e6-320">Columns</span></span>  
  
-   <span data-ttu-id="764e6-321">Procédures</span><span class="sxs-lookup"><span data-stu-id="764e6-321">Procedures</span></span>  
  
-   <span data-ttu-id="764e6-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="764e6-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="764e6-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="764e6-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="764e6-324">Vues</span><span class="sxs-lookup"><span data-stu-id="764e6-324">Views</span></span>  
  
-   <span data-ttu-id="764e6-325">Index</span><span class="sxs-lookup"><span data-stu-id="764e6-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="764e6-326">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="764e6-326">Tables and Views</span></span>  
  
|<span data-ttu-id="764e6-327">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-327">ColumnName</span></span>|<span data-ttu-id="764e6-328">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="764e6-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="764e6-330">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-330">String</span></span>|  
|<span data-ttu-id="764e6-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="764e6-331">TABLE_OWNER</span></span>|<span data-ttu-id="764e6-332">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-332">String</span></span>|  
|<span data-ttu-id="764e6-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-333">TABLE_NAME</span></span>|<span data-ttu-id="764e6-334">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-334">String</span></span>|  
|<span data-ttu-id="764e6-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-335">TABLE_TYPE</span></span>|<span data-ttu-id="764e6-336">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-336">String</span></span>|  
|<span data-ttu-id="764e6-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-337">REMARKS</span></span>|<span data-ttu-id="764e6-338">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="764e6-339">Columns</span><span class="sxs-lookup"><span data-stu-id="764e6-339">Columns</span></span>  
  
|<span data-ttu-id="764e6-340">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-340">ColumnName</span></span>|<span data-ttu-id="764e6-341">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="764e6-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="764e6-343">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-343">String</span></span>|  
|<span data-ttu-id="764e6-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="764e6-344">TABLE_OWNER</span></span>|<span data-ttu-id="764e6-345">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-345">String</span></span>|  
|<span data-ttu-id="764e6-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-346">TABLE_NAME</span></span>|<span data-ttu-id="764e6-347">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-347">String</span></span>|  
|<span data-ttu-id="764e6-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-348">COLUMN_NAME</span></span>|<span data-ttu-id="764e6-349">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-349">String</span></span>|  
|<span data-ttu-id="764e6-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-350">DATA_TYPE</span></span>|<span data-ttu-id="764e6-351">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-351">Int16</span></span>|  
|<span data-ttu-id="764e6-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-352">TYPE_NAME</span></span>|<span data-ttu-id="764e6-353">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-353">String</span></span>|  
|<span data-ttu-id="764e6-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="764e6-354">PRECISION</span></span>|<span data-ttu-id="764e6-355">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-355">Int32</span></span>|  
|<span data-ttu-id="764e6-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="764e6-356">LENGTH</span></span>|<span data-ttu-id="764e6-357">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-357">Int32</span></span>|  
|<span data-ttu-id="764e6-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="764e6-358">SCALE</span></span>|<span data-ttu-id="764e6-359">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-359">Int16</span></span>|  
|<span data-ttu-id="764e6-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="764e6-360">RADIX</span></span>|<span data-ttu-id="764e6-361">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-361">Int16</span></span>|  
|<span data-ttu-id="764e6-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="764e6-362">NULLABLE</span></span>|<span data-ttu-id="764e6-363">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-363">Int16</span></span>|  
|<span data-ttu-id="764e6-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-364">REMARKS</span></span>|<span data-ttu-id="764e6-365">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-365">String</span></span>|  
|<span data-ttu-id="764e6-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="764e6-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="764e6-367">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="764e6-368">Procédures</span><span class="sxs-lookup"><span data-stu-id="764e6-368">Procedures</span></span>  
  
|<span data-ttu-id="764e6-369">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-369">ColumnName</span></span>|<span data-ttu-id="764e6-370">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="764e6-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="764e6-372">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-372">String</span></span>|  
|<span data-ttu-id="764e6-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="764e6-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="764e6-374">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-374">String</span></span>|  
|<span data-ttu-id="764e6-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="764e6-376">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-376">String</span></span>|  
|<span data-ttu-id="764e6-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="764e6-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="764e6-378">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-378">Int16</span></span>|  
|<span data-ttu-id="764e6-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="764e6-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="764e6-380">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-380">Int16</span></span>|  
|<span data-ttu-id="764e6-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="764e6-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="764e6-382">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-382">Int16</span></span>|  
|<span data-ttu-id="764e6-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-383">REMARKS</span></span>|<span data-ttu-id="764e6-384">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-384">String</span></span>|  
|<span data-ttu-id="764e6-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="764e6-386">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="764e6-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="764e6-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="764e6-388">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-388">ColumnName</span></span>|<span data-ttu-id="764e6-389">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="764e6-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="764e6-391">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-391">String</span></span>|  
|<span data-ttu-id="764e6-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="764e6-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="764e6-393">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-393">String</span></span>|  
|<span data-ttu-id="764e6-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="764e6-395">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-395">String</span></span>|  
|<span data-ttu-id="764e6-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-396">COLUMN_NAME</span></span>|<span data-ttu-id="764e6-397">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-397">String</span></span>|  
|<span data-ttu-id="764e6-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-398">COLUMN_TYPE</span></span>|<span data-ttu-id="764e6-399">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-399">Int16</span></span>|  
|<span data-ttu-id="764e6-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-400">DATA_TYPE</span></span>|<span data-ttu-id="764e6-401">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-401">Int16</span></span>|  
|<span data-ttu-id="764e6-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-402">TYPE_NAME</span></span>|<span data-ttu-id="764e6-403">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-403">String</span></span>|  
|<span data-ttu-id="764e6-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="764e6-404">PRECISION</span></span>|<span data-ttu-id="764e6-405">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-405">Int32</span></span>|  
|<span data-ttu-id="764e6-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="764e6-406">LENGTH</span></span>|<span data-ttu-id="764e6-407">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-407">Int32</span></span>|  
|<span data-ttu-id="764e6-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="764e6-408">SCALE</span></span>|<span data-ttu-id="764e6-409">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-409">Int16</span></span>|  
|<span data-ttu-id="764e6-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="764e6-410">RADIX</span></span>|<span data-ttu-id="764e6-411">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-411">Int16</span></span>|  
|<span data-ttu-id="764e6-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="764e6-412">NULLABLE</span></span>|<span data-ttu-id="764e6-413">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-413">Int16</span></span>|  
|<span data-ttu-id="764e6-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-414">REMARKS</span></span>|<span data-ttu-id="764e6-415">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-415">String</span></span>|  
|<span data-ttu-id="764e6-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="764e6-416">OVERLOAD</span></span>|<span data-ttu-id="764e6-417">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-417">Int32</span></span>|  
|<span data-ttu-id="764e6-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="764e6-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="764e6-419">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="764e6-420">Pilote Microsoft Jet ODBC</span><span class="sxs-lookup"><span data-stu-id="764e6-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="764e6-421">Le pilote Microsoft Jet ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="764e6-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="764e6-422">Tables</span><span class="sxs-lookup"><span data-stu-id="764e6-422">Tables</span></span>  
  
-   <span data-ttu-id="764e6-423">Index</span><span class="sxs-lookup"><span data-stu-id="764e6-423">Indexes</span></span>  
  
-   <span data-ttu-id="764e6-424">Columns</span><span class="sxs-lookup"><span data-stu-id="764e6-424">Columns</span></span>  
  
-   <span data-ttu-id="764e6-425">Procédures</span><span class="sxs-lookup"><span data-stu-id="764e6-425">Procedures</span></span>  
  
-   <span data-ttu-id="764e6-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="764e6-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="764e6-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="764e6-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="764e6-428">Vues</span><span class="sxs-lookup"><span data-stu-id="764e6-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="764e6-429">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="764e6-429">Tables and Views</span></span>  
  
|<span data-ttu-id="764e6-430">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-430">ColumnName</span></span>|<span data-ttu-id="764e6-431">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="764e6-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="764e6-433">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-433">String</span></span>|  
|<span data-ttu-id="764e6-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="764e6-434">TABLE_OWNER</span></span>|<span data-ttu-id="764e6-435">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-435">String</span></span>|  
|<span data-ttu-id="764e6-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-436">TABLE_NAME</span></span>|<span data-ttu-id="764e6-437">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-437">String</span></span>|  
|<span data-ttu-id="764e6-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-438">TABLE_TYPE</span></span>|<span data-ttu-id="764e6-439">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-439">String</span></span>|  
|<span data-ttu-id="764e6-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-440">REMARKS</span></span>|<span data-ttu-id="764e6-441">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="764e6-442">Columns</span><span class="sxs-lookup"><span data-stu-id="764e6-442">Columns</span></span>  
  
|<span data-ttu-id="764e6-443">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-443">ColumnName</span></span>|<span data-ttu-id="764e6-444">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="764e6-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="764e6-446">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-446">String</span></span>|  
|<span data-ttu-id="764e6-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="764e6-447">TABLE_OWNER</span></span>|<span data-ttu-id="764e6-448">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-448">String</span></span>|  
|<span data-ttu-id="764e6-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-449">TABLE_NAME</span></span>|<span data-ttu-id="764e6-450">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-450">String</span></span>|  
|<span data-ttu-id="764e6-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-451">COLUMN_NAME</span></span>|<span data-ttu-id="764e6-452">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-452">String</span></span>|  
|<span data-ttu-id="764e6-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-453">DATA_TYPE</span></span>|<span data-ttu-id="764e6-454">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-454">Int16</span></span>|  
|<span data-ttu-id="764e6-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-455">TYPE_NAME</span></span>|<span data-ttu-id="764e6-456">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-456">String</span></span>|  
|<span data-ttu-id="764e6-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="764e6-457">PRECISION</span></span>|<span data-ttu-id="764e6-458">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-458">Int32</span></span>|  
|<span data-ttu-id="764e6-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="764e6-459">LENGTH</span></span>|<span data-ttu-id="764e6-460">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-460">Int32</span></span>|  
|<span data-ttu-id="764e6-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="764e6-461">SCALE</span></span>|<span data-ttu-id="764e6-462">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-462">Int16</span></span>|  
|<span data-ttu-id="764e6-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="764e6-463">RADIX</span></span>|<span data-ttu-id="764e6-464">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-464">Int16</span></span>|  
|<span data-ttu-id="764e6-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="764e6-465">NULLABLE</span></span>|<span data-ttu-id="764e6-466">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-466">Int16</span></span>|  
|<span data-ttu-id="764e6-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-467">REMARKS</span></span>|<span data-ttu-id="764e6-468">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-468">String</span></span>|  
|<span data-ttu-id="764e6-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="764e6-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="764e6-470">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="764e6-471">Procédures</span><span class="sxs-lookup"><span data-stu-id="764e6-471">Procedures</span></span>  
  
|<span data-ttu-id="764e6-472">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-472">ColumnName</span></span>|<span data-ttu-id="764e6-473">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="764e6-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="764e6-475">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-475">String</span></span>|  
|<span data-ttu-id="764e6-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="764e6-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="764e6-477">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-477">String</span></span>|  
|<span data-ttu-id="764e6-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="764e6-479">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-479">String</span></span>|  
|<span data-ttu-id="764e6-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="764e6-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="764e6-481">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-481">Int16</span></span>|  
|<span data-ttu-id="764e6-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="764e6-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="764e6-483">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-483">Int16</span></span>|  
|<span data-ttu-id="764e6-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="764e6-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="764e6-485">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-485">Int16</span></span>|  
|<span data-ttu-id="764e6-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-486">REMARKS</span></span>|<span data-ttu-id="764e6-487">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-487">String</span></span>|  
|<span data-ttu-id="764e6-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="764e6-489">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="764e6-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="764e6-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="764e6-491">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-491">ColumnName</span></span>|<span data-ttu-id="764e6-492">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="764e6-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="764e6-494">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-494">String</span></span>|  
|<span data-ttu-id="764e6-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="764e6-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="764e6-496">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-496">String</span></span>|  
|<span data-ttu-id="764e6-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="764e6-498">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-498">String</span></span>|  
|<span data-ttu-id="764e6-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-499">COLUMN_NAME</span></span>|<span data-ttu-id="764e6-500">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-500">String</span></span>|  
|<span data-ttu-id="764e6-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-501">COLUMN_TYPE</span></span>|<span data-ttu-id="764e6-502">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-502">Int16</span></span>|  
|<span data-ttu-id="764e6-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-503">DATA_TYPE</span></span>|<span data-ttu-id="764e6-504">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-504">Int16</span></span>|  
|<span data-ttu-id="764e6-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-505">TYPE_NAME</span></span>|<span data-ttu-id="764e6-506">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-506">String</span></span>|  
|<span data-ttu-id="764e6-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="764e6-507">PRECISION</span></span>|<span data-ttu-id="764e6-508">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-508">Int32</span></span>|  
|<span data-ttu-id="764e6-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="764e6-509">LENGTH</span></span>|<span data-ttu-id="764e6-510">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-510">Int32</span></span>|  
|<span data-ttu-id="764e6-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="764e6-511">SCALE</span></span>|<span data-ttu-id="764e6-512">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-512">Int16</span></span>|  
|<span data-ttu-id="764e6-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="764e6-513">RADIX</span></span>|<span data-ttu-id="764e6-514">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-514">Int16</span></span>|  
|<span data-ttu-id="764e6-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="764e6-515">NULLABLE</span></span>|<span data-ttu-id="764e6-516">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-516">Int16</span></span>|  
|<span data-ttu-id="764e6-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-517">REMARKS</span></span>|<span data-ttu-id="764e6-518">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-518">String</span></span>|  
|<span data-ttu-id="764e6-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="764e6-519">OVERLOAD</span></span>|<span data-ttu-id="764e6-520">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-520">Int32</span></span>|  
|<span data-ttu-id="764e6-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="764e6-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="764e6-522">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="764e6-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="764e6-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="764e6-524">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="764e6-524">ColumnName</span></span>|<span data-ttu-id="764e6-525">Type de données</span><span class="sxs-lookup"><span data-stu-id="764e6-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="764e6-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="764e6-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="764e6-527">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-527">String</span></span>|  
|<span data-ttu-id="764e6-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="764e6-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="764e6-529">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-529">String</span></span>|  
|<span data-ttu-id="764e6-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="764e6-531">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-531">String</span></span>|  
|<span data-ttu-id="764e6-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-532">COLUMN_NAME</span></span>|<span data-ttu-id="764e6-533">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-533">String</span></span>|  
|<span data-ttu-id="764e6-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-534">COLUMN_TYPE</span></span>|<span data-ttu-id="764e6-535">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-535">Int16</span></span>|  
|<span data-ttu-id="764e6-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-536">DATA_TYPE</span></span>|<span data-ttu-id="764e6-537">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-537">Int16</span></span>|  
|<span data-ttu-id="764e6-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="764e6-538">TYPE_NAME</span></span>|<span data-ttu-id="764e6-539">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-539">String</span></span>|  
|<span data-ttu-id="764e6-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="764e6-540">COLUMN_SIZE</span></span>|<span data-ttu-id="764e6-541">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-541">Int32</span></span>|  
|<span data-ttu-id="764e6-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="764e6-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="764e6-543">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-543">Int32</span></span>|  
|<span data-ttu-id="764e6-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="764e6-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="764e6-545">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-545">Int16</span></span>|  
|<span data-ttu-id="764e6-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="764e6-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="764e6-547">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-547">Int16</span></span>|  
|<span data-ttu-id="764e6-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="764e6-548">NULLABLE</span></span>|<span data-ttu-id="764e6-549">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-549">Int16</span></span>|  
|<span data-ttu-id="764e6-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="764e6-550">REMARKS</span></span>|<span data-ttu-id="764e6-551">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-551">String</span></span>|  
|<span data-ttu-id="764e6-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="764e6-552">COLUMN_DEF</span></span>|<span data-ttu-id="764e6-553">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-553">String</span></span>|  
|<span data-ttu-id="764e6-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="764e6-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="764e6-555">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-555">Int16</span></span>|  
|<span data-ttu-id="764e6-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="764e6-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="764e6-557">Int16</span><span class="sxs-lookup"><span data-stu-id="764e6-557">Int16</span></span>|  
|<span data-ttu-id="764e6-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="764e6-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="764e6-559">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-559">Int32</span></span>|  
|<span data-ttu-id="764e6-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="764e6-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="764e6-561">Int32</span><span class="sxs-lookup"><span data-stu-id="764e6-561">Int32</span></span>|  
|<span data-ttu-id="764e6-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="764e6-562">IS_NULLABLE</span></span>|<span data-ttu-id="764e6-563">Chaîne</span><span class="sxs-lookup"><span data-stu-id="764e6-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="764e6-564">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="764e6-564">See Also</span></span>  
 [<span data-ttu-id="764e6-565">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="764e6-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
