# Election Simulator Database

This project implements a comprehensive SQL schema for simulating various types of elections, including presidential, parliamentary, assembly of experts, and provincial societies elections. The schema is designed for PostgreSQL and includes tables, views, triggers, and sample data for testing.

## Features

- **Voter and Candidate Management:** Tables for storing voter and candidate information with constraints and validation triggers.
- **Election Structure:** Support for multiple election types, election funds, supervisors, and electoral districts.
- **Voting and Validation:** Tables and triggers to manage voting, candidate qualification, and vote validation.
- **Result Calculation:** Views to compute and display election results, including handling of rejected votes and candidate ranking.
- **Data Integrity:** Triggers to enforce business rules such as age limits, duplicate voting prevention, and candidate qualification.
- **Sample Data:** Pre-populated tables with sample voters, candidates, elections, and votes for testing and demonstration.

## Getting Started

1. **Requirements**

   - PostgreSQL (recommended version 12+)

2. **Setup**

   - Run the SQL script [`finalversionofproject (1).sql`](<finalversionofproject%20(1).sql>) in your PostgreSQL database.
   - This will create all tables, views, triggers, and insert sample data.

3. **Usage**
   - Query the views (e.g., `final_peresult`, `final_ICAResult`, `CandidatePE_Qualified_List`) to see election results and candidate lists.
   - Use the tables to insert new voters, candidates, or simulate new elections and votes.

## Main Components

- **Tables:** Voter, Candidate, Election, ElectionFund, Supervisor, ElectoralDistrict, and election-specific tables.
- **Views:** For user-friendly access to qualified candidates, election results, and fund evaluations.
- **Triggers & Functions:** Enforce rules such as age, name length, city validation, vote limits, and candidate qualification.
- **Indexes:** Improve query performance on commonly searched fields.

## Example Queries

- List all qualified candidates for the presidential election:

  ```sql
  SELECT * FROM CandidatePE_Qualified_List;
  ```

- Get the final results for the parliamentary election:
  ```sql
  SELECT * FROM final_ICAResult;
  ```

## Notes

- All business rules are enforced at the database level using triggers and constraints.
- The schema is extensible for additional election types or rules.

## Authors

- Hossein Mirzagol
- Pegah Gerailoo
- Narges Ghanbari
- Mahtab Jeihani

## License

This project is provided for educational purposes.
