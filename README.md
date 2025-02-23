CSV Geocoding with OpenCage

Overview

This project provides a simple way to transform location data (addresses) from a CSV file into geographic coordinates (latitude and longitude) using the OpenCage Geocoder API.

Features

Batch geocoding of addresses from a CSV file

Support for OpenCage API with rate limit handling

Error handling for missing or invalid addresses

Outputs a new CSV file with latitude and longitude data

Prerequisites

Python 3.7+

OpenCage API Key (Get one from here)

Installation

Clone the repository:

git clone https://github.com/DhaneshGore/CSV-Geocoding-with-OpenCage-Transform-Location-Data-into-Coordinates.git
cd CSV-Geocoding-with-OpenCage-Transform-Location-Data-into-Coordinates

Install required dependencies:

pip install -r requirements.txt

Usage

Prepare a CSV file containing location data. The file should have a column named address.
Example input:

address
1600 Amphitheatre Parkway, Mountain View, CA
Times Square, New York, NY
Eiffel Tower, Paris

Run the script:

python geocode.py input.csv output.csv

The output CSV file will include latitude and longitude for each address.
Example output:

address,latitude,longitude
1600 Amphitheatre Parkway, Mountain View, CA,37.4221,-122.0841
Times Square, New York, NY,40.7580,-73.9855
Eiffel Tower, Paris,48.8584,2.2945

Configuration

Update the .env file with your OpenCage API Key:

OPENCAGE_API_KEY=your_api_key_here

Error Handling

Invalid addresses will be skipped with an error message.

If the API limit is exceeded, the script will wait and retry.

Contribution

Contributions are welcome! Feel free to submit issues or pull requests.

License

This project is licensed under the MIT License.

Author

Dhanesh Gore
