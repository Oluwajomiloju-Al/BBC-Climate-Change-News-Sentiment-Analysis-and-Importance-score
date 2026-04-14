# BBC Climate Change Web Scraping & Text Analysis Project

## Project Overview
This project extracts and analyzes climate change-related articles from the BBC. It is divided into two main parts:

- **Part 1:** Web scraping using a modern browser automation tool  
- **Part 2:** Text analysis using natural language processing techniques  

The goal is to generate meaningful insights such as **sentiment, importance, and overall impact** of climate-related news.

---

# Part 1: Web Scraping

## Library Chosen: Playwright

### Why Playwright?
Playwright was selected over alternatives such as BeautifulSoup and Scrapy for the following reasons:

| Library | Strength | Limitation |
|--------|--------|-----------|
| BeautifulSoup | Simple and fast | Cannot handle JavaScript |
| Scrapy | Scalable | Complex setup |
| **Playwright** | Handles dynamic content | Slightly heavier |

BBC pages often include dynamic elements.  
Playwright ensures accurate and complete content extraction.

---

## Challenges Encountered

- Initial scraping captured non-relevant links (menus, categories, unrelated news)
- BBC structure includes mixed content and evolving URL formats

### Solution Implemented

A **hybrid filtering approach** was used:

1. **Broad link extraction**:
   - Captures all news links

2. **Content-based filtering**:
   - Filters articles using climate-related keywords:
     - climate, emissions, warming, energy, flood, wildfire, etc.

3. **Combined validation**
   - Uses both title + article text: to ensure relevance

---

## Data Collected

Each article includes:
- Title
- URL
- Full text content
