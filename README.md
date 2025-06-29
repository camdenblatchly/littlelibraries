# Somerville Little Libraries: Data Analysis and Visualization

Scripts, data, and viz for a deep dive on Somerville little libraries.

## Data collection

Over a two week period in June, I visited 15 plus Somerville-area little 
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
visualization.

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
size (172 books total) meant that conclusions around authors, language, and 
publishers didn't pop enough to be included in my final story. The remaining 
questions I answered in my piece.

## My findings

- Most books were published in the 2010s.  
- There were a few authors that had two books in the catalog, but nothing
noteworthy.  
- Fiction was the most popular genre. Biography and Young Adult/Juvenile 
fiction were common too.
- Vintage was the most common publisher with 6 books. Penguin was second with 4.
- Books were usually around 300 pages.  
- Most books were in english with some one-offs in french and german.  
- The Willoughby St library had the biggest collection with 21 books.

## New skills and approaches

I wanted to use this project to get more familiar with querying APIs using 
Python. As such, I was excited to work with the Google Books and Open 
Library APIs. Once I had the book's ISBN from Libib, I was able to query both 
APIs to create a full dataset.

## If I had more time...

Initially, I thought this project would give me a chance to create an 
interactive map to display the contents of each collection. In the end, I 
ran out of time, but I think a slippy bubble map with a toolbar that 
displayed each libraries' contents would be cool!





