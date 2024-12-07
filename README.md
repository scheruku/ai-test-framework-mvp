
# AI-Driven Automated UI Testing (MVP)

This project is a demonstration of a simple Flask-based web application coupled with a Selenium-based test agent. The web app features:
- A **Login Page** to authenticate a user.
- A **Products Page** where a logged-in user can add and view furniture product information.
- Sample static images to give the pages a more realistic look.

An accompanying **MVP test agent** (using Selenium) is included to automate UI testing of the application’s login and product addition functionality.

## Features

- **Flask Web App**:
  - `/login`: Simple login form that requires username and password.
  - `/products`: Accessible post-login, allows adding products with name, description, and optional image. Displays a list of added products.
  
- **MVP Test Agent (Selenium)**:
  - Automates the login process.
  - Navigates to the products page and adds a product.
  - Verifies that the product was successfully added.

This forms a baseline system to which an AI-driven LLM agent can later be integrated to dynamically generate or refine test scripts.

## Prerequisites

- **Python 3.x**  
- **Pip** (Python package manager)
- **WebDriver** (e.g., ChromeDriver) installed and added to your system PATH.

## Installation

1. **Clone the Repository**:  
   ```bash
   git clone https://github.com/your-username/ai-test-framework-mvp.git
   cd ai-test-framework-mvp
   ```

2. **Install Dependencies**:  
   ```bash
   pip install -r requirements.txt
   ```
   
   The `requirements.txt` file should contain:
   ```
   flask
   selenium
   ```

3. **Set Up WebDriver**:
   - Download [ChromeDriver](https://chromedriver.chromium.org/downloads) (if testing with Chrome).
   - Ensure `chromedriver` is in your PATH.

4. **Run the Flask App**:  
   ```bash
   python app.py
   ```
   
   By default, the app runs on `http://127.0.0.1:5000`.

## Usage

1. **Open the Application**:
   - In your browser, go to `http://127.0.0.1:5000/login`.
   - Enter `admin` as username and `password123` as password (hardcoded credentials).
   - On successful login, you will be redirected to the Products page.

2. **Add Products**:
   - On the `/products` page, fill in the name and description fields.
   - Optionally, provide an image URL. If omitted, a default image is used.
   - Submit the form to see your product listed.

## Running the MVP Test Agent

1. **Ensure the App is Running**:  
   Make sure `app.py` is still running and accessible at `http://127.0.0.1:5000`.

2. **Run the Test**:
   ```bash
   python test_agent.py
   ```
   
   The agent will:
   - Open the login page.
   - Enter the credentials and log in.
   - Verify that the products page loads.
   - Add a "Test Chair" product.
   - Check that the product appears on the page.

3. **Test Results**:  
   The test results will print to the console. If successful, no errors will be displayed.

## Future Plans

- **AI Integration**:  
  The current solution is an MVP without direct AI involvement. The next step is to integrate an AI agent (LLM) that:
  - Reads the application context.
  - Dynamically generates test steps instead of relying on hardcoded scripts.
  - Adapts tests as the UI evolves.

- **Enhanced Test Coverage**:
  - Add more complex scenarios and input validations.
  - Integrate visual regression testing and complex authentication flows.

## Contributing

Contributions are welcome. You can:
- Add new features.
- Improve code readability.
- Integrate with an LLM for dynamic test code generation.

## License

This project is provided under the [MIT License](LICENSE).

---

**End of README**
