# RSSScrape

## What ?
```
Feature: Consume a RSS feed from site A and present onto site B.
Given that I have no pussy on my web site
When I consume a atom/rss feed about pussy from the following source
| Blog Url                           |
| http://www.yourcat.co.uk/Your-Cat/ |
And I visit a page on my web site in the style of
| Template Url                              |
| http://sartre.thememountain.com/blog.html |
Then I see a blog about pussy on my web site
```
## How ?
1. Create "Public" DropBox folders
2. Saved contents of "http://sartre.thememountain.com/blog.html" locally. (Manually added font file as Chrome Save feature not as good as it thinks :-))
3. Created a GitHub repository, sync'd to DropBox folder
4. Add references in blog.html to:
 * Javascript RSS feed client (https://github.com/sekando/feednami-client)
 * Date formatting library (https://github.com/moment/moment)
5. Modified blog.html to include feednami-client 
6. Removed ".grid-item" elements from blog.html
7. Added script in blog.html to consume feed, and append blog entries, replacing key data parts. (The CSS class `grid-sizer is important to the styling of the original blog page so was added.)
8. Re-call isotope to reset grid.
9. Add a warning message if feednami-client fails to load the feed.
10. Sync Dropbox folder to GitHub

Worth nothing:
* Like button - I've left the "like" link (and display of likes)
* Image sizes - I've used the feed from the BBC because the original feed refers to images that are not really sized adequately for display.
* HTML Templating - Perhaps the use of handlebars or some other templating library can be used instead of naive string manipulation.

## License
RSSScrape is licensed under The MIT License (MIT).