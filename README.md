<div align="center">

# 💘 cupidcr4wl 💘
cupidcr4wl is an Open-Source Intelligence username search tool that crawls adult content platforms to see if a targeted account or person is present. The need for a tool of this manner derived from missing persons investigations where dating platforms and concerns of human trafficking were found relevant.

cupidcr4wl searches the following platforms:

**Adult photo, video, and camming platforms | Dating, hook-up, and social platforms | Escort service platforms**

If you find cupidcr4wl is returning false positives/negatives, please submit the relevant information in the [issues](https://github.com/OSINTI4L/cupidcr4wl/issues) tab so it can be fixed. You can also submit a pull request, please read the [contributing](https://github.com/OSINTI4L/cupidcr4wl/blob/main/.github/CONTRIBUTING.md) section to see how to do this.

The site list that cupidcr4wl utilizes for searching is updated for accuracy and added to regularly.

⚠️**WARNING**⚠️ 

cupidcr4wl **will** search and return results for platforms that host content for mature adult audiences. You are expected to use this tool in accordance with the laws and regulations in your respective location.

## [Installation](#installation) | [Usage](#usage) | [Contributing](https://github.com/OSINTI4L/cupidcr4wl/blob/main/.github/CONTRIBUTING.md)

![demogifcomp](https://github.com/user-attachments/assets/e2853512-6fae-4b01-a173-b25995a2de69)

</div>

## Installation

1) Clone the repository:

&nbsp;&nbsp;&nbsp;&nbsp;```git clone https://github.com/OSINTI4L/cupidcr4wl```


2) Change directories to cupidcr4wl:

&nbsp;&nbsp;&nbsp;&nbsp;```cd cupidcr4wl```


3) Install the requirements:

&nbsp;&nbsp;&nbsp;&nbsp;```pip install -r requirements.txt```

## Usage
1) To see all cupidcr4wl command line arguments:

&nbsp;&nbsp;&nbsp;&nbsp;```python3 cc.py -h``` or ```python3 cc.py --help```

```
usage: cc.py [-h] [-u USERNAME] [--export-results] [--debug] [--sites]
A tool for checking if an account exists across various websites.
options:
  -h, --help        show this help message and exit
                    
  -u USERNAME       Enter a username or multiple usernames (separated by commas) to search.
                    
  --export-results  Search results will be exported to a text file named 'cc_results.txt'.
                    
  --debug           Debug mode, shows HTTP response codes and check_text/not_found_text
                    matches for each site checked.
                    
  --sites           Print all sites that cupidcr4wl will check.
```
2) To perform a search of a username:

&nbsp;&nbsp;&nbsp;&nbsp;```python3 cc.py -u username```

3) To perform a search of multiple usernames:

&nbsp;&nbsp;&nbsp;&nbsp;```python3 cc.py -u username1,username2,username3```

4) To export a copy of the search results to a text document:

&nbsp;&nbsp;&nbsp;&nbsp;```python3 cc.py -u username --export-results```

&nbsp;&nbsp;&nbsp;&nbsp;The results will be saved as cc_results.txt in the current working directory.

5) To view a list of all sites that cupidcr4wl will search:

&nbsp;&nbsp;&nbsp;&nbsp;```python3 cc.py --sites```

6) To run cupidcr4wl in debug mode to test for false positives/negatives:

&nbsp;&nbsp;&nbsp;&nbsp;```python3 cc.py -u username --debug```

&nbsp;&nbsp;&nbsp;&nbsp;(More can be read on this mode in the wiki documentation)
