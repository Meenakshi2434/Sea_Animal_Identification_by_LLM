# Sea_Animal_Identification_by_LLM
This project aims to identify a sea animal image using a LLM and outputsa detailed information about the species.

# OVERVIEW

Marine Species Identifier (Image-based)
This project identifies marine species from images using large vision-language models (VLMs) like OpenAI GPT-4 or Google Gemini Pro Vision. It generates structured species information, including common name, scientific name, family, size, color, habitat, and more.

📌 Features

- Image-based species identification

- Marine-specific filtering

- Structured JSON output with biological attributes

- Supports both GPT-4 (Vision) and Gemini Pro Vision

- Easy API setup via environment variables

🛠️ Setup and Configuration

1. Environment Variables

- You must provide your API key using environment variables:

For Gemini Pro Vision:

export GEMINI_API_KEY=your_gemini_api_key

2. Install Dependencies

pip install -r requirements.txt


⚙️ Code Overview

- setup_api()

- Initializes the Gemini API using the GEMINI_API_KEY.

- Raises an error if the key is missing.

- Configures genai with the API key.

- process_image(image_path, client)

- Loads an image from the given path.

- Sends it to the LLM for marine species identification.

- Parses and returns structured species data (e.g., name, scientific name, size, color, habitat).


🚀 Usage


- Run with Gemini Pro Vision


from Gemini_Code import main

main()


🧪 Example Output


{
  "Name": "Clownfish",
  
  "Scientific Name": "Amphiprion ocellaris",
  
  "Family": "Pomacentridae",
  
  "Size": "10–18 cm",
  
  "Color": "Orange with white bands",
  
  "Habitat": "Warm shallow reefs",
  
  "Diet": "Algae, zooplankton, small crustaceans",
  
  "Location": "Indo-Pacific",
  
  "Category": "Fish"
  
}
