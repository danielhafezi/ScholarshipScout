# ScholarshipScout

ScholarshipScout is a Multi-Agent AI based web scraper designed to search for fully funded doctorate positions from popular academic position websites. It helps users find PhD opportunities by scraping data from websites like ScholarshipDB and FindAPhD.

## Features

- Scrapes fully funded PhD positions from multiple sources.
- Filters positions based on desired countries.
- Saves results in CSV and Excel formats.
- Securely handles API keys using environment variables.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [License](#license)

## Installation

1. **Clone the repository**:
    ```sh
    git clone https://github.com/your-username/ScholarshipScout.git
    cd ScholarshipScout
    ```

2. **Create a virtual environment**:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install dependencies**:
    ```sh
    pip install -r requirements.txt
    ```

4. **Create a `.env` file**:
    ```sh
    touch .env
    ```

5. **Add your API key to the `.env` file**:
    ```env
    API_KEY=your_api_key_here
    ```

## Usage

1. **Run the script**:
    ```sh
    python ScholarshipScout.py
    ```

2. **Example usage**:
    ```python
    import asyncio
    from ScholarshipScout import main

    keywords = 'Computer Science'
    maxpage = 2
    countries = 'United States, Belgium, Netherlands, Germany, Switzerland'
    output = 'both'

    df = asyncio.get_event_loop().run_until_complete(main(keywords, maxpage, countries, output))
    print(df.head())
    ```

## Configuration

### Environment Variables

- `API_KEY`: Your API key for accessing the required services.

### Script Parameters

- `keywords`: Keywords to search for PhD positions.
- `maxpage`: Maximum number of pages to scrape.
- `countries`: Desired countries to filter the positions.
- `output`: Output format (`csv`, `xlsx`, or `both`).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or suggestions, please open an issue or contact the repository owner.

