# Google Dorking Cheatsheet

| **Dork**                         | **Description**                                                                 | **Example**                              |
|-----------------------------------|---------------------------------------------------------------------------------|------------------------------------------|
| `site:`                           | Search within a specific site or domain.                                        | `site:example.com`                      |
| `intitle:`                        | Search for pages with specific words in the title.                              | `intitle:"admin"`                        |
| `inurl:`                          | Search for specific keywords in the URL.                                        | `inurl:login`                           |
| `filetype:`                       | Search for specific file types.                                                 | `filetype:pdf`                          |
| `intext:`                         | Search for a word or phrase in the body text of the page.                       | `intext:"confidential"`                 |
| `cache:`                          | View Google's cached version of a page.                                         | `cache:example.com`                     |
| `allintitle:`                     | Search for multiple words in the title.                                        | `allintitle:"login" "admin"`            |
| `allinurl:`                       | Search for multiple keywords in the URL.                                        | `allinurl:"admin" "login"`              |
| `allintext:`                      | Search for multiple keywords in the body of the page.                           | `allintext:"password" "admin"`          |
| `related:`                        | Find sites related to a specific URL.                                           | `related:example.com`                   |
| `link:`                           | Find pages that link to a specific URL.                                         | `link:example.com`                      |
| `define:`                         | Search for the definition of a word or phrase.                                  | `define:phishing`                       |
| `location:`                       | Find pages related to a specific geographic location.                          | `location:"New York"`                   |
| `ext:`                            | Search for specific file extensions.                                           | `ext:zip`                               |
| `inanchor:`                       | Search for specific words in anchor text (links).                               | `inanchor:"click here"`                 |
| `allinanchor:`                    | Search for multiple keywords in anchor text.                                    | `allinanchor:"login" "admin"`           |
| `numrange:`                       | Search within a specific range of numbers.                                      | `numrange:100..500`                     |
| `intitle:index.of`                | Find directory listings or indexes on a website.                               | `intitle:index.of mp3`                  |
| `inurl:wp-admin`                  | Search for WordPress login pages.                                               | `inurl:wp-admin`                        |
| `inurl:wp-login.php`              | Find WordPress login pages.                                                     | `inurl:wp-login.php`                    |
| `filetype:xls inurl:"password"`   | Search for Excel files (.xls) that contain the word "password" in the URL.      | `filetype:xls inurl:"password"`         |
| `filetype:sql intext:"dump"`      | Find SQL dump files with the word "dump".                                       | `filetype:sql intext:"dump"`            |
| `inurl:admin intext:"password"`   | Find admin login pages with the word "password" in the text.                    | `inurl:admin intext:"password"`         |
| `intitle:"index of" "backup"`     | Find backup file directories.                                                  | `intitle:"index of" "backup"`           |
| `inurl:"/cgi-bin/"`               | Find CGI scripts on websites.                                                   | `inurl:"/cgi-bin/"`                     |
| `inurl:"/cgi-bin/" "admin"`       | Find admin CGI scripts.                                                        | `inurl:"/cgi-bin/" "admin"`             |
