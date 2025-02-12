
## Setup

1. Create Python virtual environment:
```bash
# Create a virtual environment in ./py310
python3 -m venv py310

# Activate the virtual environment
# On Unix/macOS:
source py310/bin/activate
# On Windows:
.\py310\Scripts\activate
```

2. Install dependencies:
```bash
# Install required packages
pip install -r requirements.txt

# Install Playwright's Chromium browser (required for web scraping)
python -m playwright install chromium
```

## Docker Setup

### Prerequisites
- Docker installed on your machine
- Docker Compose installed on your machine

### Running with Docker

1. Make sure you have the virtual environment activated.

2. Build and start the container:
```bash
# Build and run the container
docker-compose up --build

# Or run in detached mode
docker-compose up --build -d
```

3. Access the application at `http://localhost:3000`

### Docker Commands

- Stop the container:
```bash
docker-compose down
```

- View logs:
```bash
docker-compose logs -f
```

- Rebuild after changes:
```bash
docker-compose up --build
```

## Tools Included

- Web scraping with JavaScript support (using Playwright)
- Search engine integration (DuckDuckGo)
- LLM-powered text analysis
- Process planning and self-reflection capabilities

## Testing

The project includes comprehensive unit tests for all tools. To run the tests:

```bash
# Make sure you're in the virtual environment
source py310/bin/activate  # On Windows: .\py310\Scripts\activate

# Run all tests
PYTHONPATH=. python -m unittest discover tests/
```

The test suite includes:
- Search engine tests (DuckDuckGo integration)
- Web scraper tests (Playwright-based scraping)
- LLM API tests (OpenAI integration)

## Background

For detailed information about the motivation and technical details behind this project, check out the blog post: [Turning $20 into $500 - Transforming Cursor into Devin in One Hour](https://yage.ai/cursor-to-devin-en.html)

## License

MIT License


