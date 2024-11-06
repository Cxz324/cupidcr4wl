<div align="center">
  
# Thank you for taking the time to contribute!

There are two main ways you can contribute platforms to add to the cupidcr4wl search list:
</div>

## The easy way:
Utilize the [issues](https://github.com/OSINTI4L/cupidcr4wl/issues) tab to fill out and submit the information. I will then do all the heavy lifting of checking that the platform can be crawled by cupidcr4wls' current code, check for accuracy, and format the platform information into the websites.json file.

## The hard way:
Utilize a pull request to directly submit code to the websites.json file.

If you choose this route, the json format must follow the following syntax:

```
         },
        "Name of Platform": {
            "url": "https://www.example.com/path/to/username/{username}",
            "check_text": [
                "html snippets of account page"
            ],
              "not_found_text": [
                "html snippets of no account page"
            ],
            "category": "the category of the platform"
```
