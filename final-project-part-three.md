| [home page](README.md) | [data viz examples](dataviz-examples.md) | [critique by design](critique-by-design.md) | [final project I](final-project-part-one.md) | [final project II](final-project-part-two.md) | [final project III](final-project-part-three.md) |

# Final Project Part III: Same Basket, Different City

[Read the finished Shorthand story](https://carnegiemellon.shorthandstories.com/same-basket-different-city/index.html) · [See the Part II storyboard and interview notes](final-project-part-two.md) · [View the 32 price entries](part-two-grocery-prices.csv)

The question I started with is still the one I ask in the final story: if I take the same grocery list to another city, how much does the bill change? I compare eight foods in fixed quantities in Pittsburgh, New York, San Francisco and Seattle. For this list, the estimated total ranges from $23.44 in Pittsburgh to $30.29 in New York. The difference comes from particular foods; a higher total does not mean that every item costs more.

I chose these cities with MISM-BIDA students' post-graduation moves in mind, rather than at random. Pittsburgh represents staying near CMU; New York, San Francisco and Seattle reflect places graduates may move for work. I want classmates to get a feel for the price gap they might encounter when the same grocery list moves with them. This is an illustration, not an official destination ranking or a personal budget. The Numbeo pages were consulted on October 1, 2026; that is not a common collection date, and the estimates are not representative city-wide grocery prices.

## What changed after Part II

I kept the path from my original [Part I proposal](final-project-part-one.md): compare the total, look inside the basket, then ask what a fixed budget covers. Part I proposed USDA metropolitan-area data and considered a map and a time-series chart. In [Part II](final-project-part-two.md), I explained why I switched to Numbeo city entries: the USDA dataset did not cover three of the cities I wanted to compare. The four-city Numbeo snapshot also cannot support a broader geographic pattern or a price trend, so I left out the map and line chart. I did not combine the two sources. I made the shifts between the remaining questions more explicit. Before the food-group chart I say that it measures **extra dollars** relative to Pittsburgh. Before the item chart I say that it measures each food's **percentage difference** from its Pittsburgh price. Seattle's potatoes and chicken make the distinction concrete: potatoes have the larger percentage difference, while chicken adds more dollars to the bill.

Three CMU graduate students read the Part II draft. Their most consistent concern was the $25 chart. They could eventually explain 82.5% and 106.7%, but the chart did not immediately say what 100% represented. In the final story I drew a new budget chart with a percentage axis and a line labeled **“100% = one basket.”** I also explain that the percentages compare $25 with the full basket cost. They do not show what someone could literally put in a cart.

The Tableau receipt in Part II cut off long city names, so I rebuilt it as a table with full headings and the same eight prices. I also rebuilt the total, food-group, item and $25 comparisons with HTML and CSS in Shorthand. All five use the same prices and calculations as my Tableau drafts, which I link beside the final charts. This change made city names, units and the 100% line easier to read on desktop and phone. Short captions and source cautions sit beside the figures. The longer explanation of dates, formulas and data limitations comes after the main comparison.

Professor Christopher Goranson suggested a sample student story and a closer look at the budget. I added a short hypothetical scenario after the $25 chart about how I would check real store prices before planning a move.

## Who I made it for

I wrote first for CMU students and recent graduate classmates who buy groceries and are deciding where to live after CMU. Based on my experience of the program, these four cities reflect plausible places to stay or move; I did not use an official CMU placement dataset to rank them. Pittsburgh gives us a familiar starting point. Holding the eight-item list fixed helps us feel the scale of a price difference before making our own budgets. The three readers in Part II were women in CMU graduate programs, most of whom cook for themselves. Their responses helped me clarify the units, the Pittsburgh baseline and what 100% means in the $25 chart. Their comments are design feedback, not a representative survey.

## Design choices and what I learned

The basket stays fixed so the city comparison has a common denominator. It includes grains, vegetables, fruit, dairy and protein, but it is not a week's groceries or a complete diet. I used bars for comparing totals and dollar contributions, a dot plot for item percentages, a readable price table for exact lookup and a separate percentage chart for the $25 question. The category chart's tiny negative values are still hard to see at a glance; I explain the sign and give Seattle's milk as a concrete example rather than pretending the small mark is prominent.

Building the final page showed me how much a caption or axis label can change the reading of a chart. I had put the calculation in Part II prose, but P2 still had to pause at the budget percentages. Making “one basket” visible in the chart did more than another paragraph would have. I also learned to keep a limit next to the claim it qualifies, instead of asking readers to find it in a distant methods section.

The final story does not estimate what any particular student will spend. A stronger study would compare matching products at documented stores in each city, collect them during the same periods and repeat the collection over time. That evidence would support conclusions that this exploratory set of rolling estimates cannot.

## Sources and credits

The [Shorthand story](https://carnegiemellon.shorthandstories.com/same-basket-different-city/index.html#sources) links to the sources below. Its five final comparisons use the 32 listed price entries and my calculations. The Tableau links beside the charts show earlier drafts. The student scenario is hypothetical, not a participant quote.

- Grocery prices: Numbeo's [Pittsburgh](https://www.numbeo.com/cost-of-living/in/Pittsburgh), [New York](https://www.numbeo.com/cost-of-living/in/New-York), [San Francisco](https://www.numbeo.com/cost-of-living/in/San-Francisco) and [Seattle](https://www.numbeo.com/cost-of-living/in/Seattle) Markets tables, checked October 1, 2026. See also [Numbeo's methodology](https://www.numbeo.com/common/motivation_and_methodology.jsp) and my [item-level CSV](part-two-grocery-prices.csv).
- Photos: [SHVETS production](https://www.pexels.com/photo/man-in-white-t-shirt-holding-brown-paper-bag-8900035/) and [Ivan S](https://www.pexels.com/photo/a-woman-in-a-grocery-store-7990381/) on Pexels. I credit them beside the photos in Shorthand.
- Process: [Part I proposal](final-project-part-one.md) and [Part II storyboard and reader feedback](final-project-part-two.md).

I used ChatGPT/Codex to help edit wording.
