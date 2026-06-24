# Customer Behavior & Trends Analytics



Why I built this
I wanted to work through the kind of problem a data analyst actually faces at a company — not just clean a dataset and make a chart, but answer a real business question from scratch.
The question I picked: which customers should a retail brand prioritise for its next marketing campaign, and why?
That meant going from messy transaction records all the way to a dashboard a non-technical stakeholder could actually use — defining the problem, wrangling the data, writing SQL to segment customers, and building something visual at the end. The full loop.

What I found
The most interesting result wasn't what I expected going in. Young adults (18–24) turned out to be the highest revenue-generating demographic — not because they spend more per order, but because they buy more frequently. That distinction matters for campaign strategy: you don't win them with premium pricing, you win them with repeat-purchase incentives and discount-led offers.
A few other things that stood out:

Loyal customers make up roughly 15% of the customer base but account for nearly 40% of total revenue — the classic pattern, but useful to quantify with actual numbers
The Online channel drives around half of all transactions, which makes a strong case for digital-first campaign spend
Electronics and Home & Kitchen consistently outperform other categories across almost every demographic segment


How I approached it
I started in Python — loaded the raw data, explored distributions, and engineered the features I'd need downstream: age-group segments using pd.cut(), order-count-based cohort labels, and encoded categoricals for SQL compatibility.
The SQL layer is where the segmentation logic lives. I used window functions to rank customers within categories, CTEs to keep the cohort classification readable, and an RFM scoring model to prioritise customers by recency, frequency, and spend. All queries are SQLite-compatible so anyone can run them without a database server.
The final Power BI dashboard has five pages — executive summary, demographic breakdown, category performance, RFM segments, and a geographic view — with dynamic slicers so the marketing team can filter by year, channel, city, or cohort without touching the data.


python sql pandas data-analytics power-bi customer-segmentation rfm-analysis sqlite exploratory-data-analysis retail-analytics
