# Rust Blog API
A simple blog-style REST API built with Iron web framework in Rust. The application provides basic blog post functionality with in-memory storage.
## Features
- Create and retrieve blog posts
- JSON response format
- Logging middleware
- UUID-based post identification
- In-memory database implementation

## API Endpoints
- GET /post_feed - Retrieve all posts
- POST /post - Create a new post
- GET /post/:id - Get a specific post by UUID

## Project Structure
```rust
src/
├── database.rs    - In-memory database implementation
├── handlers.rs    - HTTP request handlers
├── main.rs        - Application entry point
└── models.rs      - Data models (Post)
```
## Dependencies
- Iron - Web framework
- Router - URL routing
- Serde - Serialization/deserialization
- Chrono - DateTime handling
- UUID - Unique identifier generation
- Logger - Request logging

### Running the Application
- Clone the repository

Run the server:
```rust
cargo run
```
The server will start at 
```rust
localhost:8000
```
### Example Post Format
```rust
Copy{
  "title": "Example Post",
  "body": "Post content goes here",
  "author": "Author Name",
  "datetime": "2024-01-06T12:00:00Z",
  "uuid": "123e4567-e89b-12d3-a456-426614174000"
}
```
