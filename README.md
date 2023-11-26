# Startup Name Generator with ChatGPT and Domain Availability Checker

## Overview

ChatGPT Name Generator is a small utility that uses ChatGPT to generate creative and unique startup name ideas based on a given description. Additionally, this utility checks for the availability of domain names for the generated startup names. It is a handy tool for entrepreneurs, helping them to find a suitable and available domain name for their startups.

## Installation

### Prerequisites

- Python 3.6 or higher
- `pip` for installing the required packages

### Steps

1. Clone this repository to your local machine:

```bash
git clone https://github.com/mylh/chatgpt-name-generator.git
cd startup-name-generator
```

2. Create a virtual environment (optional but recommended):

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

3. Install the required packages:

```bash
pip install -r requirements.txt
```

4. Set up your OpenAI API key as an environment variable:

```bash
export OPENAI_API_KEY="your_api_key"  # On Windows, use `set OPENAI_API_KEY=your_api_key`
```

**Note**: Replace `your_api_key` with your actual OpenAI API key.

## Usage

Run the `namegen.py` script with a description of your startup:

```bash
python namegen.py --prompt "A platform for connecting freelance designers with clients" --tld="com"
```

The script will generate a list of potential startup names and check the availability of the corresponding domain names. The results will be displayed in the terminal.

### Example Output

```
Getting Ideas for "A platform for connecting freelance designers with clients"...
Generated names: PixelMatch, DesignHive, WorkPalette, Artista, BrightCrowd, TalentedTies, DesignDuo, CreateConnect, DesignVine, ProPalette.
Checking https://pixelmatch.com
✗ Got DNS response
Checking https://designhive.com
✗ Got DNS response
Checking https://workpalette.com
✗ Got DNS response
Checking https://artista.com
✗ Got DNS response
Checking https://brightcrowd.com
✗ Got DNS response
Checking https://talentedties.com
✔ Domain talentedties.com is available!
Checking https://designduo.com
✗ Got DNS response
Checking https://createconnect.com
✗ Got DNS response
Checking https://designvine.com
✗ Got DNS response
Checking https://propalette.com
✗ Got DNS response
---
Available domains:
talentedties.com
```

## Additional Options

- To specify a different Top-Level Domain (TLD), use the `--tld` option:

```bash
python namegen.py --prompt "A platform for connecting freelance designers with clients" --tld "io"
```

- To provide a comma-separated list of names to check for availability, use the `--names` option:

```bash
python namegen.py --names "DesignLink, CreativeConnect, ArtistryHub, DesignerMatch, DesignBridge"
```

- To save the available domain names to an output file, use the `--output` option:

```bash
python namegen.py --prompt "A platform for connecting freelance designers with clients" --output available_domains.txt
```

- To specify OpenAI model to use, use the `--model=gpt-3.5-turbo` option

- To specify DNS servers use `-dns-server="<dns-server1>,<dns-server2>"` option

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
