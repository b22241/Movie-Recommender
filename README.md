
# Movie-Recommender

A simple movie recommendation application built with Python, Streamlit, and precomputed similarity data.

## Features
- Displays movie recommendations based on a selected movie.
- Uses precomputed similarity matrices for fast recommendations.
- Designed for local deployment using Streamlit.

## Installation

### Prerequisites
Ensure you have Python installed (Python 3.10 or above is recommended).

### Steps
1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd Movie-Recommender
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv .venv
   # On Windows
   .venv\Scripts\activate
   # On MacOS/Linux
   source .venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the application:
   ```bash
   streamlit run app.py
   ```

5. Access the application in your browser at `http://localhost:8501`.

## File Structure
```
Movie-Recommender/
|
├── app.py              # Main application code.
├── requirements.txt    # Python dependencies.
├── similarity.pkl      # Precomputed similarity matrix.
├── movie_dict.pkl      # Movie dictionary.
├── setup.sh            # Shell script for deployment setup (optional).
├── Procfile            # Configuration for deployment on Heroku.
├── .gitignore          # Files and directories to ignore in version control.
```

## Usage
1. Select a movie from the dropdown menu in the Streamlit app.
2. View the list of recommended movies based on similarity.

## Key Functions
### `fetch_foster(movie_id)`
Fetches additional information about a movie using an API request (e.g., Douban API).

### `recommend(movie)`
Generates a list of recommended movies based on the input movie and the similarity matrix.

## Deployment
To deploy the app on a platform like Heroku:
1. Ensure the `requirements.txt` and `Procfile` are properly configured.
2. Push the repository to a Heroku app.
3. Follow Heroku’s deployment instructions.

## Dependencies
Key dependencies include:
- `streamlit`: For creating the web application interface.
- `pandas`: For data handling and manipulation.
- `pickle`: For loading precomputed data (similarity matrix and movie dictionary).

Install all dependencies using the provided `requirements.txt` file.

## Contributing
Feel free to fork the repository and submit pull requests. Suggestions and improvements are welcome!

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
