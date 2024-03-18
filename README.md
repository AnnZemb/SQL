## Drug Database Overview

### Introduction
This repository contains a SQL database schema and related queries and procedures for managing a drug database system. The system is designed to efficiently store and manage information related to doctors, patients, prescriptions, pharmacies, drug availability, drug manufacturers, drug prices, and more.

### Tables
1. **Doctor**: Stores information about doctors, including their ID, name, specialization, and contact number.
2. **Drug**: Contains details about drugs, such as ID, name, stock quantity, expiration date, and the manufacturer company.
3. **DrugAvailability**: Tracks the availability of drugs in different pharmacies, including the quantity and availability date.
4. **DrugManufacturer**: Stores information about drug manufacturing companies, including their ID, name, and contact number.
5. **DrugStatus**: Keeps track of the status of drugs in pharmacies, indicating whether they are available or out of stock.
6. **Patient**: Stores details about patients, including their ID, name, address, and contact number.
7. **Pharmacy**: Contains information about pharmacies, such as their ID, name, contact number, and city.
8. **Prescription**: Stores records of prescriptions issued to patients by doctors, including details like prescription ID, patient ID, doctor ID, and prescription date.
9. **PrescriptionDetails**: Contains information about the drugs prescribed in each prescription, including the quantity.
10. **Price**: Stores the cost prices of drugs along with their previous prices.
11. **PriceChangeHistory**: Tracks changes in drug prices over time.

### Functions
1. **GetDrugsInPharmacy**: Retrieves a list of drugs available in a given pharmacy.
2. **GetPrescriptionCountForDoctor**: Calculates the total number of prescriptions issued by a specific doctor.
3. **GetTotalCostForPatient**: Computes the total cost of drugs for a particular patient.
4. **GetAverageDrugsPerPatient**: Determines the average number of drugs prescribed to a patient by all doctors.

### Procedures
1. **UpdateDrugAvailability**: Updates the quantity of a drug in a pharmacy.
2. **UpdateDrugPrice**: Modifies the price of a drug and maintains a history of price changes.
3. **MarkPrescriptionAsFulfilled**: Marks a prescription as fulfilled once it's been processed.

### Views
1. **PatientPrescriptionInfo**: Combines information about patients, doctors, and prescribed drugs.
2. **DrugAvailabilityInfo**: Provides details about drug availability in pharmacies.
3. **DrugInfo**: Presents information about drugs, including their prices and manufacturers.
4. **PatientPrescriptionDrugAvailability**: Combines data about patients, doctors, drugs, prescriptions, and drug availability.
   
### Triggers
1. **UpdateDrugAvailabilityOnPrescriptionFulfillment**: Automatically updates drug availability upon prescription fulfillment.
2. **TrackDrugPriceChanges**: Tracks changes in drug prices and maintains a history of price changes.
3. **NotifyOutOfStock**: Notifies about out-of-stock drugs before the update is made.

### Indexing
Indexes have been added to the DrugAvailability table to optimize querying performance, specifically on the DrugID, PharmacyID, and AvailabilityDate columns.

This comprehensive database schema and associated functionalities aim to facilitate efficient management and retrieval of information related to drugs, prescriptions, pharmacies, and medical practitioners.
