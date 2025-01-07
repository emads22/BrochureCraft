
# BrochureCraft

## Overview 
**BrochureCraft** is a versatile Python-based tool designed to create brochures for companies in a variety of tones, including professional, humorous, friendly, serious, persuasive, etc. By leveraging advanced AI models like GPT (`gpt-4o-mini`), Claude (`claude-3-haiku-20240307`), and the open-source Ollama model (`llama3.2`), it analyzes website content to extract and summarize key details. The tool generates Markdown-formatted brochures that highlight company culture, customer information, and career opportunities, catering to prospective customers, investors, and recruits.

### Variants
- **Lite Version**: Utilizes the open-source Ollama model `llama3.2` for brochure generation.
- **Pro Version**: Employs the paid GPT model `gpt-4o-mini` for enhanced capabilities and flexibility.
- **UI Version**: Introduces a Gradio-powered user interface for streamlined brochure crafting, leveraging GPT (`gpt-4o-mini`) and Claude (`claude-3-haiku-20240307`) models.

## Features
- **Website Content Extraction**: Scrapes and parses website content, including titles, text, and links, while excluding irrelevant elements.
- **Relevant Links Filtering**: Uses AI to identify and prioritize links, such as "About", "Careers", or "Company" pages, for inclusion in the brochure.
- **Brochure Generation**: Generates professional or humorous Markdown-formatted brochures.
  - Lite: Powered by Ollama model `llama3.2`.
  - Pro: Powered by GPT model `gpt-4o-mini`.
  - UI: Offers a user-friendly interface using Gradio, powered by GPT and Claude models.
- **Dynamic Streaming**: Displays the brochure content dynamically as it is being generated.
- **Standard Brochure Creation**: Allows users to generate the full brochure at once using the `create_brochure` function.

## Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/emads22/brochure-craft.git
   cd brochure-craft
   ```
2. Ensure Conda is installed.
3. Create the Conda environment using the provided `brochure_env.yml` file:
   ```bash
   conda env create -f brochure_env.yml
   conda activate brochure
   ```
4. Configure the script to use the desired model:
   - Lite: Ensure access to the Ollama model `llama3.2`.
   - Pro: Ensure access to the GPT model `gpt-4o-mini` and set the API key in the `.env` file.
   - UI: Ensure access to both GPT (`gpt-4o-mini`) and Claude (`claude-3-haiku-20240307`) models, and set their respective API keys in the `.env` file.
5. Launch Jupyter Lab:
   ```bash
   jupyter lab
   ```
6. Open the corresponding notebook:
   - Lite: `brochure_craft_lite.ipynb`
   - Pro: `brochure_craft_pro.ipynb`
   - UI: `brochure_craft_ui.ipynb`
7. Run the cells step-by-step to generate the brochure.
8. Optionally, adjust constants like `MODEL` and `HEADERS` in the script if necessary.

## Usage
1. Open Jupyter Lab and navigate to the appropriate notebook:
   - Lite: `brochure_craft_lite.ipynb`
   - Pro: `brochure_craft_pro.ipynb`
   - UI: `brochure_craft_ui.ipynb`
2. Run the notebook cells sequentially.
3. To create a brochure dynamically:
   - Lite/Pro: Use the `stream_brochure` function:
     ```python
     stream_brochure("Company Name", "https://companywebsite.com")
     ```
   - UI: Launch the Gradio interface by running the last cell in `brochure_craft_ui.ipynb`. Enter the company name, website URL, and desired tone directly into the interface.
4. If you prefer not to stream the content, use the `create_brochure` function instead (Lite/Pro only):
   ```python
   create_brochure("Company Name", "https://companywebsite.com")
   ```
5. Modify the `brochure_system_prompt` to change the tone of the brochure in `brochure_craft_lite.ipynb` and `brochure_craft_pro.ipynb`. For example:
    - Uncomment the humorous prompt in the script to generate a lighthearted, entertaining brochure.
    - Adjust the prompt text to suit your specific needs, such as focusing on particular aspects of the company or adopting a custom tone.
6. Results are dynamically displayed in the Jupyter Lab interface or Gradio UI.

## Contributing
Contributions are welcome! Here are some ways you can contribute:
- Report bugs or issues.
- Suggest new features or improvements.
- Submit pull requests with bug fixes or enhancements.

## Author
- Emad  
  [<img src="https://img.shields.io/badge/GitHub-Profile-blue?logo=github" width="150">](https://github.com/emads22)

## License
This project is licensed under the MIT License, which grants permission for free use, modification, distribution, and sublicense of the code, provided that the copyright notice (attributed to [emads22](https://github.com/emads22)) and permission notice are included in all copies or substantial portions of the software. This license is permissive and allows users to utilize the code for both commercial and non-commercial purposes.

Please see the [LICENSE](LICENSE) file for more details.
