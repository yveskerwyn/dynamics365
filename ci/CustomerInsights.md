# Customer Insights

Get insights about **who** your customers are, or about **how** they are engaging with your business. 

Change your focus **at any time** by using the navigation menu:

![](images/ChooseYourFocus.png)

## Data Sources

- eCommerceContacts Extract of Customers who have made an online purchase: https://aka.ms/CI-ILT/Contacts 
- LoyaltyScheme Extract of Customers who’ve signed-up for the Contoso Retail Loyalty Card Scheme: https://aka.ms/CIILT/LoyaltySchemeCustomers 
- OnlinePurchases Extract of purchases made via the Contoso Retail Website: https://aka.ms/CIILT/OnlinePurchases 
- POSPurchases Extract of in-store purchase detail:https://aka.ms/CI-ILT/POSPurchases
- WebsiteReviews Online Website Reviews from online users: https://aka.ms/CI-ILT/WebReviews

## Data Ingestion

![](images/AddDataSource.png)

![](images/DataSourceCategories.png)

![](images/PowerQueryPreviewData.png)

![](images/PowerQueryEditQuery.png)

## Data Unification

![](images/Unify.png)

![](images/UnifySelectEntities.png)

Map fields to common model types:

![](images/Unify-Map.png)

Next we needs to set the match order:

![](images/Unify-Match.png)

![](images/Unify-Match-Order.png)

![](images/Unify-Match-MatchRulesNeeded.png)

Specify the match rules:

![](images/Unify-Match-Rule.png)

When you run the match process you get to see the number exact matches based on the rule(s) set:

![](images/Unify-Match-Run.png)

When you set the precision for full name to low you'll get more matches:

![](images/Unify-Match-RuleWithLowerPrecision.png)

![](images/Unify-Match-Run2.png)

To see the match results open the **Match preview** where you also see the **confidence score** for each match:

![](images/Unify-Match-Preview.png)

![](images/Unify-Match-Results.png)

You can also check the match preview per condition (criteria), here for instance for the FullName condition:

![](images/Unify-Match-Rule-Preview.png)

![](images/Unify-Match-Rule-CriteriaPreview.png)

The last step in the unification process is about reconciling conflicting data, which you do in the **Merge** step, allowing you to decide which version of the field should chosen and what the display will be in the merged profile, here for instance for the First Name field:

![](images/Unify-Merge.png)

![](images/Unify-Merge-Edit.png)


## Relationships

In order to create measure we first need to create relationships between the various entities.

![](images/Relationships.png)
![](images/Relationships2.png)


## Measures

By deleting the customer dimension, these changes the measure from a **customer measure** to a **business measure**:

![](images/Measure-Delete-Dimension.png)

In this business measure we calculate the average total spend per purchase:

![](images/Measure-AverageStorePurchase.png)

Here's an example of a customer measure:

![](images/Measure-TotalInStoreSpend.png)

You can review the measures under **Data** > **Entities**:

![](images/ReviewMeasures.png)

Click **Customer_Measure** here and then the **Data** tab:

![](images/CustomerMeasure.png)

![](images/CustomerMeasureData.png)

Back in the **Attributes** tab click the **Summaru** icon next to the **Total Club Points** measure:

![](images/OverviewOfTotalClubPoints.png)

## Segments

New dynamic segment from measure:

![](images/NewSegmentFromMeasure.png)

![](images/NewSegmentFromMeasure2.png)


New dynamic segment from blank:

![](images/NewSegmentFromBlank.png)

![](images/NewSegmentFromBlank2.png)

![](images/NewSegmentFromBlank3.png)

![](images/NewSegmentFromBlank4.png)

![](images/NewSegmentFromBlank5.png)

Review your segments:

![](images/ReviewSegments.png)

![](images/ReviewSummerPromotionSegment.png)

Segments can be exported:

![](images/ExportSegments.png)

## Segment Insights

Create a segment insight of type **Differentiator**:

![](images/SegmentInsights.png)

![](images/SegmentInsights2.png)

![](images/SegmentInsights3.png)

![](images/SegmentInsights4.png)

![](images/SegmentInsights5.png)

![](images/SegmentInsights6.png)

![](images/SegmentInsights7.png)

![](images/SegmentInsights8.png)

Create a segment insight of type **Overlap**:

![](images/SegmentInsightsOverlap.png)

![](images/SegmentInsightsOverlap2.png)

![](images/SegmentInsightsOverlap3.png)

## Segment Expansion

Segment Expansion can be used to find similar customers to your segment customer base using 
Artificial Intelligence. 

Earlier we created a segment called Summer Promotion which has millennial customers with 
higher than average instore purchase. Now, let us expand that segment and find customers that 
are similar to them for us to market our newly launched Cold Brew Coffee. 

![](images/SegmentExpansion.png)

![](images/SegmentExpansion2.png)

## Activities

![](images/CreateActivity.png)

![](images/CreateActivity2.png)

![](images/CreateActivity3.png)

![](images/CreateActivity4.png)

![](images/CreateActivity5.png)

See the result:

![](images/CreateActivity6.png)

## Data Enrichment

![](images/DataEnrichment.png)

![](images/DataEnrichment2.png)

![](images/DataEnrichment3.png)

![](images/DataEnrichment4.png)

![](images/DataEnrichment5.png)

![](images/DataEnrichment6.png)

Another one for interests:

![](images/DataEnrichment-Interest.png)

![](images/DataEnrichment-Interest2.png)

Review the result:

![](images/BrandEnrichment.png)

![](images/InterestsEnrichement.png)

![](images/DataEnrichmentOnProfile.png)
