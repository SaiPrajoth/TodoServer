
This is a simple Express.js HTTP server for managing a TODO list. It allows you to create, read, update, and delete TODO items. The server stores TODO data in-memory using a JSON file, allowing data persistence across server restarts.

## Features

- Create TODOs: You can create new TODO items by making a POST request to `/todos` with a JSON object representing the TODO item.

- Retrieve TODOs: You can retrieve all TODO items by making a GET request to `/todos`, or retrieve a specific TODO item by its ID with a GET request to `/todos/:id`.

- Update TODOs: Existing TODO items can be updated by making a PUT request to `/todos/:id` with a JSON object representing the updated TODO item.

- Delete TODOs: You can delete a TODO item by making a DELETE request to `/todos/:id`.

- Error Handling: The server handles errors gracefully and returns appropriate HTTP status codes (e.g., 404 Not Found) for invalid requests.

## Getting Started

1. Clone this repository to your local machine.

2. Install the required dependencies using `npm install`.

3. Start the server by running `npm start`.

4. You can access the server locally at `http://localhost:3000`.

## API Endpoints

- GET /todos: Retrieve all TODO items.
  - Example: `GET http://localhost:3000/todos`

- GET /todos/:id: Retrieve a specific TODO item by ID.
  - Example: `GET http://localhost:3000/todos/123`

- POST /todos: Create a new TODO item.
  - Example: `POST http://localhost:3000/todos`
  - Request Body: `{ "title": "Buy groceries", "description": "I should buy groceries" }`

- PUT /todos/:id: Update an existing TODO item by ID.
  - Example: `PUT http://localhost:3000/todos/123`
  - Request Body: `{ "title": "Buy groceries", "completed": true }`

- DELETE /todos/:id: Delete a TODO item by ID.
  - Example: `DELETE http://localhost:3000/todos/123`

## Data Persistence

The server stores TODO data in an in-memory JSON file (`a.json`). This allows data to persist even after restarting the server. However, keep in mind that this is a simple demonstration, and in a production environment, you may want to use a database for data storage.

## Error Handling

For any routes not defined in the server, the server will return a 404 Not Found response.

## Testing

To run tests for this server, use the `npm run test-todoServer` command in the terminal.

## Author

Sai Prajoth

## License

This project is licensed under the License - see the LICENSE.md file for details.

