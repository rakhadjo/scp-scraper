# SCP Foundation Web Scraper
This is a web scraper for the SCP Wikidot website for SCP entities. Returns them in a JSON format (see schema below). To be used in tandem with my personal scp-api but feel free.

### TODO Next:
- Scrape the authors names and credits as well
- Add procedure to collect all addendums and documents to be stored in different json

### Requirements
- Jupyter Notebook (or Python should be fine)
- The `requests`, `bs4`, `json`, and `re` modules
- A will to live

### Get Started
Just initialize all the helper functions and then run the `scrape-scp` function which takes an ID of the entity you want returned. Can be used in a for loop for mass scraping.

### Scrape Schema
Currently scrapes and returns as follows:
```json
{
    "id": "str",
    "class:" "str",
    "containment": "str",
    "description": "str",
    "more_info": "json"
}
```
e.g.:

```json
{
    "id": "SCP-343",
    "class:" "Safe",
    "containment": "SCP-343 resides in a 6.1m by 6.1m (20 ft by..."
    "description": "CP-343 is a male, seemingly race-less, humanoid in...",
    "more_info": {
        "Addendum #343-1": "SCP-343, colloquially nicknamed...."
    }
}
```
