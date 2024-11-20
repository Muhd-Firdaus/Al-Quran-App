# Al-Quran Web App

This is a simple Al-Quran web application built using HTML, CSS, JavaScript, and jQuery. The app interacts with the Al-Quran API to allow users to select and retrieve verses from any chapter (surah) of the Quran. The app dynamically loads and displays Quranic verses in an easy-to-read format.

## Features
- Dropdown to select a Surah from the Quran.
- Fetches Surah information and verses using the **Al-Quran API**.
- Displays the verses in an elegant, styled format.
- Responsive design with user-friendly UI.

## How It Works

1. **Surah Dropdown Population**:
   - On page load, the app makes an AJAX GET request to the Al-Quran API endpoint `http://api.alquran.cloud/v1/surah`.
   - The response contains details about all Surahs, which are dynamically added to a dropdown list using jQuery.

2. **Fetching and Displaying Ayahs**:
   - When the user selects a Surah from the dropdown and clicks the "GET" button, another AJAX GET request is sent to `http://api.alquran.cloud/v1/surah/{id}`.
   - The app processes the returned JSON response, extracts the verses (ayahs), and displays them in a scrollable container.

3. **Dynamic Rendering**:
   - Verses are displayed with large Arabic text and their corresponding verse numbers.
   - The app uses jQuery to manage dynamic content rendering.

4. **Error Handling**:
   - The app includes error-handling mechanisms to log and manage API failures gracefully.

## Technical Implementation

### 1. Frontend
- **HTML**: Provides the structure for the application, including the Surah dropdown, "GET" button, and result container.
- **CSS**: Adds styling to make the app visually appealing, including a centered card layout, hover effects for the button, and scrollable results.
- **JavaScript with jQuery**:
  - Handles DOM manipulation.
  - Manages asynchronous API calls using `$.ajax`.
  - Processes JSON data from the API and dynamically updates the DOM.

### 2. Backend/API
- The app interacts with the **Al-Quran API**:
  - `GET /v1/surah`: Retrieves the list of all Surahs.
  - `GET /v1/surah/{id}`: Retrieves details of a specific Surah, including its verses.

## How to Use

1. Clone this repository or download the HTML file.
2. Open the HTML file in any modern web browser.
3. Wait for the Surah dropdown to populate.
4. Select a Surah from the dropdown.
5. Click the "GET" button to fetch and display the Surah's verses.

## Prerequisites

- Internet connection (to fetch data from the Al-Quran API).
- Modern browser that supports JavaScript and AJAX.

## Limitations

- Requires the Al-Quran API to be online and accessible.
- The API requests use HTTP; for better security, it is recommended to switch to HTTPS.

## Credits

- **Frontend Development**: HTML, CSS, JavaScript, and jQuery.
- **API**: [Al-Quran Cloud API](http://alquran.cloud/api).
- **Author**: Muhd-Firdaus

## License

This project is licensed under the MIT License.

## Contact

For inquiries or contributions, please visit [GitHub](https://github.com/Muhd-Firdaus).
