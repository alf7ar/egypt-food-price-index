# Egypt food price index (weekly)

Weekly, aggregate-only index of ingredient prices that Egyptian restaurants buy, plus the food and restaurant searches rising in Egypt.

- `data/basket_index.csv`: basket and group level figures per week (index, week-over-week %, items on sale, mean discount). The first week is the baseline (index 100), so it has no change figures.
- `data/trends_rising.csv`: food queries rising in Google Trends (geo EG, last 7 days), filtered to dish and ingredient words.
- `data/YYYY-MM-DD.json`: the same figures per run.

**Not published on purpose:** per-product prices, product names, brands and images. Carrefour Egypt's terms restrict republishing site content, so only aggregates are shared here.

## How it is made

Data collected weekly with our open Apify actor: https://apify.com/alfhar/carrefour-price-tracker-mena
Search trends collected with our Google Trends actor: https://apify.com/alfhar/google-trends-scraper-pro

Disclosure: we (Alfhar Development, the team behind RestaurantOS, a restaurant management system for Egypt) built both actors and run this series. The basket is a fixed list of about 25 staple products, so week-over-week changes compare the same items. The weekly runs use a private build of the same actor code on our own Apify account.

Method: the week-over-week % for the basket and for each group is computed on the items that were priced in both weeks; the index chains these changes from the baseline week (100). Google Trends values are relative, not search counts.

Figures are for information only and are not financial advice.
