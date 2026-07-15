# Limitations

- **2021 is a partial year.** The dataset only includes Q1 and Q2 of 2021, while 2018–2020 each have all 4 quarters. Any year-over-year comparison involving 2021 should be normalized (e.g., average per quarter) rather than compared on raw annual totals, or it will understate 2021's actual growth.

- **Lepa Rada district (Arunachal Pradesh) has zero recorded population, area, and density.** This is likely because it's a newly formed district not yet reflected in the demographic source data. Any population- or density-based analysis involving this district should treat it as missing data rather than a true zero.

- **Registered Users is not additive across time.** Summing `Registered Users` across multiple quarters for the same state (as done in a few merge steps, e.g. users-to-population ratio) overstates the true user base, since the same registered users are counted repeatedly in each quarter they appear. A more precise version of these metrics would use only the most recent quarter's registered user count rather than a sum across all quarters.

- **ATV (Average Transaction Value) is a derived field**, calculated in the source data as `Amount / Transactions`. It was not independently recalculated in this analysis; its accuracy depends on the source data's own computation.

- **Correlation analysis (density vs. transaction volume) is at the district level only** and does not control for other variables (income, urbanization, merchant density, internet penetration) that likely also influence transaction activity. The reported correlation should be read as descriptive, not causal.
