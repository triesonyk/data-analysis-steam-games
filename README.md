# data-analysis-steam-games

## Dataset Info

Dataset was acquired from steam using web scraping technique. The git repo can be access from [here](https://github.com/triesonyk/web-scraping-steam-games). The dataset was scrapped on 07 April 2022.

## Dataset Feature Definition

`title` = title of the game
`url` = url of the game on steam
`image` = url of the cover image of the game
`release_date` = release date of the game
`platform` = operating system and VR availibilty
`discount_rate` = discount given on the date the data scrapped
`original_price` = non-discounted price
`discounted_price` = price after discount
`developer` = companies that create and develop the game
`publisher` = companies that publish the game
`overall_reviews` = overall reviews categories (Positive, Negative, etc)
`text_reviews` = description of the reviews that contain user rating and total user that rate the game
`description` = brief summary of the game
`tags` = popular tags given to the game including genre of the game
`processor` = minimum CPU needed to run the game
`ram` = minimum ram needed to run the game
`graphic_card` = minimum GPU needed to run the game
`rating` = it should be rating by pegi but 
`language` = language supported by the game
`metacricts` = rating  by metacriticts

## Data Preprocessing for EDA

- All the data that I scraped was still in wrong dtype. So, the first thing I did was fix all the data type
- Drop duplicates
- Drop columns that can't be used for analysis
- Extracting `month` and `year` from release_date
- Extracting `user_rating` and `total_reviews` from `text_reviews`
- Turning language `language` into `supported_language`
- Extracting `price` from `original_price`
- Turning `rating` into `rated_by_pegi`
- Extracting `windows`, `mac`, and `linux` from `plaforms` (similar to one hot encoding)
- Remapping `ram` and `overall_reviews
- Turn `tags`, `developer`, and `publisher` into list
- Export new dataset into csv file

## EDA and Insight (Ongoing)
