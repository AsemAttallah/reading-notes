# What are the key differences between scraping static and dynamic websites?

* 'A dynamic website is a type of website that can update or load content after the initial HTML load. So the browser receives basic HTML with JS and then loads content using received Javascript code. Such an approach allows increasing page load speed and prevents reloading the same layout each time you'd like to open a new page'.

* 'In contrast to dynamic websites, we can observe static websites containing all the requested content on the page load'.

* 'one of differences between scraping static and dynamic websites is : dynamic content make harder to extract data from such web pages, as it requires the execution of internal Javascript in the page context while scraping.'



# Explain at least three techniques or best practices that can be employed to avoid getting blocked while scraping websites.

* 'Respect Robots.txt : Web spiders should ideally follow the robot.txt file for a website while scraping. It has specific rules for good behavior, such as how frequently you can scrape, which pages allow scraping, and which ones you can’t. Some websites allow Google to scrape their websites, by not allowing any other websites to scrape. This goes against the open nature of the Internet and may not seem fair, but the owners of the website are within their rights to resort to such behavior'. 

* 'Do not follow the same crawling pattern: Humans generally will not perform repetitive tasks as they browse through a site with random actions. Web scraping bots tend to have the same crawling pattern because they are programmed that way unless specified. Sites that have intelligent anti-crawling mechanisms can easily detect spiders by finding patterns in their actions and can lead to web scraping getting blocked.
Incorporate some random clicks on the page, mouse movements and random actions that will make a spider look like a human'.

* 'Make the crawling slower, do not slam the server, treat websites nicely :Web scraping bots fetch data very fast, but it is easy for a site to detect your scraper, as humans cannot browse that fast. The faster you crawl, the worse it is for everyone. If a website gets too many requests than it can handle it might become unresponsive.
Make your spider look real, by mimicking human actions. Put some random programmatic sleep calls in between requests, add some delays after crawling a small number of pages and choose the lowest number of concurrent requests possible. Ideally, put a delay of 10-20 seconds between clicks and not put much load on the website, treating the website nice'.