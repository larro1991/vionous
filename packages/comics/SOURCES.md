# Data Sources

## Primary Source

### Grand Comics Database (GCD)

- **Website**: https://www.comics.org/
- **Data Dump Date**: 2021-05-29
- **Download Source**: Internet Archive
- **License**: Creative Commons Attribution-ShareAlike 4.0 International (CC-BY-SA 4.0)

The Grand Comics Database is an open, community-built database of comic book bibliographic data. It has been maintained since 1994 and contains detailed information about:

- Comic book issues and their publication details
- Series information and run dates
- Creator credits (writers, artists, inkers, colorists, letterers)
- Publisher information
- Character and feature appearances
- Reprint tracking
- Cover prices and page counts

## Data Extraction Methodology

### Tables Used

| Table | Records Used | Description |
|-------|--------------|-------------|
| gcd_series | 150,000 | Comic book series/titles |
| gcd_issue | 500,000 | Individual comic issues |
| gcd_story | 280,327 | Stories within issues |
| gcd_story_credit | 200,000 | Creator credits per story |
| gcd_creator | 47,000+ | Creator profiles |
| gcd_creator_name_detail | 26,255 | Creator name variants |
| gcd_publisher | 14,000+ | Publisher records |
| gcd_feature | 13,080 | Characters/features |
| gcd_reprint | 200,000 | Reprint relationships |

### Q&A Generation Process

1. **Direct Field Extraction**: Series names, publication dates, issue counts, prices
2. **Cross-Reference Linking**: Creator-to-series relationships via story credits
3. **Pattern Matching**: First appearances extracted from notes fields using regex
4. **Feature Enrichment**: Character creation years from gcd_feature metadata
5. **Reprint Chain Building**: Origin-to-target story relationships

### Data Quality Notes

- Some records contain uncertain data marked with "?" or "[uncertain]"
- Publication dates may include approximations like "[circa 1870's]"
- First appearance data derived from editorial notes, not always structured
- Non-English titles and publishers included (Japanese, French, German, etc.)

## License Compliance

This dataset inherits the **CC-BY-SA 4.0** license from the Grand Comics Database.

### You are free to:

- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material for any purpose, even commercially

### Under the following terms:

- **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made
- **ShareAlike** — If you remix, transform, or build upon the material, you must distribute your contributions under the same license

## Attribution

When using this data, please include:

```
Data derived from the Grand Comics Database (https://www.comics.org/)
Original data licensed under CC-BY-SA 4.0
```

## GCD Contribution

The Grand Comics Database is a volunteer-run project. If you find this data valuable, consider:

- Contributing to the GCD by adding or correcting data
- Donating to support their hosting and development costs
- Crediting GCD in any public use of derived works

Visit https://www.comics.org/ to learn more.
