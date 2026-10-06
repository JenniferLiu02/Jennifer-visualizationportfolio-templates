| [home page](README.md) | [data viz examples](dataviz-examples.md) | [critique by design](critique-by-design.md) | [final project I](final-project-part-one.md) | [final project II](final-project-part-two.md) | [final project III](final-project-part-three.md) |

# Final Project Part II
# Same Basket, Different City
## An exploratory grocery-price comparison for students considering a move

I started this project with a simple question: how much would the same grocery list cost in another city? This draft brings together my five Tableau charts, the choices behind them and feedback from three CMU graduate students.

**Read this comparison as an illustration, not a city ranking.** Numbeo combines user contributions with manually collected information. Its rolling estimates are not official representative city averages or a uniform 2026 survey. October 1, 2026 is the date the pages were consulted, not a common observation date for all prices.

[Open the five-sheet Tableau workbook](https://public.tableau.com/views/Finalproject_17908994232220/Sheet1?:tabs=yes&:showVizHome=no) · [Download/view the 32 source entries](part-two-grocery-prices.csv)

**What I found:** This list costs $6.85 more in New York than in Pittsburgh. But a higher bill does not mean every food costs more: Seattle’s milk and San Francisco’s rice are slightly cheaper in these estimates.

**Reading path:** Start with the total bill → identify which groups add dollars → inspect the receipt → compare item-level percentages → translate the total into $25 of model basket coverage.

[Read the story](#wireframes--storyboards) · [Data and methods](#data-methods-and-reproducibility) · [Interview protocol](#user-research-protocol) · [Feedback and revisions](#interview-findings)

<details>
<summary>How I developed Part I and responded to feedback</summary>

### Development from Part I and instructor feedback

I kept the question from Part I: what happens to the bill when the shopping list stays the same? The story starts with the total, looks at the foods behind the difference and ends with what $25 covers. I developed the horizontal bar, stacked bar and dot-plot sketches from [Part I](final-project-part-one.md), with two refinements:

- The stacked chart now shows **category contributions to the difference from Pittsburgh**, rather than total category spending. This more directly answers “What creates the difference?”
- The dot plot now shows **individual foods as percentage differences from Pittsburgh**, making the baseline explicit while retaining the original city-comparison concept.

In Part I, I proposed using USDA Food-at-Home Monthly Area Prices, which covers 2012–2018 and does not include Pittsburgh, San Francisco or Seattle. For this draft, I switched to Numbeo city entries so I could explore these four cities. This changes the geography from USDA metropolitan areas to Numbeo city definitions; the two datasets are not combined.

Professor Christopher Goranson asked me to clarify the geographic scope and city-selection criteria and encouraged me to keep the basket definition simple. All four places here are **U.S. cities**. I chose them with my MISM-BIDA classmates' decisions after graduation in mind: Pittsburgh represents staying near CMU, while New York, San Francisco and Seattle reflect places graduates may move for work. This choice comes from my experience of the program, **not an official ranking of CMU destinations**. Comparable prices for all eight foods were available in these four cities. I want the comparison to give classmates a feel for a possible grocery-price gap after graduation; it does not represent all U.S. cities or predict anyone's bill.

When I asked about changing data sources, Professor Goranson emphasized making the limitations prominent, avoiding strong conclusions and considering what better data could reveal. I have therefore framed the story around patterns in these estimates, without treating them as predictions of student spending or recommendations about where to move. The basket uses major food groups; detailed calculations appear after the story.


</details>

## Wireframes / storyboards

I organized the sections below as a story that readers can follow from a familiar shopping list to a budget comparison. Each chart preview links to my interactive Tableau sheet. My original three sketches remain in Part I.

### 1. Same basket, same budget

Imagine taking the same small grocery list to four cities. Before comparing the bills, hold the quantities constant.

| Food group | Items and fixed quantities |
|---|---|
| Grains | White bread: one 1 lb loaf; white rice: 1 lb |
| Vegetables | Tomatoes: 1 lb; potatoes: 1 lb |
| Fruit | Apples: 1 lb |
| Dairy | Milk: 1 liter |
| Protein | Eggs: 12 large; chicken fillets: 1 lb |

I defined this eight-item basket as a simple comparison tool. It is not a weekly meal plan, a complete diet or a claim about what every student buys. It uses the source’s displayed quantities consistently across cities.

**Reader question:** If the list stays the same, how much do the estimated bills differ?

### 2. The basket stays the same. The bill does not.

[![Sorted horizontal bars comparing estimated eight-item basket totals in four cities](part-two-images/sheet-1.png)](https://public.tableau.com/views/Finalproject_17908994232220/Sheet1?:showVizHome=no)

*Figure 1. Estimated basket total in USD. Source: Numbeo city Markets tables, consulted October 1, 2026. Exploratory rolling estimates, not representative city averages.*

The list totals **$23.44 in Pittsburgh, $27.92 in San Francisco, $29.43 in Seattle and $30.29 in New York**. The bars are sorted to make the range easy to compare. This ordering applies to these eight quantities and estimates; a different list, retailer or sample could produce a different result.

New York’s bill is $6.85 higher. How much of that comes from eggs and chicken, and how much comes from the rest of the list?

### 3. Open the receipt: where does the extra cost come from?

[![Stacked bars showing food-group contributions to each city's basket-cost difference from Pittsburgh](part-two-images/sheet-2.png)](https://public.tableau.com/views/Finalproject_17908994232220/Sheet2?:showVizHome=no)

*Figure 2. Food-group cost differences from Pittsburgh, in USD. Positive segments add to the gap; negative segments reduce it. Protein includes only eggs and chicken. Source: Numbeo, consulted October 1, 2026. These are illustrative Numbeo estimates, not representative city-wide grocery prices.*

Relative to Pittsburgh, the **net** difference is **+$6.85 for New York, +$5.99 for Seattle and +$4.48 for San Francisco**. For New York and Seattle, eggs and chicken together contribute $3.31 and $3.00 respectively. In San Francisco, grains contribute $1.35, close to the $1.40 contribution from protein.

The chart shows which foods add to the gap; it cannot explain why stores charge different prices. A negative segment reduces the gap. Seattle’s milk, for example, is $0.04 cheaper than Pittsburgh’s.

[![Four-city receipt table with item quantities, individual estimates and basket totals](part-two-images/sheet-4.png)](https://public.tableau.com/views/Finalproject_17908994232220/Sheet4?:showVizHome=no)

*Figure 3. A reconstructed receipt comparison. All amounts are USD per stated quantity; these are not actual store receipts. Source: Numbeo, consulted October 1, 2026. These are illustrative Numbeo estimates, not representative city-wide grocery prices.*

The receipt shows the prices behind each total. Next I compare each food with its Pittsburgh price. That helps distinguish a small dollar change on a cheap item from a larger dollar change on an expensive one.

### 4. What actually costs more?

[![Dot plot of individual food-price percentage differences from Pittsburgh, with a zero-percent reference line](part-two-images/sheet-3.png)](https://public.tableau.com/views/Finalproject_17908994232220/Sheet3?:showVizHome=no)

*Figure 4. Percentage difference for the same food and quantity. Pittsburgh is the 0% baseline; each colored dot represents another city. Source: Numbeo, consulted October 1, 2026. These are illustrative Numbeo estimates, not representative city-wide grocery prices.*

The pattern varies by food. Seattle’s chicken estimate is about **48.3% higher** than Pittsburgh’s, while its milk estimate is about **3.3% lower**. San Francisco’s rice estimate is about **2.2% lower**. A higher total does not mean every item is more expensive.

**A bigger percentage does not necessarily mean more extra dollars.** For Seattle, compare:

| Food and quantity | Pittsburgh | Seattle | Extra dollars | Relative difference |
|---|---:|---:|---:|---:|
| Potatoes, 1 lb | $1.10 | $1.70 | +$0.60 | +54.5% |
| Chicken fillets, 1 lb | $5.72 | $8.48 | +$2.76 | +48.3% |

Potatoes have the larger percentage gap, but chicken adds more dollars to the bill. The percentage uses each food’s own Pittsburgh price as its denominator.

### 5. The geography of the grocery bill

The comparison includes Pittsburgh and New York in the eastern U.S. and San Francisco and Seattle on the West Coast. These locations give the audience concrete scenarios, but four selected city entries cannot establish a national or regional pattern.

In Part I, I considered a symbol map. I decided not to include it in this draft because four selected cities provide too little evidence for a broader geographic pattern. I explain the locations and selection criteria directly.

### 6. Prices also change over time — but this snapshot cannot show how

In Part I, I planned to include a time-series chart only if the data supported it. I do not have comparable repeated observations for this draft, so I have not drawn a trend line.

A stronger comparison would collect matching products and quantities at multiple documented stores in each city during the same periods, then repeat collection over time. It would also document store selection and variability. Such evidence could help distinguish persistent differences from changes in products, sample composition or collection dates.

Opening all four pages on the same day does not mean their prices were collected on the same day.

### 7. Same money, different basket

Now return to the shopping list. If I have $25 in each city, how much of this same list could that cover?

[![Horizontal bars showing the fraction of the selected basket covered by an illustrative 25-dollar budget](part-two-images/sheet-5.png)](https://public.tableau.com/views/Finalproject_17908994232220/Sheet5?:showVizHome=no)

*Figure 5. Model basket coverage with $25: Pittsburgh 106.7%, San Francisco 89.5%, Seattle 84.9%, New York 82.5%. On the current interactive axis, 1.0 means 100% of one basket. Source: Numbeo estimates and author calculations. These are illustrative Numbeo estimates, not representative city-wide grocery prices.*

| Coverage | What it means in this model |
|---|---|
| 100% (1.0 on the current axis) | Exactly one eight-item basket |
| Above 100% | More than one basket-equivalent; Pittsburgh reaches 106.7% |
| Below 100% | Less than one basket-equivalent; New York reaches 82.5%, or 17.5 percentage points short of a full basket |

The $25 amount is a round illustration budget near the sample totals, not a recommended grocery allowance. The model divides $25 by each city’s basket cost and scales all eight quantities proportionally.

The calculation scales every quantity together, including fractions. In practice, I cannot buy 82.5% of an egg carton: I would choose different items or packages. The chart compares the budget with the price of the list; it is not a shopping plan.

### 8. What this means for a budget

This exercise suggests a useful next step: write down the foods and quantities you actually buy, then check comparable products at the stores you would use in a prospective city.

Before using these numbers for my own budget, I would check the foods I actually buy at stores near where I might live. This small list cannot tell me which city I can afford; rent, income, transportation and my diet would matter too.

## Data, methods and reproducibility

<details>
<summary>Source data, formulas, units and detailed limitations</summary>

The public [item-level CSV](part-two-grocery-prices.csv) contains 32 rows: four cities × eight foods. Each row identifies the city, food and quantity, food group, USD estimate, source URL and consultation date. No missing prices were imputed. The source values are retained at their displayed precision.

For this basket:

- **Basket total:** sum the eight USD estimates within each city.
- **Category difference:** sum the category’s item prices in the city, then subtract the equivalent Pittsburgh category sum.
- **Relative item difference:** city item price ÷ Pittsburgh item price − 1. Format the result as a percentage.
- **Budget coverage:** $25 ÷ city basket total. Format the result as a percentage.

Amounts are rounded to cents for display and percentages to one decimal. The budget calculation permits fractional quantities. The displayed milk quantity is one liter; bread is a 1 lb loaf, the other listed weight-based foods are 1 lb, and eggs are 12 large.

All eight San Francisco entries were rechecked directly against the source page on October 1, 2026 and matched the draft; that page reported a September 30 update. Source-page verification confirms transcription, not the representativeness of the underlying estimates.

### Limits that affect interpretation

Numbeo combines crowdsourced and manually collected observations. Collection dates, contributors, retailers, brands and product characteristics differ. These are rolling estimates rather than matched-store observations from a uniform 2026 survey. The consultation date is not the date of every observation.

The data do not support statistical significance claims or confidence intervals for these basket differences. Numbeo’s displayed ranges are not treated as confidence intervals. City-wide contributor counts are not item-specific sample sizes. No causal explanation, universal city ranking, inflation trend or actual student-spending estimate is inferred.

</details>

### Method and medium

I created and published the five Tableau sheets and use this GitHub page as my Part II storyboard. I added captions and transitions to guide readers between the visualizations. As proposed in Part I, I plan to develop the final story in Shorthand, with each section focused on one question.

These are draft visualizations for Part II. In Part III, I plan to use the feedback below to improve the budget axis, receipt labels and small negative values. For this stage, I am using the charts to test whether readers can follow the story.

## User research protocol

### Target audience and recruitment

My intended audience is college students, graduate students and recent graduates who buy their own groceries and may move to another U.S. city. Readers should not need training in economics or data visualization.

I focused on CMU graduate students because they are part of the audience I want to reach and grocery spending is relevant to their daily lives. All three participants are women studying at CMU at the graduate level, and most cook for themselves. This is a small group of friends, so their responses help me spot confusing parts of the story rather than speak for all students.

Recruitment message: “I am testing a short grocery-price story for a class project. Would you be willing to spend about 15–20 minutes reading it and telling me what makes sense or feels confusing? Participation is optional, and I will report feedback anonymously.”

### Research goals

I want to learn whether readers understand the city selection, fixed quantities, dollar-versus-percentage comparisons, $25 model and source limitations. I also want to test whether the progression from totals to food differences to purchasing power feels coherent.

### Script for the chart review and follow-up

1. I will explain the activity and ask permission to take anonymous notes. I will only record audio with separate consent.
2. Opening script: “I am testing the story, not your knowledge. Please read it at your own pace and think aloud when something catches your attention or feels confusing. You can skip any question or stop at any time.”
3. I will let the participant read the storyboard and explore the charts, noting pauses, rereading and attempted interactions before offering explanations.
4. I will ask the prompts below and record the participant’s initial interpretation before clarifying anything.
5. I will close with: “What is the single most useful change I could make to this story?” Then I will thank the participant.

| Research goal | Neutral prompt / task | What to observe |
|---|---|---|
| Audience and selection | Who is this story for? Why do you think these four cities were chosen? | Whether readers infer a verified CMU ranking or national coverage |
| Basket meaning | What does this basket include? Does it describe a week of groceries? | Understanding of fixed quantities and illustrative scope |
| Total comparison | What does the first chart tell you? What does it leave unanswered? | Reading totals without generalizing to overall living costs |
| Difference decomposition | Explain one segment in the extra-cost chart. What would a negative segment mean? | Category versus item interpretation; positive versus negative contributions |
| Percent comparison | What does the 0% line mean? Does the largest percentage gap necessarily add the most dollars? | Distinction between relative differences and dollar contributions |
| Receipt clarity | Find one food’s price in two cities and check their quantities. | Legibility, units, column labels and whether readers mistake the table for a store receipt |
| Budget model | Explain 106.7% or 82.5% in your own words. How would real package purchases differ? | Meaning of one basket, fractional quantities and the $25 assumption |
| Evidence and limits | What does October 1, 2026 mean here? What would you need before using this to plan actual spending? | Distinguishing access date from observation date and recognizing source limits |
| Narrative | Where did you hesitate, lose the thread or want more explanation? | Transitions, reading order and missing context |

### How I recorded the feedback

I use P1–P3 instead of names. The findings below come from written responses, not a record of me watching each person use the charts. I quote the wording where available and summarize the rest. I compare the responses below and link the suggestions to the changes I plan to make.

## Interview findings

I collected feedback from three female CMU graduate students, whom I refer to as P1, P2 and P3. Most of them cook for themselves, so comparing grocery prices is relevant to their everyday lives. Their responses focused on different parts of the project: P1 on the explanations, P2 on understanding the $25 comparison and P3 on the chart details and reading order.

### P1: making the comparisons easier to follow

P1 understood the story’s main point but felt that I could do more to explain why each chart uses a different measure.

She understood that the price gap comes from particular foods, not every item becoming more expensive. Her concern was how quickly the story moves between totals, extra dollars, percentages and budget coverage.

Specific feedback:

- **Narrative transitions:** “the transition between them could be more explicit so readers immediately understand why they are moving from one measure to another.”
- **Dollars versus percentages:** The respondent warned that readers might mistake the largest percentage difference for the largest contribution to the total gap.
- **Budget interpretation:** She requested a visible 100% reference line and a percentage-formatted axis, with clearer explanations of values above and below 100%.
- **Limitations:** She recommended placing the central warning beside the main charts while reducing the amount of methodological information in the main reading path.

My friend organized the response around the main message, what the charts show and what could be improved. I treat the suggested misunderstandings as issues to test, rather than as mistakes I observed them making.

### P2: understanding what $25 covers

P2 first commented on the portfolio structure and suggested adding more concrete examples. I then asked her to look at the five charts and answer three questions about the story.

**1. What is the main story?**

P2 understood that I was comparing the same grocery basket across cities, using Pittsburgh as the baseline. She noticed that the charts move from total prices to the food groups and items behind the differences. She felt the $25 comparison made those differences easier to connect to everyday spending.

**2. What do 82.5% and 106.7% mean?**

P2 read 82.5% as the share of the New York basket that $25 would cover. She understood that $25 would cover the full Pittsburgh basket with some money left over, but had to think about the percentages before the meaning became clear:

> “the percentages were not immediately intuitive to me, especially because a value above 100% is a little unusual when thinking about a grocery basket.”

**3. Which part was hardest to understand, and what would you change?**

The $25 chart was the hardest part for P2:

> “I had to stop and figure out what 82.5% and 106.7% were percentages of.”

Her first choice was to label 100% as **one full grocery basket**. She also wanted the axis to use percentages instead of decimals.

This helped me see that the issue was not the calculation itself. P2 reached the intended interpretation, but the chart made her work to identify the reference point. I need to make that reference visible in the chart.

### P3: feedback on the story and five charts

P3 reviewed the story and all five charts, then answered the questions below. I have summarized her written feedback.

P3 could compare the totals and understood why some dots fall below Pittsburgh’s price. Her suggestions were more specific to the charts:

- Tiny negative contributions in the extra-cost chart are difficult to see.
- The receipt abbreviates city headings, which makes looking up prices harder.
- The budget chart mixes percentage labels with a decimal axis and needs a labeled 100% reference line.
- The geography and missing-time-series sections interrupt the transition from item prices to the $25 comparison; the reviewer suggests placing them after the main story.

<details>
<summary>P3’s answers to the interview questions</summary>

The table summarizes P3’s answers, including the parts they found clear and the details that slowed them down.

| Prompt | P3’s response |
|---|---|
| Audience and cities | Students or recent graduates considering a move; Pittsburgh is a CMU reference point, while the other cities are comparison examples rather than ranked destinations. |
| Basket | Eight foods in fixed quantities, not a week of groceries or a complete diet. |
| First chart | Totals range from $23.44 in Pittsburgh to $30.29 in New York; they do not predict personal spending or establish overall affordability. |
| Extra-cost chart | New York’s eggs and chicken contribute $3.31 more than Pittsburgh’s; a negative category reduces the gap. |
| Zero-percent line | The same estimated item price as Pittsburgh; a larger percentage gap does not necessarily add more dollars, as the potatoes-and-chicken example shows. |
| Receipt | Chicken is 1 lb in both Pittsburgh ($5.72) and Seattle ($8.48). P3 reported that the shortened city headings slowed the lookup. |
| $25 chart | 82.5% means that share of one model basket; 106.7% means slightly more than one. Actual purchases depend on whole packages and item choices. |
| Date and evidence | October 1 is the consultation date, not a common collection date. A practical budget needs local products, stores and personal shopping habits. |
| Story flow | The written dollar-versus-percentage example helps, but the distinction should be clearer within the visualizations themselves. |

**P3’s main suggestion:** Format the $25 chart’s axis as percentages and add a labeled 100% line so the closing comparison makes sense without the explanatory table.

</details>

### What I learned from the feedback

All three readers asked for a clearer 100% reference in the budget chart. P2’s follow-up made the problem especially clear: she understood the percentages eventually, but first had to work out what counted as 100%. This makes a labeled “one full grocery basket” line my first priority.

P1 and P3 also wanted clearer transitions between extra dollars and percentage differences. P2 understood the overall sequence and felt the $25 chart made the comparison more practical. These responses do not directly conflict: readers could follow the main story while still finding an individual chart hard to read.

P3 pointed out details the others did not mention, including the shortened city names in the receipt and the tiny negative segments in the extra-cost chart. P2’s earlier request for concrete examples supports keeping the potatoes-and-chicken comparison.

The main lesson for me is that the story makes sense, but some of the charts still need the surrounding text to explain them. In the next version, I want the units, reference points and labels to do more of that work.

## Identified changes for Part III

I have already added clearer transitions, the potatoes-and-chicken example and short source notes beside each chart. I also moved the detailed methods into an expandable section. Based on the feedback, these are my next changes:

| Feedback | What I will change |
|---|---|
| P1, P2 and P3 asked for a clearer budget reference; P2 had to work out what the percentages were of | Format the $25 axis as percentages and add a labeled **100% = one full grocery basket** line. |
| P1 and P3 wanted the difference between dollars and percentages to be clearer | Keep the worked example and give the two charts short subtitles stating which measure they use. |
| P3 found the receipt headings hard to read | Widen the columns so Pittsburgh and San Francisco appear in full. |
| P3 found the small negative segments difficult to see | Add value labels or short annotations without changing their scale. |
| P3 felt the geography and time-data sections interrupted the story | Move those discussions after the $25 comparison, while keeping the main source limitation beside each chart. |
| P1 wanted the main limitation closer to the charts | Keep the brief Numbeo caveat with each figure and the longer explanation in the methods section. |

After making these changes, I want to check whether readers can explain the budget chart without first reading the paragraph underneath it.

## References

- [Numbeo: Pittsburgh cost of living — Markets](https://www.numbeo.com/cost-of-living/in/Pittsburgh). Consulted October 1, 2026.
- [Numbeo: New York cost of living — Markets](https://www.numbeo.com/cost-of-living/in/New-York). Consulted October 1, 2026.
- [Numbeo: San Francisco cost of living — Markets](https://www.numbeo.com/cost-of-living/in/San-Francisco). Consulted October 1, 2026.
- [Numbeo: Seattle cost of living — Markets](https://www.numbeo.com/cost-of-living/in/Seattle). Consulted October 1, 2026.
- [Numbeo methodology](https://www.numbeo.com/common/motivation_and_methodology.jsp).
- [USDA ERS: Food-at-Home Monthly Area Prices](https://www.ers.usda.gov/data-products/food-at-home-monthly-area-prices). Original Part I source; not used in the current numerical comparison.
- [Jennifer Liu: Final Project Part I](final-project-part-one.md).
- [Jennifer Liu: Published Tableau workbook](https://public.tableau.com/views/Finalproject_17908994232220/Sheet1?:tabs=yes&:showVizHome=no).
- 94-870 Telling Stories with Data: Part II assignment instructions and feedback from Professor Christopher Goranson.

## AI acknowledgements

I used ChatGPT/Codex to help polish wording and give me suggestions.
