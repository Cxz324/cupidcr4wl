<div align="center">
  
# 🌟 Thank you for taking the time to contribute! 🌟

>**NOTE:** Not all platforms are able to be crawled by cupidcr4wl. Some platforms may produce html code that is identical accross different pages, thus the changes being rendered via Javascript. These pages are unable to be crawled by cupidcr4wl code. If you are contributing via a pull request, please test the site prior to creating the pull request for false positives/negatives. This can be done by searching a random string of characters "safgdh543g24" and a known good account name "john". The random string of characters should return no results and the known good account should be listed. You can also use ```--debug``` mode to receive more detail about what is *actually* happening in cupidcr4wls' code during a search.

There are two main ways you can contribute platforms to add to the cupidcr4wl search list:
</div>

## The easy way:
Utilize the [issues](https://github.com/OSINTI4L/cupidcr4wl/issues) tab to fill out and submit the information. I will then do all the heavy lifting of checking that the platform can be crawled by cupidcr4wls' current code, check for accuracy, and format the platform information into the websites.json file.

## The hard way:
Utilize a pull request to directly submit code to the [websites.json file](https://github.com/OSINTI4L/cupidcr4wl/blob/main/websites.json).

If you choose this route, the json format must follow the following syntax:

```
         },
        "Name of Platform": {
            "url": "https://www.example.com/path/to/{username}",
            "check_text": [
                "html snippets of account page"
            ],
              "not_found_text": [
                "html snippets of no account page"
            ],
            "category": "the category of the platform"
```

### Platform
Enter the name of the platform that cupidcr4wl will search:
```
},
        "Name of Platform": {
```

### URL
Enter the URL path to an account or search:

```"url": "https://www.example.com/path/to/{username}",```

### check_text
The ```check_text``` and ```not_found_text``` feature in cupidcr4wl parses the html of the pages it searches to look for specific html code snippets present on a valid account page. This helps with the accuracy of the tool. To parse html code,
1. Go to a valid account page.
2. Right click > View Page Source.
3. Parse and list html code that is present **ONLY** on a **VALID** account page and not a non-valid account page (spoken about next).

List this information in the ```"html snippets of account page"``` section.

Multiple html snippets can be added to this section using commas:

```
"check_text": [
  "followers",
  "subscribe",
  "profile"
],
```

### not_found_text
Inversely, not_found_text are html code snippets that are **NOT** found on a valid account page.
1. Find an invalid account page by adding a string of random characters in the username area of the url e.g., ```https://example.com/sdf4657u66h4g3```.
2. You will be redirected to an "account not found page". This could be a redirection back to the landing page of the platform or a dedicated "404/page not found/we're sorry" page.
3. Parse and list html code that is present **ONLY** on a **NON-VALID** account page.

Multiple html snippets can be added to this section using commas:
```
"not_found_text": [
  "404",
  "page not found",
  "sorry that profile doesn't exist"
],
```

You can see examples of html parsed code snippets used for the purposes of ```check_text``` and ```not_found_text``` in the [websites.json](https://github.com/OSINTI4L/cupidcr4wl/blob/main/websites.json) file.

### Category
Finally, add the category type so that cupidcr4wl will display results to their respective categories.
The current categories are:
```
"dating, hook-up, and social"
"adult video, photo, and camming"
"escort"
```
