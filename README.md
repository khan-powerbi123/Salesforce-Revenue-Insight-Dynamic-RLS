# Salesforce Revenue Insight – Dynamic Row-Level Security (RLS)

### 📊 Project Overview  
This project demonstrates an enterprise-grade Power BI dashboard built using **Salesforce opportunity and account data**.  
It provides actionable insights on revenue, deal size, and win rates while implementing **Dynamic Row-Level Security (RLS)** to ensure users see only data relevant to their access level.

---

### ⚙️ Key Highlights  
- **Dynamic RLS:** Implemented using `USERPRINCIPALNAME()` for user-based filtering.  
- **Composite Security Logic:** Combined `Account Type` + `Industry` into a single key (`CombinedKey`) to control multi-field RLS access.  
- **Optimized Data Modeling:** Managed *many-to-many* relationships with controlled cross-filter direction to avoid ambiguity.  
- **KPIs Included:**  
  - Total Revenue ($)  
  - Win Rate %  
  - Average Deal Size ($)  
  - Forecasted Pipeline Revenue ($)  
- **Deployed as Power BI App:** Packaged and published to Power BI Service for secure sharing and access management.

---

### 🧠 Tools & Technologies  
| Category | Tools Used |
|-----------|-------------|
| BI Platform | Microsoft Power BI Desktop & Service |
| Data Source | Salesforce (Accounts, Opportunities) |
| ETL | Power Query |
| Modeling | DAX, Relationships, Dynamic RLS |
| Deployment | Power BI Workspace & App |

---

### 🗂️ Data Model Summary  
- **Account ↔ Opportunity:** One-to-many (AccountID).  
- **Account ↔ Dynamic_RLS_Mapping:** Many-to-many (CombinedKey).  
- **Cross-filter direction:** Single (for performance & clarity).  
- **Security propagation:** Via relationship between `Account` and RLS mapping table.  

---

### 🚀 Deployment Steps  
1. Created workspace **Salesforce_Insights** in Power BI Service.  
2. Published dataset and report from Power BI Desktop.  
3. Configured Dynamic RLS using `USERPRINCIPALNAME()`.  
4. Validated access for each user role.  
5. Deployed and published as a Power BI App for end-user access.

---

