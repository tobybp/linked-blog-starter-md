[[Computing]]  
#21/3/26
# Functional Programming – Big Data

## What is Big Data?
- **Big Data** refers to data that is:
    - too large to be processed on a single server
    - often **unstructured**
- It is difficult to store, process, and analyse using traditional methods

---
## Examples of Big Data use
- Organisations that collect and analyse Big Data:
    - NHS → patterns in illness/injury
    - Passport control → border crossing patterns
    - Police / GCHQ → security analysis
    - CCTV systems → monitoring activity
---
## Google Flu Trends (GFT)
- Used search data to predict flu outbreaks
- Initially more accurate than official data
- Later became less reliable because:
    - user behaviour changed
    - media coverage affected searches
- Shows Big Data analysis can be **complex and unreliable**

---
## Unstructured data
- Big Data is often **unstructured** and “fuzzy”
- Same word can have multiple meanings
Example:
- “smoking” could mean:
    - cigarettes
    - cooking food
    - slang meaning

---
## Finding patterns
- Big Data is used to:
    - identify patterns
    - make predictions
- Example:
    - online shopping recommendations

---
## Characteristics of Big Data (3 Vs)
### Volume
- Extremely large amounts of data
- Too big for one server
Examples:
- billions of card transactions
- billions of search queries per day

---
### Velocity
- Data is generated **very quickly**
- Often needs real-time processing
Examples:
- smartphones
- sensors
- CCTV

---
### Variety
- Data comes in many formats:
    - structured
    - unstructured
    - text, images, audio
Examples:
- social media posts
- videos
- photos

---
## Big Data and functional programming
- Big Data is often processed across **multiple servers (distributed systems)**
- Functional programming is useful because it supports this

---
## Features of functional programming for Big Data
### Immutable data
- Data cannot be changed
- Prevents accidental modification

---
### Statelessness
- Functions do not depend on previous states
- Order of execution does not matter

---
### Higher-order functions
- Functions like:
    - `map`
    - `fold`
- Can be passed around and reused

---
## Map and reduce (fold)
### Map
- Applies a function to every element in a list
- Returns a **new list**
Example:
	map (+5) [1,2,6] → [6,7,11]

---
### Fold (reduce)
- Combines a list into a single value
- Uses recursion
Example:
	foldl (+) 0 [2,3,4,5] → 14

---
## Parallel processing
- `map` and `reduce` can be:
    - split across multiple processors
    - run at the same time
- Improves efficiency for large datasets

---
## Fact-based model
- Represents data as **individual facts**
Examples:
- location = coordinates
- product = stock ID
- employer = organisation
- Useful for flexible, large datasets

---
## Graph schema
- Used to represent **relationships between data**
- Data is stored as:
    - **nodes** → entities
    - **edges** → relationships

---
## Example uses of graph schema
- Finding:
    - employees with specific skills
    - relationships between people
    - connections in organisations

---
## Social networks
- Social media is a good example of Big Data graphs
- Tracks relationships between users

---
## Nodes and edges
- Node → a person or object
- Edge → a connection (e.g. friendship)

---
## Six degrees of separation
- Idea: any two people are connected by a small number of links
- Large-scale data analysis supports this concept