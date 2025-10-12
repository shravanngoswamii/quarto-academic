# Quarto Academic Template

A Quarto-based academic website template with publication management and people pages. Inspired by the [Cambridge Machine Learning Group website](https://mlg.eng.cam.ac.uk/).

## Introduction

This template provides a simple system for managing academic group websites with publications that automatically filter and display on individual people pages. Publications are defined once and automatically appear on relevant person pages based on author name matching.

## Setup

### Prerequisites

- [Quarto](https://quarto.org/docs/download/) version 1.3 or later

### Local Development

1. Clone or download this repository

2. Preview the website:
   ```bash
   cd quarto-academic
   quarto preview
   ```
   Opens at [http://localhost:4200](http://localhost:4200)

3. Build the static site:
   ```bash
   quarto render
   ```
   Output is generated in the `_site` folder

## Adding Publications

Publications are stored in `publications/` with each in its own folder following the naming pattern `YEAR-NUMBER_pub-number_short-title`.

### Steps

1. Copy `publications/_template/` and rename to `YEAR-NUMBER_pub-number_short-title`
2. Edit `index.qmd` with publication details
3. Add `featured.jpg` image (optional)

The `pub_number` field is used for sorting and display on the main publications page.

## Adding People

People pages are in `people/` with each person in a folder named `firstname-lastname`.

### Steps

1. Copy `people/_template/` and rename to `firstname-lastname`
2. Edit `index.qmd` with person details
3. Add profile image (e.g., `firstname.png`, `firstname-lastname.jpg`)
4. Update the `name` field to match exactly how it appears in publication author lists


## Notes

- Person names must match exactly between person pages and publication author lists for filtering to work
- YAML anchors (`&NAME` and `*NAME`) reduce repetition within the same file
- Publication `pub_number` is used for sorting (higher numbers appear first)

## Author

Created by [Shravan Goswami](https://shravangoswami.com)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

