# Somerville Little Libraries: Data Analysis and Visualization

Scripts, data, and viz for a deep dive on Somerville little libraries.

## Data collection

Over a two week period in June, I visited 17 Somerville-area little 
libraries. At each library, I used the Libib app to catalog the library's 
collection by scanning barcodes, if present.

Once catalogued, I exported the Libib collection as a CSV. In 
`scripts/libib_data_generation.ipynb`, I used this CSV to build a more 
complete dataset of books using the Google Books and Open Library API.

From the Open Library API, I pulled information on each book's physical format, 
weight, revision number, and subject (a messy and ultimately unfruitful category 
that combined several genres with dashes).

From the Google Books API, I pulled category (a better proxy for genre), 
language, and public domain status.

Once the dataset was built, I exported it as a cleaned CSV for easy analysis and 
visualization: `data/little_libraries_books_2025_06_27.csv`.

## Analysis and Visualization

My analysis and visualization code can be found in 
`scripts/little_library_analysis_viz.qmd`.

At the outset of my analysis, I sought to answer the following questions. 

- When were most books published?
- Are there any popular authors?
- What are the most popular genres?
- Who are the most common publishers?
- How long are these books?
- How many are in the public domain?
- What are the most common languages?
- Are there trends in format (paperback vs. hardcover)?
- Which little libraries have the most books?

Ultimately, incomplete data limited my ability to tackle my 
questions around public domain status and book format, while a small sample 
size (191 books total) meant that conclusions around authors, language, and 
publishers didn't pop enough to be included in my final story. The remaining 
questions I answered in my piece.

## My findings

- Most books were published in the 2010s.  
- There were a few authors that had two books in the catalog, but nothing
noteworthy.  
- Fiction was the most popular genre. Biography and Young Adult/Juvenile 
fiction were common too.
- Vintage was the most common publisher with 6 books.
- Books were usually around 300 pages.  
- Most books were in English with some one-offs in French and German.  
- The Willoughby St library had the biggest collection with 21 books.
- Yes, there was a copy of the Girl with the Dragon Tattoo in one of the 
little libraries.

## New skills and approaches

I used this project to get more comfortable querying APIs in Python, 
experimenting with both the Google Books and Open Library APIs. 
With each book’s ISBN from Libib, I pulled data from both APIS to build a 
full dataset.

## If I had more time...

I’d initially considered building an interactive map to show each 
library’s collection (I was imagining a bubble map with a toolbar to explore 
the titles) but I ran out of time. I also wanted to add chart annotations
highlighting standout books, like the longest one by page count 
or the oldest by publication date etc. I'm hoping I'll be able to eventually add 
this last feature to help add some more life to the visualizations :)





