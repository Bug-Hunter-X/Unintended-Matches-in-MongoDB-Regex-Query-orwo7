# Unintended Matches in MongoDB Regex Query

This repository demonstrates a common issue with MongoDB regex queries: unintended matches due to lack of indexing or overly broad regular expressions.

## The Problem

The provided `bug.js` script uses a regular expression to query a MongoDB collection. However, without a proper index or a more specific regex, this query can return many more results than expected, impacting performance and potentially returning incorrect data.

## The Solution

The `bugSolution.js` script addresses this by:
1. **Adding an index:** This significantly speeds up queries.
2. **Refining the regex:**  A more precise regex reduces the chance of unintended matches.

## How to Reproduce

1. Clone this repository.
2. Ensure you have MongoDB installed and running.
3. Set up a MongoDB connection string and update the code as needed.
4. Run `bug.js`. Observe the excessive or unexpected results.
5. Run `bugSolution.js`. Observe the improved results.

## Contributing

Contributions are welcome!