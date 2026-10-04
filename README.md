# Mapping Compliance Risk in Consumer Finance: Evidence from 2025 CFPB Complaints

An analysis of 5.4 million consumer complaints filed with the Consumer Financial Protection Bureau (CFPB) in 2025, examining where consumer harm is concentrated, how well companies resolve complaints, and what drives sudden spikes in complaint volume.

**[View the interactive dashboard]([ADD_YOUR_TABLEAU_LINK](https://public.tableau.com/app/profile/hana.elzayat/viz/MappingComplianceRiskinConsumerFinance/Dashboard1))** · **[Read the findings memo](file:///Users/hanaelzayat/Downloads/Mapping%20Compliance%20Risk%20in%20Consumer%20Finance_%20Evidence%20from%202025%20CFPB%20Complaints%20(1).pdf)**

## Key findings

- **Relief rates vary tenfold among companies offering the same product.** For checking account complaints, Citibank and Bank of America provided relief in about 40% of cases, compared with about 4% for Capital One.
- **Two major payment providers almost never resolve complaints in consumers' favor.** Block (Cash App) and Early Warning Services (Zelle) provided relief in essentially 0% of complaints, while PayPal (30%) and Coinbase (26%) did so far more often. Block's rate stayed near zero even after excluding a January surge.
- **A three-day surge in January 2025 distorted company metrics.** Complaints against four companies exploded between January 14 and 17. Most of the Zelle and Cash App surge has been attributed to a viral social media campaign, while the Navy Federal and Capital One spikes coincided with CFPB enforcement actions.
- **Debt collection is the largest source of complaints** (39.5%), led by attempts to collect debts consumers say they do not owe.

## Approach

1. **Data preparation:** Combined six bimonthly exports covering all 2025 complaints (5,442,964 records) and removed duplicates.
2. **Scoping:** Credit reporting made up 88% of complaints, so I analyzed it separately. I also removed 94,271 complaints against the three credit bureaus that were filed under other product labels, since these most likely reflect credit report disputes. The final analysis set contains 538,171 complaints.
3. **Company scorecards:** For companies with at least 1,000 complaints, I calculated timely response rates and relief rates (monetary or non-monetary), comparing companies within the same product.
4. **Anomaly detection:** Flagged unusual monthly spikes using z-scores, then examined daily data to test competing explanations.
5. **Robustness check:** Recalculated relief rates excluding January to confirm which patterns persisted beyond the surge.

## Tools

- **Python** (pandas) in Google Colab for data cleaning and analysis
- **Tableau Public** for the interactive dashboard

## Repository contents

- `analysis.ipynb`: full analysis notebook with code and documented decisions
- `memo.pdf`: two-page findings memo with recommendations

## Data source

[CFPB Consumer Complaint Database archive](https://www.consumerfinance.gov/foia-requests/foia-electronic-reading-room/cfpb-consumer-complaint-database-narratives-archive/). Raw data files are not included due to their size.

## Limitations

Complaint outcomes are self-reported by companies and not verified by the CFPB. Complaints are not a representative sample of consumer experiences, and complaints about institutions with less than $10 billion in assets are not published. Low relief rates indicate areas for further investigation rather than proof of misconduct.

## Author

Hana Elzayat, New York University (B.A. Economics; B.A. Global Liberal Studies, Law and Ethics; Minor in Data Science)
