### Project Data

All data files are stored in UVA OneDrive.  
Access the data here: [OneDrive Data Folder](<https://myuva-my.sharepoint.com/:f:/r/personal/csg7su_virginia_edu/Documents/DS4320-Project1-Data?csf=1&web=1&e=mRTiR>)

### Data Files

The following files are available in the OneDrive folder:

| File | Rows | Size | Description |
| :--- | :--- | :--- | :--- |
| **projects.csv** | 11,473 | 0.81 MB | Central registry metadata (Name, Type, developer_id) |
| **developers.csv** | 3,676 | 0.16 MB | Unique project developer entities |
| **locations.csv** | 11,473 | 0.83 MB | Geographic data (Region, Country, State) |
| **methodology.csv** | 11,473 | 0.91 MB | Technical protocols and registry scopes |
| **performance.csv** | 11,473 | 0.59 MB | Credit issuance and retirement metrics |
| **TOTAL** | **~49,500** | **3.30 MB** | **5 Relational Tables** |

### Parquet Versions

Compressed parquet versions are also available (0.56 MB total, 83% smaller).

### Data Source

Berkeley Carbon Trading Project (v2026-02) University of California, Berkeley - Goldman School of Public Policy.  
Official URL: [Berkeley Carbon Registry](https://gspp.berkeley.edu/research-and-impact/centers/cepp/projects/berkeley-carbon-trading-project/offsets-database)  
Downloaded: March 30, 2026

---

### Architectural Note: Row Count Consistency & 3NF
The identical row counts (**11,473**) across the `projects`, `locations`, `methodology`, and `performance` tables are a result of **Vertical Partitioning** designed to satisfy **Third Normal Form (3NF)** requirements.

1. **1:1 Relationships:** Each unique carbon project possesses exactly one set of geographic coordinates, one technical methodology, and one set of performance results. Isolating these into separate tables removes transitive dependencies and ensures that non-key attributes (like "State" or "Protocol") are strictly related to their specific dimension's Primary Key.
2. **1:N Relationships:** The `developers` table contains only **3,676** rows. This creates a one-to-many relationship where a single developer entity can be associated with multiple project records, significantly reducing data redundancy and optimizing the database for group-based analysis.