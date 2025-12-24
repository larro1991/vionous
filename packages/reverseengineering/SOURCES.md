# Data Sources

## Primary Source

### Reverse Engineering Stack Exchange

- **Website**: https://reverseengineering.stackexchange.com
- **License**: Creative Commons Attribution-ShareAlike 4.0 International (CC-BY-SA 4.0)

## Data Extraction Methodology

### Process

1. Downloaded data dump from Internet Archive
2. Parsed Posts.xml to extract questions and answers
3. Matched answers to parent questions
4. Selected best answer per question:
   - Accepted answer (if exists)
   - Highest-scored answer with Score >= 1
5. Cleaned HTML to plain text
6. Preserved code blocks with markdown formatting
7. Filtered short/empty responses

### Quality Filters

- Minimum answer score: 1
- Minimum question title length: 10 characters
- Minimum answer length: 50 characters
- Maximum question length: 2000 characters
- Maximum answer length: 3000 characters

### Statistics

- Total questions processed: 9,681
- Questions with answers: 7,535
- Q&A pairs created: 7,301
- Accepted answer ratio: 55.3%

## License Compliance

This dataset inherits the **CC-BY-SA 4.0** license from Stack Exchange.

### Attribution

When using this data, please include:

```
Data derived from Reverse Engineering Stack Exchange (https://reverseengineering.stackexchange.com)
Original data licensed under CC-BY-SA 4.0
```
