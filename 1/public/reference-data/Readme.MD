## Reference Data 'Standard Library'

Read the blog over at https://raw-labs.com/blog/reference-data-standard-library/

Inspired by Financial Services organisations, who have central reference (static) data 
which is reused many times, we have created this example showing how RAW can create
base reference data to serve as building blocks for other types of data product.

Currently there are APIs for Geography (Countries, Regions), Languages and Currencies but this can
expand to include other types of highly reusable data.

Data comes from a variety of authoritative data sources, well maintained open and free. (XML, CSV and TSV data)

Moreover this is being used to show how RAW can create a whole series of endpoints within and 
across domains - for instance supporting a Data Mesh concept. 


This can be used as an example of how to properly structure raw data to produce an API 
that is "managed". The problem we're trying to get around is where raw data is just exposed. 
This is a bad design pattern, because APIs provide a level of indirection and isolation 
from the underlying sources or your solution will be brittle.

We adopt a standard 3 Layer technique used in data warehousing and data virtualisation tools:

1. RAW Layer
    
Define what is in the "RAW" files.
It's good practice not to use SELECT * in case things change. 
If they do break you want it to break here, and not further down.
Notice there may be a lot of use of backticks (`) which is not easy to read or nice to use.
typically very many sources, databases, files, APIs are found in this layer

2. MODEL Layer

This is the normalised 'business' view. If there was a data model it would be here
We expose from Layer 1 only what is needed for the API (Layer 3). 
Good practice to rename fields for consistency, benefits are:
 - name standardisation (for your org), 
 - alignment with a business glossary
 - remove need for quoting
Can also remove/select rows here too that we know are not of interest, or just "bad"
Think of this as a control point.
This is the base informtion for consumption layer 3.

3. CONSUMPTION Layer

Functions here are used in API endpoints and are based on user requirements
Principles of good API design need to apply.
Data is sourced from Layer 2 only (not Layer 1)


