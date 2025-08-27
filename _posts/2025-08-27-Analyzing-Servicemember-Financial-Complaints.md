---
title: An Analysis of Complaint Data Using Python and NLP
date: 2025-08-27
image: 
blurb: Utilizing 5 years of CFPB complaint data concerning three pillars of financial security, credit cards, car loans (or leases), and mortgages, we explore how Servicemembers are reflected and what, if any, trends are present...
---

## Introduction
This report presents an in-depth analysis of consumer complaints submitted to the Consumer Financial Protection Bureau (CFPB) over the past five years (1-1-2020 - 1-1-2025), with a particular focus on complaints tagged as 'servicemember.' The objective is to uncover patterns, trends, and unique challenges faced by servicemembers in the financial marketplace, using advanced data science and natural language processing techniques. The findings are intended for portfolio demonstration and professional presentation.

## Data Preparation and Segmentation
The dataset was rigorously cleaned to ensure accuracy and relevance. Complaints were segmented into two groups: those tagged as 'servicemember' and those from the general population. This separation enabled direct comparison and ensured that insights were specific to the experiences of servicemembers.

## Key Findings

### 1. Complaint Volume and Temporal Trends
- Servicemember complaints exhibit distinct seasonal patterns, with notable increases during the PCS (Permanent Change of Station) season (May to September).
- General complaint volume remains relatively stable, but servicemember complaints show spikes that align with periods of increased relocation and financial activity.

# ![Seasonal Trends](/assets/images/posts/complaint-analysis/complaint_seasonal.png)

### 2. Product and Issue Frequency
- The most common products associated with complaints include mortgages, credit cards, and vehicle loans or leases, servicemember or not. Therefore are the three products our analysis focuses on.
- Issue frequency analysis reveals that servicemembers are more likely to report problems related to loan servicing, payment processing, and account transfers compared to the general population.

# ![Issue Types](/assets/images/posts/complaint-analysis/complaint_type.png)

### 3. Comparative Analysis and Normalization
- When normalized for group size, certain issues and companies are disproportionately represented in servicemember complaints.
- Servicemembers report higher rates of specific issues per 100 complaints, highlighting areas where targeted consumer protection may be warranted.

# ![Company Comparisons](/assets/images/posts/complaint-analysis/complaint_issues.png)

### 4. Company-Level Insights
- A small number of financial institutions account for a significant share of servicemember complaints, particularly in mortgage and vehicle loan products.
- These companies may warrant further scrutiny or engagement to address recurring problems.

# ![Company Comparisons](/assets/images/posts/complaint-analysis/complaint_companies.png)

### 5. Narrative Analysis and Thematic Clustering
- Topic modeling and n-gram analysis of complaint narratives reveal recurring themes such as payment delays, account access issues, and customer service challenges.
- Semantic clustering using sentence embeddings and t-SNE visualization uncovers distinct groups of complaints, each characterized by unique language and concerns.
- Sample complaints from each cluster provide context and help define the main issues represented.

# ![Narrative Cluster](/assets/images/posts/complaint-analysis/complaint_cluster.png)

## Narrative Cluster Examples

## Cluster 0 sample complaints:
- I placed my mortgage into forbearance in XXXX oXXXX XXXX and missed 7 total payments. XXXX of XXXX was the beginning of XXXX and the forbearance guidelines were not fully established by any company. I...
- I was approved for tax exemption in XX/XX/2022, retroactively, the extra money that was paid for tax hasn't been returned to me. 

I caught XXXX in XX/XX/2022. I requested a forbearance due to other m...

## Cluster 1 sample complaints:
- The problem is with fraudulent charges that were made on my Ally XXXX  acct. ending in XXXX, in XXXX, XXXX, for {$14.00}, {$21.00}, {$19.00}, and {$18.00}, totaling {$73.00}, and on XX/XX/XXXX for {$1...
- To Whom it May Concern, I closed my account from your credit card company ( I was a card holder for 21 years ), when I first was a member, the interest rate was a fixed rate of 14 % ( estimated ), in ...

## Cluster 2 sample complaints:
- I filed a complaint with the CFPB in XXXX over this issue about the Goldman Sachs and Apple scam and Goldman lied and I have a note after their response in XXXX on the same website that they lied now ...
- Please attached. This company is engaged is some outlandish accounting and credit reporting actions. They have reported me as being late, and most egregious, have been charging me late charges every m...

## Cluster 3 sample complaints:
- I am disputing all of the debt the including the initial funding with Mercedes Benz Financial Services and the fact that my promissory note operates at lawful tender in the United States and I challen...
- Hello, my name is XXXX XXXX. I co-signed a loan with XXXX XXXX at a XXXX dealership. On XX/XX/XXXX, we opened a loan agreement with Chrysler Financial in the amount of {$33000.00}. It has an APR of 21...

## Cluster 4 sample complaints:
- We have a mortgage with Union Home Mortgage. It was a 5 % down mortgage with a balance of $ XXXX at closing. We understood that until we got our principal balance down to 78 % of LTV that we would hav...
- I have filed multiple complaints against this company, And they continue to not rectify the issues. I am going to continue to file a complaint and until I can get what I asked for over a year ago. I h...

## Cluster 5 sample complaints:
- I reached out to Mr.Cooper regarding an increase in my mortgage with a new monthly bill of {$2200.00} that was scheduled for XXXX via telephone on XX/XX/XXXX. There was an escrow shortage in the amoun...
- On XXXX I sent a letter to the XXXX along with documents from Wells Fargo and a spreadsheet showing a detailed list of every financial item from XX/XX/XXXX until XX/XX/XXXX. It was assigned complaint ...



## Detailed Findings

Over the past five years, servicemember complaints to the CFPB have revealed several distinct patterns and challenges compared to the general population:

- Seasonal Complaint Surges: Servicemember complaint volume shows pronounced increases during the PCS (Permanent Change of Station) season, indicating that financial stress and service disruptions are heightened during periods of relocation. This seasonal effect is not observed in the general population, underscoring the unique impact of military life on financial experiences.

- Product and Issue Concentration: Mortgages, credit cards, and vehicle loans or leases are the most frequently cited products in servicemember complaints. Within these categories, servicemembers disproportionately report issues related to loan servicing, payment processing, and account transfers. These issues often coincide with relocation events, suggesting that servicemembers face additional barriers when managing financial products during moves.

- Disproportionate Representation of Companies: A small number of financial institutions account for a significant share of servicemember complaints, especially in mortgage and vehicle loan products. These companies are repeatedly cited for problems such as delayed payments, misapplied funds, and poor customer service. The concentration of complaints suggests systemic issues that may require targeted regulatory attention.

- Comparative Issue Rates: When normalized for group size, servicemembers report higher rates of certain issues per 1,000 complaints than the general population. For example, complaints about payment processing and account access are notably more frequent among servicemembers, highlighting areas where consumer protection efforts could be strengthened.

- Narrative Themes and Clusters: Topic modeling and semantic clustering of complaint narratives reveal several recurring themes. Servicemember complaints often describe difficulties with timely payment posting, confusion over account status during relocations, and challenges in resolving disputes with financial institutions. Clustering analysis further identifies distinct groups of complaints, each characterized by specific language and concerns, such as relocation-related account problems or persistent customer service failures.

- Implications for Stakeholders: The findings indicate that servicemembers encounter unique financial challenges, particularly during relocation periods. Financial institutions should improve support and communication for military customers, especially during PCS season. Regulators may wish to monitor companies with high rates of servicemember complaints and consider targeted interventions to address recurring issues.

# ![Company Comparisons](/assets/images/posts/complaint-analysis/complaint_monthly.png)

---


