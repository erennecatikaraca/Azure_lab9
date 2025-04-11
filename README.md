# Load Data into a Relational Data Warehouse - Lab Exercise 🚀

## 📌 Lab Overview
This lab guides you through loading data into a **dedicated SQL pool** in Azure Synapse Analytics. You'll practice:
- Using the `COPY` statement for efficient data loading
- Creating tables with `CTAS` (CREATE TABLE AS SELECT)
- Implementing slowly changing dimension (SCD) patterns
- Performing post-load optimization

## ⏳ Estimated Duration
Approximately **30 minutes**

## 🛠️ Prerequisites
- [Azure subscription](https://azure.microsoft.com/free) with admin access
- Basic knowledge of SQL and data warehousing concepts

## 🏗️ Lab Setup
1. **Provision Azure Synapse workspace**:
   - Run the provided PowerShell script in Azure Cloud Shell
   - Script will deploy:
     - Synapse workspace
     - Data Lake Storage Gen2
     - Dedicated SQL pool

2. **Prepare data**:
   - Verify CSV files (`Product.csv`, `Customer.csv`) in the data lake
   - Start the dedicated SQL pool

## 🔍 Key Tasks
### 1. Load data using COPY statement
- Load data from CSV files into staging tables
- Handle errors with error files in `_rejectedrows` folder

### 2. Create dimension tables
- Use `CTAS` to create `DimProduct` table
- Implement SCD patterns for `DimCustomer`:
  - Type 1 changes (in-place updates)
  - Type 2 changes (historical tracking)

### 3. Post-load optimization
- Rebuild table indexes
- Create statistics for query optimization

## 🧹 Cleanup
Don't forget to:
1. Pause or delete the SQL pool when not in use
2. Delete the resource group to avoid ongoing charges

## 📚 Additional Resources
- [Data loading strategies for dedicated SQL pool](https://learn.microsoft.com/azure/synapse-analytics/sql-data-warehouse/design-elt-data-loading)
- [COPY command documentation](https://docs.microsoft.com/sql/t-sql/statements/copy-into-transact-sql)
- [CTAS best practices](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-tables-ctas)
- [lab-9](https://github.com/secedit/dp-203-azure-data-engineer/blob/master/Instructions/Labs/09-Load-Data-into-Data-Warehouse.md)