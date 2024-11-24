# RAG-for-Summarization
Created an LLM based summarization agent that summarizes an automotive issue 
using the given dataset. Input to the agent comes in the form of a json object with the 
following structure 
Input =  { ‘make’: ‘ford’, 
‘model’: ‘escape,  
‘year’: ‘2001’,  
‘issue’: ‘stuck throttle risk’} 
The agent retrieves the relevant documents in the dataset and summarize the 
issue using those documents. The final response of the agent includes both the 
retrieved documents as well as the final summarization. 
Dataset: Used the NHTSA Recalls dataset. The dataset is downloaded from the 
following link https://www.nhtsa.gov/nhtsa-datasets-and-apis. Download the 
FLAT_RCL.zip file. Relevant columns for this assignment are {make, model, year, 
defect summary, consequence summary, corrective summary}. All the three 
summaries is merged and considered as a single document for computing 
vector embeddings. For this assignment, a subset of this dataset by 
selecting data for only Ford and Toyota makes. 
Note: The embedding model used was SentenceTransformer('all-MiniLM-L6-v2'). For summarization, used 
the LLaMA 3.1 8b model. Used google collab for GPU 
resources.
