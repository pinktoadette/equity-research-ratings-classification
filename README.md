# Equity Research Ratings (Classification)

Every equity researcher examines a company's financial statement. Each statement maybe adjusted to reflect certain items (depending on the industry), such as adding back non-recurring items, adjustment for depreciation and amortization. Some of these adjustments are necessary and close attention to SEC filing on the footnotes is necessary.

With that in mind, is it possible to predict an earnings classification ratings based on financial statements and the researchers' output?

This notebook will analyze over 10 year CFRA reports with each quarterly filings.

### Process

* Find all equity research report and its corresponding financial statement reportings
* With domain knowledge, select necessary features on the 3 statements to determine what is necessary
* (future) SEC started providing footnotes. We will need to map the footnote ID to the company
The ratings are broken down into another feature called delt. This occurs when an analyst indicates a change in position. For example: "...maintain buy", "...upgrade from buy to strong buy", "... downgrade from strong buy to buy" etc.

### Word on Models
This model is simplified to first test out certain features.

* There are imbalance problems (of course!)
* Imbalance occurs when one class is significantly more or less than other.
* Test for 4 classification models (Logistic, gradient boost, random forest, decision trees)
