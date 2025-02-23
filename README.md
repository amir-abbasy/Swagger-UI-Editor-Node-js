# README.md

## Overview
In Node.js, we typically define Swagger schemas at the top of each API endpoint, which can be repetitive and time-consuming. To streamline this process, I developed a **Swagger Schema Helper** that allows you to write API schemas in a structured **JSON format** instead of embedding them directly in the code. 

Additionally, I have created a **web-based schema generator** accessible at `/swagger-editor-ui`. This webpage provides an interface to generate and visualize Swagger schemas dynamically, making API documentation more efficient and manageable.

## Features
- **Simplified Schema Writing**: Define schemas in a structured JSON file rather than within the API code.
- **Automatic Swagger Schema Generation**: Converts JSON schema definitions into valid Swagger (OpenAPI) specifications.
- **Web-Based Editor**: Access a UI at `/swagger-editor-ui` to generate and modify schemas visually.
- **Consistent API Documentation**: Ensures all endpoints follow a structured and uniform documentation style.

## Installation & Setup

1. **Clone the Repository**
   ```sh
   git clone <your-repo-url>
   cd <your-project-directory>
   ```

2. **Install Dependencies**
   ```sh
   npm install
   ```

3. **Run the Application**
   ```sh
   node server.js
   ```

4. **Access the Swagger Schema Generator**
   Open your browser and navigate to:
   ```sh
   http://localhost:<PORT>/swagger-editor-ui
   ```

## How It Works
1. Write API schemas in a dedicated JSON file.
2. The helper processes these JSON files and automatically injects the schema into your API.
3. Visit `/swagger-editor-ui` to edit and visualize your API schema dynamically.
4. The generated Swagger JSON can be exported and integrated with your API documentation tools.

## Example JSON Schema Format
```json
{
  "post": {
    "requestBody": {
      "content": {
        "application/json": {
          "schema": {
            "$ref": "#components/schema/User"
          }
        }
      }
    },
    "responses": {
      "200": {
        "content": {
          "application/json": {
            "schema": {
              "$ref": "#components/schema/User"
            }
          }
        }
      }
    }
  }
}
```

## Future Enhancements
- **Support for More API Methods** (PUT, DELETE, PATCH)
- **Customizable Theme for the UI Editor**
- **Export to YAML Format**

## License
This project is licensed under the MIT License.

## Contribution
Feel free to submit issues or pull requests to enhance functionality!

