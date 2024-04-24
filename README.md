# CORS Proxy Microservice

This is a simple Python Flask microservice that serves as a CORS (Cross-Origin Resource Sharing) proxy. It allows you to retrieve resources from a remote URL on a different site, bypassing CORS restrictions.

## Prerequisites

- Python 3.x
- Flask
- Flask-CORS

## Installation

1. Clone the repository or download the source code:

   ```
   git clone https://github.com/EugeneTeplitsky/cors-proxy-microservice.git
   ```

2. Navigate to the project directory:

   ```
   cd cors-proxy-microservice
   ```

3. Install the required dependencies:

   ```
   pip install -r requirements.txt
   ```

## Usage

1. Run the microservice:

   ```
   python app.py
   ```

   The microservice will start running on `http://localhost:5000`.

2. Send a GET request to the `/proxy` endpoint with the `url` parameter containing the URL of the remote resource you want to retrieve:

   ```
   GET http://localhost:5000/proxy?url=https://example.com/api/data
   ```

   Replace `https://example.com/api/data` with the actual URL you want to retrieve.

3. The microservice will retrieve the resource from the specified URL and return the response to the requester, bypassing any CORS restrictions.

## Configuration

- The microservice runs on port 5000 by default. You can modify the port by changing the `app.run()` statement in the `app.py` file.

## Error Handling

- If the `url` parameter is missing in the request, the microservice will return an error response with a status code of 400 (Bad Request) and an error message in JSON format.

- If an error occurs during the request processing (e.g., invalid URL, network issue), the microservice will return an error response with a status code of 500 (Internal Server Error) and an error message in JSON format.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgements

- [Flask](https://flask.palletsprojects.com/)
- [Flask-CORS](https://flask-cors.readthedocs.io/)
- [Requests](https://docs.python-requests.org/)
