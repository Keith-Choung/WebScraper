# WebScraper
scrapes sites for price drops

NOTES:

get_info -> check_price -> store_data & send_mail || do nothing

get_rows:
    gets the total number of rows in the csv file

get_info: 
    gets all information needed for an item, from the items.csv
        - input is row index that needs to be read in.
    return title, short_desc, converted_price

send_mail:
    sends the mail for a specific item
    return bool

check_price:
    reads the csv file and stores all of the prices in a list
    returns bool

store_data: Desc, Price, Date
    1) overwrites if check_price is true
    2) adds if the Desc does not exist yet
    returns bool

    
TODO:
- add ID column & create ID -> index translator map?

- add_data: returns boolean
    - calls create_ID()

- remove_data: if url returns nothing or DNE anymore

- send_mail() should be called last
    - needs to have all of the updated 

- check_price() should tell whether the price went up or down

- bs4 parsing test cases to ensure they UPDATE and don't add on

test cases

get_row(): returns the row number for the specific desc

create_ID(): if new item, creates an ID

organizing prices via price_list is unsustainable.
    - will need to sort by ID's
