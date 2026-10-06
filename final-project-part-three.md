| [home page](README.md) | [data viz examples](dataviz-examples.md) | [critique by design](critique-by-design.md) | [final project I](final-project-part-one.md) | [final project II](final-project-part-two.md) | [final project III](final-project-part-three.md) |

# Final Project Part III: Same Basket, Different City

[Read the finished Shorthand story](https://carnegiemellon.shorthandstories.com/same-basket-different-city/index.html) · [See the Part II storyboard and interview notes](final-project-part-two.md) · [View the 32 price entries](part-two-grocery-prices.csv)

The question I started with is still the one I ask in the final story: if I take the same grocery list to another city, how much does the bill change? I compare eight foods in fixed quantities in Pittsburgh, New York, San Francisco and Seattle. For this list, the estimated total ranges from $23.44 in Pittsburgh to $30.29 in New York. The difference comes from particular foods; a higher total does not mean that every item costs more.

This is a small illustration for students considering a move, not a ranking of affordable cities. The figures use Numbeo estimates from pages I consulted on October 1, 2026. That date is not a common collection date, and the estimates are not representative city-wide grocery prices. I say this near the first chart and again with the sources.

## What changed after Part II

I kept the path from my original [Part I proposal](final-project-part-one.md): compare the total, look inside the basket, then ask what a fixed budget covers. Part I proposed USDA metropolitan-area data and considered a map and a time-series chart. In [Part II](final-project-part-two.md), I explained why I switched to Numbeo city entries: the USDA dataset did not cover three of the cities I wanted to compare. The four-city Numbeo snapshot also cannot support a broader geographic pattern or a price trend, so I left out the map and line chart. I did not combine the two sources. I made the shifts between the remaining questions more explicit. Before the food-group chart I say that it measures **extra dollars** relative to Pittsburgh. Before the item chart I say that it measures each food's **percentage difference** from its Pittsburgh price. Seattle's potatoes and chicken make the distinction concrete: potatoes have the larger percentage difference, while chicken adds more dollars to the bill.

Three CMU graduate students read the Part II draft. Their most consistent concern was the $25 chart. They could eventually explain 82.5% and 106.7%, but the chart did not immediately say what 100% represented. In the final story I drew a new budget chart with a percentage axis and a line labeled **“100% = one basket.”** I also explain that the model scales quantities proportionally; it does not describe what someone could literally put in a cart.

The Tableau receipt in Part II cut off long city names, so I rebuilt it as a table with full headings and the same eight prices. I kept the interactive Tableau charts for the total, food-group and item comparisons, but gave them more room on the Shorthand page. Short captions and source cautions sit beside the figures. The longer explanation of dates, formulas and data limitations comes after the main comparison.

Professor Christopher Goranson suggested a sample narrative or persona and thinking about resources for CMU graduate students. I added a brief hypothetical student decision after the $25 chart: what I would check before using these numbers to plan a move. I also link to the [CMU Pantry](https://www.cmu.edu/student-affairs/resources/cmu-pantry/) as a resource for students who need supplemental food while at CMU. Neither addition turns the basket into a meal plan or changes the price calculations.

## Who I made it for

I wrote for CMU students and recent graduates who buy groceries and may move to another U.S. city. Pittsburgh is the familiar reference point. The other three cities are examples with matching food entries; I do not claim they are the most common CMU destinations. The three readers in Part II were women in CMU graduate programs, most of whom cook for themselves. Their responses helped me make the units, reference point and reading order clearer. They are useful design feedback, not a representative survey of students.

## Design choices and what I learned

The basket stays fixed so the city comparison has a common denominator. It includes grains, vegetables, fruit, dairy and protein, but it is not a week's groceries or a complete diet. I used bars for comparing totals and dollar contributions, a dot plot for item percentages, a readable price table for exact lookup and a separate percentage chart for the $25 question. The category chart's tiny negative values are still hard to see at a glance; I explain the sign and give Seattle's milk as a concrete example rather than pretending the small mark is prominent.

Building the final page showed me how much a caption or axis label can change the reading of a chart. I had put the calculation in Part II prose, but P2 still had to pause at the budget percentages. Making “one basket” visible in the chart did more than another paragraph would have. I also learned to keep a limit next to the claim it qualifies, instead of asking readers to find it in a distant methods section.

The final story does not estimate what any particular student will spend. A stronger study would compare matching products at documented stores in each city, collect them during the same periods and repeat the collection over time. That evidence would support conclusions that this exploratory set of rolling estimates cannot.

## Sources and credits

The [Shorthand story](https://carnegiemellon.shorthandstories.com/same-basket-different-city/index.html#sources) links to the four Numbeo city pages, Numbeo's methodology, the CMU Pantry page, the item-level CSV and the Part II research notes. The Tableau workbook and the revised $25 chart use those 32 listed price entries and my calculations. I used no external photos or illustrations. The story includes a hypothetical student scenario, clearly labeled as such; it is not a participant quote.

I used ChatGPT/Codex to help edit wording.
